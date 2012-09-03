---
layout: post
title: GildedRose WebStyle
lang: français
badge: binary
---

Le second tour de codestory qui a eu lieu le 1er février dernier a été une soirée haute en couleurs.
David et moi même avons accueillis 14 binômes particulièrement motivés. 
6 personnes venant de Suisse, 4 du Luxembourg et 18 de France (essentiellement de région Parisienne).

Nous avions préparé pour nous les organisateurs une paire de tshirt CodeStory histoire de mettre tout le monde dans l'ambiance.
Mais plusieurs binômes avaient, eux aussi, préparé des tshirts assez élaborés. Bravo encore à vous pour votre préparation.

![tshirt1](/images/tshirt2.jpeg)

Chaque binôme a amené son propre matériel, Xebia fournissant boissons, nourriture et wifi.

Après les encouragements de notre guest star du soir, à savoir Nicolas Martignole, auteur du blog le Touilleur Express et organisateur de la conférence Devoxx France, pendant laquelle CodeStory va se dérouler.

L'exercice
===========

L'exercice de la soirée consistait à hériter d'un bout de code particulièrement atroce, d'ajouter une nouvelle fonction dans celui-ci puis de présenter le tout dans une webapp. Le tout en 2 heures, compréhension de l'exercice compris !

L'exercice en question est un dérivé du kata de refactoring nommé GildedRose dont voici l'énoncé :

Gilded Rose Kata
-------------

Hi and welcome to team Gilded Rose. As you know, we are a small inn with a prime location in a prominent city ran by a friendly innkeeper named Allison. We also buy and sell only the finest goods. Unfortunately, our goods are constantly degrading in quality as they approach their sell by date. We have a system in place that updates our inventory for us. It was developed by a no-nonsense type named Leeroy, who has moved on to new adventures.

Your tasks
-------------

Your tasks are to :

* Add the new feature to our system so that we can begin selling a new category of items.
* Present the system as a web application so that we can take orders worldwide.

First an introduction to our system:

* All items have a SellIn value which denotes the number of days we have to sell the item
* All items have a Quality value which denotes how valuable the item is
* At the end of each day our system lowers both values for every item

Pretty simple, right? Well this is where it gets interesting:

* Once the sell by date has passed, Quality degrades twice as fast
* The Quality of an item is never negative
* “Aged Brie” actually increases in Quality the older it gets
* The Quality of an item is never more than 50
* “Sulfuras”, being a legendary item, never has to be sold or decreases in Quality
* “Backstage passes”, like aged brie, increases in Quality as it’s SellIn value approaches; Quality increases by 2 when there are 10 days or less and by 3 when there are 5 days or less but Quality drops to 0 after the concert

New feature
-------------
We have recently signed a supplier of conjured items. This requires an update to our system:

* “Conjured” items degrade in Quality twice as fast as normal items


L'exercice est "livré" avec la classe [Inn](https://github.com/dgageot/CodeStoryStep2/blob/master/src/main/java/fr/xebia/katas/gildedrose/Inn.java) (qui a elle seule vaut le détour) et [Item](https://github.com/dgageot/CodeStoryStep2/blob/master/src/main/java/fr/xebia/katas/gildedrose/Item.java).
Vous trouverez l'ensemble de l'exercice dans le dépot [github de codestory](https://github.com/dgageot/CodeStoryStep2)

Déroulé
=========
Sur un exercice de ce style, et vu le code absolument abominable que l'on récupère, ajouter du comportement dans le code sans un minimum de tests est un allez simple pour un crash en beauté. La plupart des binômes l'ont compris assez vite en commençant à tisser un harnais de tests.<br/>
Le harnais de tests permet, dans cet exercice, de mieux comprendre le fonctionnement du système et de rentrer dans l'exercice progressivement sans forcément tout avoir à comprendre d'un coup.<br/>
Une fois ce harnais de tests plus ou moins constitué, vient la phase de refactoring de la méthode **updateQuality** de la classe **Inn**, afin de simplifier un peu ces imbrications impossibles de if.<br/>
Certains binômes ont cherché à pousser très loin le refactoring, qui n'a rien d'un refactoring facile. D'autres on simplement profité du harnais de tests pour ajouter la nouvelle fonctionnalité en toute confiance.

![tshirt2](/images/tshirt1.jpeg)

L'exercice étant limité à 2 heures, certains ont du se résoudre soit à finir le refactoring pour présenter le code le plus propre possible, soit à démarrer la webapp. Certains ont choisi la première voie, d'autre la seconde. Parfois dans les dernières 10 minutes, non sans un certain stress...


A la fin du temps imparti nous avions 6 binômes ayant partiellement refactoré la méthode **UpdateQuality** (pour certain c'était vraiment super léger...), ajouté un harnais de tests sur la classe **Inn** et présenté le tout dans une WebApp.


Nous avons eu droit, a une servlet, du SpringMVC, du Simple et même du Play!, le tout parfois agrémenté de css maison voir de Twitter BootStrap pour les plus webaware d'entre eux.

Conclusion
=========
Nous avons sélectionné 5 binômes en partant du principe que ce que nous voulions c'est l'ensemble des fonctionnalités. A savoir une webapp avec des objets "conjured" fonctionnelle et le code le plus propre possible. Dans cet ordre.


Vous trouverez la solution [propre](https://github.com/dgageot/CodeStoryStep2/tree/David) et moins [propre](https://gist.github.com/1782268) de David et de [Jean-Laurent](https://github.com/jeanlaurent/CodeStoryStep2) si vous voulez voir à quoi nous sommes arrivé, dans sensiblement les mêmes conditions que les binômes.


Rendez-vous le 14 février [au Paris JUG](http://www.parisjug.org/xwiki/bin/view/Meeting/20120214) pour l'élection du top binôme qui partira faire des étincelles à Devoxx.

Un autre résumé avec de belles photos est disponible sur le [site web de Nicolas](http://www.touilleur-express.fr/2012/02/04/code-story-demie-finale-chez-xebia/).