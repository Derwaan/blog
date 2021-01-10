---
layout: post
title: Tout ce que j'ai appris - Mai 2020
---

Premier article d'une série qui, je l'espère, va durer longtemps !
Je vais recenser ici une tonne d'informations que j'ai apprises chaque mois.
Ce premier article risque d'être plus conséquent car il reprend des informations apprises sur plusieurs mois.
Il n'y aura pas vraiment de structure.
Juste une liste avec chaque à point une nouvelle information.
Alors c'est parti !

- Pour construire des objectifs sur le long-terme (e.g. devenir bodybuilder), il faut commencer par des petites habitudes sur le court-terme (faire une séance de sport de 30 minutes tous les jours).
Plus l'habitude est petite et bien définie plus il sera facile de la suivre. En accumulant ces petites habitudes sur le long-terme, on se rapproche petit à petit de nos grands objectifs.

- Quand on commence dans l'investissement, il vaut mieux se concentrer sur un seul véhicule financier à la fois (bourse, immobilier, business) avant de se lancer dans le suivant.
Se diversifier c'est bien mais c'est mieux de se restreindre au sein d'un seul véhicule.

- J'ai découvert le principe d'[Evergreen's Note](https://notes.andymatuschak.org/z4SDCZQeRo4xFEQ8H4qrSqd68ucpgE6LU155C) d'[Andy Matuschak](https://andymatuschak.org/).
Je vous conseille vivement d'aller jeter un coup d'oeil à son site et d'expérimenter avec.
Le principe est d'écrire des notes atomiques (c-à-d sur une idée seulement, qui ne peut pas être divisée) avec le plus de liens possibles vers d'autres notes.

- La méthode [Zettelkasten](https://zettelkasten.de/posts/overview/).
C'est une méthode de prise de notes (oui je raffole beaucoup de ce genre de méthodes) permettant de stocker et de retrouver facilement tout ce qu'on lit et apprend.
Avec un système de numérotation particulier qui permet de créer une arborescence de ses notes, il est facile de créer des cheminements d'idées avec cette méthode.

- Dans le livre [The STEMpunk Project](https://www.amazon.fr/STEMpunk-Project-Trent-Fowler/dp/1521994676), Trent Fowler parle de la différence entre l'*intelligence innée* et l'*intelligence incrémentale*.
Si on suppose que nous avons une intelligence innée alors nous naissons tous avec un niveau d'intelligence défini et celle-ci ne peut changer au cours de notre vie.
À l'inverse, si vous avons une intelligence incrémentale, il est possible d'améliorer petit à petit notre intellect.

- Toujours dans le livre [The STEMpunk Project](https://www.amazon.fr/STEMpunk-Project-Trent-Fowler/dp/1521994676), la notion de *semignotism* est abordée.
L'idée selon laquelle, lorsque l'on commence à apprendre une nouvelle matière, *on ne sait pas ce qu'on ne sait pas*.
Autrement dit, nous ne savons pas quelles connaissances manquent à notre savoir.
Cette notion rejoint ce que dit Nathaniel Drew dans sa vidéo [How I Learn Things Online (Way More Efficiently)](https://www.youtube.com/watch?v=rVmMbMa3ncI).

- Dans la vidéo [How I Learn Things Online (Way More Efficiently)](https://www.youtube.com/watch?v=rVmMbMa3ncI), Nathaniel Drew donne trois étapes pour apprendre de nouvelles choses via Internet.
  1. Absorber le plus de contenu possible afin de déterminer si ce que l'on cherche à apprendre nous intéresse vraiment.
  Cela permet aussi de déterminer quels concepts il faut acquérir car, en commençant, on n'a pas conscience de la matière qu'il va falloir accumuler.
  2. Trouver les bonnes ressources.
  Avec le nombre d'influenceurs, de vidéastes, de blogs, etc. qui grandit sur Internet il est parfois difficile de trouver la pépite qui va nous permettre d'apprendre de nouvelles choses.
  3. Construire quelque chose.
  Dans tout projet d'apprentissage, il faut, à un moment ou à un autre, construire quelque chose.
  C'est la meilleure façon d'apprendre tout simplement.

- Dans la vidéo [Transforming Code into Beautiful, Idiomatic Python](https://www.youtube.com/watch?v=OSGv2VnC0go), Raymond Hettinger nous apprend à écrire du code Python bien plus performant.
La clé derrière tout ça est de bien faire attention à utiliser des structures itérables.
Par exemple:
```python
for i in range(len(l)):
    # Do stuff...
```
n'est pas une bonne façon de parcourir une liste.
La bonne méthode est:
```python
for x in [a, b, c]:
    # Do stuff...
```

- Toujours dans la vidéo [Transforming Code into Beautiful, Idiomatic Python](https://www.youtube.com/watch?v=OSGv2VnC0go), on apprend qu'il est possible de déterminer si on est sorti d'une boucle `for` normalement ou au moyen d'un `break` avec une boucle `for-else`:
```python
for x in [a, b, c]:
    # Do stuff or break...
else:
    # No break occured, the loop exit normally
```

- Une technique de brainstorming que j'ai découverte pendant mon [expérience de prise de notes](https://derwaan.com/blog/2020/05/14/note-taking-experiment-part-1.html).
En utilisant des petites cartes cartonnées pour y écrire les idées, on se retrouve rapidement avec une tonne de cartes que l'on peut manipuler sur son bureau, bouger, regrouper, etc.
Le fait de pouvoir manipuler physiquement ses idées rajoute quelque chose de très intéressant au brainstorming.
De plus, c'est un très bon moyen de visualiser ce qu'on est en train de construire.

- Le livre papier ou un carnet pour prendre des notes aide la mémorisation spatiale.
C'est encore une raison de plus pour laquelle je continue à utiliser un carnet.
Je sais **où** se trouve mes notes dans mon carnet.
De la même façon entre un livre physique et un e-book, je sais **où** dans le livre se trouve l'information que je recherche.

- Pour se motiver, il est important de se créer des pensées positives.
Par exemple, si on cherche à se motiver pour aller à la salle de sport on aura tendance à penser "Je vais à la salle de sport pour être en forme".
Cependant, penser de cette façon laisse notre subconscient imaginer que si on va à la salle de sport c'est parce qu'on est pas en forme.
Ça peut alors nous démotiver et tous nos efforts partent à la poubelle.
Une autre façon de penser serait de dire "Je vais à la salle de sport car j'aime prendre soin de mon corps".
De cette façon, notre esprit est bien plus positif et motivé à faire du sport.

- On ne retient pas bien les prénoms car ils ne créent pas d'association avec d'autres idées dans notre mémoire.

- Le *machine learning* n'est pas un nouvel outil qui a été créé récemment.
C'est un outil que l'on utilise maintenant pour résoudre des **nouveaux types de problèmes**.
On utilise le machine learning pour résoudre des problèmes *business* (Quelle est la meilleure campagne marketing ? Quel email va me permettre de convertir le plus d'utilisateurs ? ...)

- Une *fonction pure* est une fonction qui avec les mêmes paramètres d'entrée fournira toujours le même résultat.

- Les *unions* en C.
Cela permet de regrouper plusieurs variables derrière une seule (celle qui prend le plus de place).
C'est utilisé, par exemple, dans une structure lorsqu'une seule variable est utilisée à la fois:
```c
struct foo {
  bool isInt
  union {
    int a
    double b
  }
}
// Stuff...
if(f.isInt) {
  // use f.a
} else {
  // use f.b
}
```

- `set -euxo pipefail` est une commande qui permet de repérer toutes les erreurs dans un script bash.
  - `set -e` permet de stopper l'exécution du script à la moindre erreur
  - `set -x` permet d'afficher les commandes exécutées
  - `set -u` permet de stopper l'exécution du script dès qu'une variable n'a pas été définie
  - `set -o pipefail` permet de détecter les erreurs dans les pipes (attention c'est un *bashism* donc cela ne peut pas être utilisé dans un script pure shell)

- Le *dollar cost averaging* est une méthode permettant d'investir des petits montants tous les mois (par exemple) dans la bourse.
De cette façon, l'argent investi est réparti sur une longue période et les gains sont en moyenne supérieurs à un investissement ciblé sur une courte période.

- Dans sa vidéo [Le principe de Pareto (et ses limites)](https://www.youtube.com/watch?v=paQzJCfo6Rw), Chat Sceptique nous explique que le principe de Pareto, qui dit que 80% des résultats sont fournis par 20% des efforts, a ses limites.
En effet, ce principe ne montre pas les coûts cachés des efforts nécessaires.
Par exemple, on pourrait dire que pour réduire les risques de cancer il suffit de supprimer la tabagisme mais cela ne dit pas quel est le coût de supprimer le tabagisme.

- Le time boxing est une technique de productivité très utilisée.
Elle consiste à se fixer une période de temps précise pour une tâche et de s'y tenir.
Cela permet de rajouter une deadline personnelle et de rester concentré sur son travail.
Cela rejoint la [loi de Parkinson](https://fr.wikipedia.org/wiki/Loi_de_Parkinson) selon laquelle un employé prendra toujours tout le temps qui lui est alloué pour faire une tâche même si celle-ci aurait pu être terminée plus rapidement.

- Dans sa vidéo [How to Remember What You Read | How I Digest Books (Plus: A Few Recent Favorite Books)](https://www.youtube.com/watch?v=YQOrqAKKcUQ), Tim Ferris explique sa méthode pour assimiler tout ce qu'il lit.
Ce que j'en ai retenu est qu'il prend beaucoup de notes directement dans le livre et, surtout, après avoir terminé un livre, il crée un index au début de celui-ci avec les idées importantes et les pages qui s'y rapportent.
De cette manière, il peut rapidement retrouver les informations qui l'intéressent en utilisant l'index au début du livre.

- Dans le livre [The Productivity Project: Accomplishing More by Managing Your Time, Attention, and Energy](https://www.amazon.fr/Productivity-Project-Accomplishing-Managing-Attention/dp/1101904038), Chris Bailey explique que nous sommes plus apte à faire du travail créatif en début de journée.
Du coup, j'utilise ce principe pour relire mes notes dans mon journal le matin.
Cela me permet de générer de nouvelles idées et directement déterminer quelles seront mes prochaines étapes pour la suite de ma journée.

- Un business doit savoir cibler un groupe plus petit afin de lui fournir le produit adéquat.
On parle souvent de cibler soit une niche très petite soit cibler un public le plus large possible.
Le problème en ciblant un très grand groupe c'est qu'on ne sait pas à qui on s'adresse.
Tandis qu'en ciblant une petit niche de personnes (semblables à nous), on sait ce que ces gens veulent et on peut plus facilement communiquer avec eux et déterminer leurs besoins.

- Le principe de Netflix.
Netflix ne diffuse pas de programmes de sport car une fois la saison terminée plus personne ne reviendra voir ces épisodes.
À l'inverse, Netflix diffuse des séries qui restent intéressantes à regarder peu importe la période.
Ce principe peut s'appliquer à tout créateur de contenu.
Créer un article, une vidéo, un podcast qui garde son intérêt même bien plus tard que sa date de diffusion.

- Dans une conférence TedX [How to know your life purpose in 5 minutes](https://www.youtube.com/watch?v=om-XLTeQee0), Adam Leipzig explique que pour trouver son *but dans la vie* il faut essayer de compléter cette phrase qui rejoint le principe d'[Ikigai](https://fr.wikipedia.org/wiki/Ikigai):
> "Je fais **(qu'est-ce que j'aime?)** pour **(qui je veux aider?)** afin qu'ils puissent **(qu'est-ce que j'apporte aux autres?)**"

- Lorsqu'on apprend quelque chose, 50% du temps est passé à l'apprentissage et 50% du temps est passé au partage de cet apprentissage aux autres.
Cela rejoint la [technique de Feynman](https://evernote.com/blog/fr/la-technique-feynman-peut-vous-aider-a-ameliorer-votre-travail/#:~:text=La%20technique%20Feynman%20pour%20l,et%20d'un%20langage%20simple.).
Et c'est exactement ce que je fais avec mes articles.
Je partage ce que j'apprends afin de mieux assimiler et comprendre les informations.


Voilà qui termine ce premier article sur "Tout ce que j'ai appris".
J'espère continuer cette série pendant une longue période et en faire une habitude dans mon apprentissage quotidien.
Ce mois-ci était rempli de nouvelles informations mais la plupart dataient déjà de plusieurs mois.
Mais il faut bien commencer quelque part !
Car un petit pas est toujours plus loin qu'aucun pas du tout.
