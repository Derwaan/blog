---
layout: post
title: How to emulate a webcam stream with Python3, OpenCV and v4l2loopback
---

In this article, we are going to create a virtual device using v4l2loopback on which we are going to write frames with OpenCV.

This article assumes that Python3, pip3 and OpenCV are installed.
The techniques and tools presented in this article were tested on Ubuntu 18.04.

## Context

At Nalys, a previous Qt application was created during a project. This application reads the video device of a tablet and performs some video processing algorithms with OpenCV. This [blog post](https://nalys-taas-projects.gitlab.io/internal/taas_blog/post/qt_app_led_detection/) describes in more depth the application. But to test the application, you would need to have a video device plugged to your computer. In order to remove this constraint, a python script was created. This script emulates a video device that the Qt application will read and use for the video processing.

Before writing the script, some research were necessary in order to find the correct tools for such task.

### v4l2 and v4l2loopback

V4l2 or "Video4Linux" is an API that allows to capture video device. V4l2loopback is a kernel module not installed by default that can create virtual video devices (or "dummy devices") that any v4l2 application would be able to read.

For our case, v4l2loopback will be used to create a dummy device that the Qt application will be able to read. But in order to write frame to this virtual device, we need something else.

### OpenCV

OpenCV is a famous library for video processing. In our script, we will only use a small portion of the capabilities of this library to create frame for our v4l2loopback device.

## Preparations

Before writing our Python3 script, we need to make some preparations.
In order for our script to write frames on a virtual device, we will need to install and use the v4l2loopback kernel module that creates such devices.

### Install v4l2 and v4l2loopback

In order to create a dummy device that will be used by OpenCV to display the frames, we will need to install [https://github.com/umlaeute/v4l2loopback](v4l2loopback).

#### With a package manager

A Debian package is available for Debian-based distribution.

```bash
$ sudo apt install v4l2loopback-dkms
```

#### From source

With Ubuntu 18.04, there can be some issues with this package and we might want to install v4l2loopback from source.
To do so, we will need to have the latest kernel headers for our system:

```bash
$ sudo apt install linux-headers-$(uname -a)
```

After that, we can clone the v4l2loopback [https://github.com/umlaeute/v4l2loopback](repository) and install the kernel module from the source:

```bash
$ git clone https://github.com/umlaeute/v4l2loopback
$ cd v4l2loopback
$ make
$ sudo make install
$ sudo depmod -a
```

We might need to install `v4l-utils` if it is not present in our system yet.

```bash
$ sudo apt install v4l-utils
```

In order to use v4l2 in Python3, we will need to install the package `v4l2` with pip3.
But, currently this package has a bug with Python3 and it need to be installed from a specific commit that fixes the issue.
In order to install the package with pip3, we will also need to have `bzr` installed.

```bash
$ sudo apt install bzr
$ pip3 install -e bzr+lp:~jgottula/python-v4l2/fix-for-bug-1664158
```

### Creating a dummy device

Now that we have all the requirements installed, it is time to create our first dummy device.

Using v4l2loopback kernel module, we can add our freshly installed kernel module:

```bash
$ sudo modprobe v4l2loopback
```

With v4l-utils, we can check if the virtual video device is created:

```bash
$ v4l2-ctl --list-device
```

We should see a dummy device in the list.  
We will consider `/dev/video0` as the virtual device created by v4l2loopback for the next part of this article.

## Python script

Now that every things is set up, let's move on to the actual script.

### Opening the virtual device
Before writing our frames to the virtual device, we must create a v4l2 format.
This format will be then written into the device with ioctl.

```python
import sys, fcntl
from v4l2 import *

width = 1920
height = 1080
device = open('/dev/video0', 'wb')

# Setup format
fmt                      = v4l2_format()
fmt.type                 = V4L2_BUF_TYPE_VIDEO_OUTPUT
fmt.fmt.pix.field        = V4L2_FIELD_NONE
fmt.fmt.pix.pixelformat  = V4L2_PIX_FMT_BGR24
fmt.fmt.pix.width        = width
fmt.fmt.pix.height       = height
fmt.fmt.pix.bytesperline = width * 3
fmt.fmt.pix.sizeimage    = width * height * 3

# Writing the format to the virtual device
if fcntl.ioctl(device, VIDIOC_S_FMT, fmt) == 0: print("Running on {}".format(device_name))
else: sys.exit()
```

### Generate a frame
Once we have the device open with the correct format, we can generate frames with numpy and OpenCV.
We use an infinite loop to keep sending new frames to the dummy device.

```python
import cv2
import numpy as np

while True:
  frame = np.zeros((height, width, 3), np.uint8) # Generate a black frame
  cv2.circle(frame, (width / 2, height / 2), 10, (255, 255, 255), -1) # Filled circle
  device.write(frame) # Write the frame to the virtual device
```

## Reading our virtual device

We can now run our script and use VLC to check if our virtual device is displaying our frames.

```bash
$ python3 our_script.py &
$ vlc v4l2:///dev/video0
```

## Clean it up

To remove the virtual device, you can simply remove the kernel module:

```bash
$ sudo rmmod v4l2loopback
```

