---
layout: post
title: Sélection FooBarQix
---

Le 16 décembre dernier était la date de fin de soumission pour la sélection pour participer à CodeStory, le live coding que nous organisons dans le cadre de [Devoxx France](http://devoxx.com/display/FR12) du 18 au 20 avril 2012.
Cette pré-sélection consistait à nous fournir un bout de code répondant à des critère précis ainsi que de trouver un binôme pour coder avec nous.

Quelques statistiques
=========================

La participation a été largement au delà de nos espérances, nous sommes en train de dépiler les 55 différentes soumissions de code de la part de 45 personnes différentes (sans compter les binômes). Et le moins que l'on puisse dire, c'est qu'il y a de la variété ! Ces soumissions ont été écrites à l'aide de 11 langages différents : Java, Scala, Ruby, Groovy, Javascript, Clojure, Haskell, Fantom, Jython, Ioke, Yeti. (Si si, [ça](http://mth.github.com/yeti/) existe...) On y trouve de tout, des one-liner, du test first, du test after, des builders, de l'instrospection, du play, du guava, du maven, du clean-code et du moins clean-code, bref un grand éclectisme. Certains ont soumis jusqu'à 4 solutions differentes.

Une majorité de Java et pas mal de scala, la participation des autres langages est plus diluée, mais bien présente (1/4). Autant la contrainte de FooBarQix ne demandait que de pouvoir s'exécuter sur une JVM autant pour le live coding à Devoxx, nous utiliserons Java (7 avec des bouts de 8 dedans en fonction de ce qui sera disponible dans quelques mois). Le live coding en lui même étant déjà assez contraignant pour que nous nous limitions à des langages que nous maitrisons bien. Le but ultime de ce live coding est de fournir une application utilisable à la fin de Devoxx, tout en étant distrayant, instructif & fun.

<script type="text/javascript" src="//ajax.googleapis.com/ajax/static/modules/gviz/1.0/chart.js"> {"dataSourceUrl":"//docs.google.com/a/morlhon.net/spreadsheet/tq?key=0Alr12p0nBBordEhMdnFiaVN6YWZZTVR6ZXFfUjhRUGc&transpose=0&headers=0&range=A5%3AB7&gid=1&pub=1","options":{"vAxes":[{"viewWindowMode":"pretty","viewWindow":{}},{"viewWindowMode":"pretty","viewWindow":{}}],"title":"Langages","backgroundColor":"#FFFFFF","legend":"right","colors":["#38761d","#f1c232","#cc0000","#3d85c6","#990099","#0099C6","#DD4477","#66AA00","#B82E2E","#316395","#994499","#22AA99","#AAAA11","#6633CC","#E67300","#8B0707","#651067","#329262","#5574A6","#3B3EAC","#B77322","#16D620","#B91383","#F4359E","#9C5935","#A9C413","#2A778D","#668D1C","#BEA413","#0C5922","#743411"],"is3D":true,"hasLabelsColumn":true,"hAxis":{"maxAlternations":1},"width":565,"height":376},"state":{},"view":"{\"columns\":[0,1]}","chartType":"PieChart","chartName":"Graphique 1"} </script>


La genèse
=========================

Lorsque nous avons publié l'énoncé lors de Devoxx 2011, nous avons été assaillis de questions, et comme nous nous étions inspiré d'un [kata existant](https://github.com/jeanlaurent/fizzbuzz-kata) en le transformant un peu... Du coup nous n'avions pas pu répondre à toutes les questions sur l'instant. Nous avons donc codé un laptop sur les genoux pendant la soporifique keynote d'Oracle une [solution](https://github.com/jeanlaurent/FooBarQix) pour pouvoir répondre à toutes les questions.

Les prochaines étapes
=========================

Nous allons contacter tous les participants dans les jours à venir pour leur indiquer le statut de leur soumission, le temps qu'on dépile ce tas de code. Nous allons aussi proposer un système pour ceux qui seront sélectionnés sans binôme afin qu'ils en trouve un. 

L'étape suivante sera de se retrouver tous ensemble une soirée afin de coder et de s'apprécier d'un point de vue technique et humain. David et moi même sélectionneront à ce moment là quelques binômes pour un battle final qui aura lieu début mars.

Dans les semaines à venir, nous publierons ce que nous avons aimé et ce que nous avons moins aimé dans le code qui nous a été soumis, avec l'accord des auteurs, bien sur.

Merci à vous tous, d'avoir participer avec une telle ferveur.

Stay tuned pour la suite !

{% include sig.md %}
