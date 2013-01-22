---
layout: post
title: L'échoppe de monade sur Scalaskel
lang: français
badge: top
category: post
---

Le concours de codestory bat son plein et nous avons actuellement pas loin de 115 participants actifs.
Vous pouvez suivre, en live, les résultats sur la page de [statut](http://status.code-story.net/). A noter que vous pouvez contribuer au code source de cette page (hors concours) en envoyant une pull-request sur ce [dépôt](https://github.com/dgageot/code-story-status).

Cette année, le concours consiste à monter un serveur http, de s'inscrire et d'attendre que notre robot vienne vous soumettre des questions auxquelles pour y répondre vous allez devoir coder un petit peu. Les questions sont posées de manière à ce que votre code soit écrit de manière incrémentale. Mais vous n'êtes pas obligé de suivre nos suggestions... Il est encore possible de s'[inscrire](https://docs.google.com/a/xebia.fr/spreadsheet/viewform?formkey=dDdHc3N2V2R1bHRMZHFmOGk3SWZKTmc6MQ#gid=0) cette semaine, vous pouvez tout à fait encore rattraper les autres.

Pour ceux qui ne sont pas dans la compétition, ou qui se demande bien de quoi on parle, voici l'énoncé du premier exercice que notre robot soumet aux participants :

>
> ##L’échoppe de monade sur Scalaskel.
>
> Sur la planète Scalaskel, une planète en marge de la galaxie, aux confins de l'univers, la monnaie se compte en cents, comme chez nous. 100 cents font un groDessimal. Le groDessimal est la monnaie standard utilisable partout sur toutes les planètes de l’univers connu. C'est un peu compliqué à manipuler, mais si on ne s'en sert pas y'a toujours des erreurs d'arrondis incroyables quand on les soustrais ou on les divise, c’est idiot, mais c’est comme ça.  Sur Scalaskel, on utilise rarement des groDessimaux, on utilise des pièces plus petites : Le **Foo** vaut **1 cent**, le **Bar** vaut **7 cents**, le **Qix** vaut **11 cents** et le **Baz** vaut **21 cents**.
>
> Vous tenez une échoppe de monade et autres variables méta-syntaxique sur Scalaskel. Pour faire face à l’afflux de touristes étrangers avec les poches remplies de groDessimaux vous avez besoin d’écrire un programme qui pour toute somme de 1 à 100 cents, vous donnera toutes les décompositions possibles en pièces de **Foo**, **Bar**, **Qix** ou **Baz**.
>
>Par exemple, 1 cent ne peut se décomposer qu’en une seule pièce **Foo**.
>Par contre 7 cents peuvent se décomposer soit en 7 pièces **Foo**, soit en 1 pièce **Bar**.
>
>##Serveur Web :
>
>Votre serveur doit répondre aux requetes http GET de la forme `http://serveur/scalaskel/change/X`, `X` étant une valeur en cents de 1 à 100 cents.
>
>La réponse attendue est un json de la forme :
>
	[{“foo”: w, “bar”: x, “qix”: y, “baz”: z}, …]>
>
>Exemples
>Pour `http://serveur/scalaskel/change/1` il faut répondre :
>
	[ {“foo”: 1} ]
>
>Pour `http://serveur/scalaskel/change/7` il faut répondre :
>
	[ {“foo”: 7}, {“bar”: 1} ]
>
>
>L’ordre des valeurs dans le tableau json, ainsi que le formatage n’a pas d’importance à partir du moment ou c’est du json valide, il s’entends.
>
>Bon courage !
>

Ainsi si vous avez reussi cet exercice, que vous pourriez faire sans appel http, vous avez fait une bonne partie du challenge.

Happy Clean Coding & see you at Devoxx.
