---
layout: post
title: Location d’astronef sur Jajascript
lang: français
badge: fatty
category: post
---

Maintenant que le concours est terminé, nous vous livrons le second exercice auxquel nous avons soumis nos candidats. C'est sur cet exercice en particulier que nous avons augmenté la complexité par petit pas.

Cet exercice est plus complexe que le précédent, notamment lorsque vous devez traiter des niveaux importants de flux d'astronefs. Nous avons soumis nos candidats à effectuer une réponse de traitement de calcul en moins de 30 secondes.

1. Essayez de résoudre l'exercice, avec le cas de test inclus qui contient 4 trajets.
2. Essayez avec le ce fichier de [50 trajets](http://code-story.net/data/jajascript-50.zip)
3. Puis sur celui-ci de [50000 trajets](http://code-story.net/data/jajascript-10k.zip). (attention 4mo de json, que nous vous avons zippé par respect de bande passante).
4. Amusez vous avec notre [générateur de payload](https://github.com/CodeStory/jajascript-generator), a tenter des chiffres encore plus grand.

Notez que dans le cas du concours, il convient de répondre en 30 secondes, temps de transport de l'information compris, c'est à dire du payload json final. Vous aurez du mal à reproduire cette contrainte sans un client/serveur distant l'un de l'autre. Mais cela vous donne une idée des difficultés que les joueurs ont rencontrés pour finir cet exercice. Une réponse en moins de 30 secondes du fichier de 50000 trajets lié plus haut, permettait d'obtenir les 10000 points nécessaire pour être en tête.

Sans plus attendre voici l'énoncé que nous avons envoyé il y a 15 jours à nos candidats :

> ## Location d'astronef sur Jajascript

> Votre cousin par alliance, Martin O. sur la planète Jajascript vient de monter sa petite entreprise de vol spatial privée: Jajascript Flight Rental. Il loue aux grosses corporations son astronef lorsqu'elles ont de fortes charges ou un pépin avec leurs propres appareils. Il s'occupe de la maintenance et de l'entretien de son petit astronef. Il ne pouvait s'en payer qu'un pour démarrer.
> 
> Ces grosses corporations envoient des commandes de location qui consistent en un intervalle de temps, et le prix qu'ils sont prêts à payer pour louer l'astronef durant cet intervalle.
> 
> Les commandes de tous les clients sont connues plusieurs jours à l'avance. Ce qui permet de faire un planning pour une journée.
> Les commandes viennent de plusieurs sociétés différentes et parfois elles se chevauchent. On ne peut donc pas toutes les honorer.
> 
> Idéalement, il faut donc être capable de prendre les plus rentables, histoire de maximiser les gains de sa petite entreprise, et de s'acheter d'autres astronefs.
> Votre cousin passe des heures à trouver le planning idéal et vous demande **pour un planning donné de calculer une solution qui maximise son gain**.
> 
> ### Exemple
> 
> Considérez par exemple le cas où la JajaScript Flight Rental a 4 commandes :
> 

    MONAD42 : heure de départ 0, durée 5, prix 10
    META18 : heure de départ 3, durée 7, prix 14
    LEGACY01 : heure de départ 5, durée 9, prix 8
    YAGNI17 : heure de départ 5, durée 9, prix 7

> 
> La solution optimale consiste à accepter MONAD42 et LEGACY01, et le revenu est de `10 + 8 = 18`. Remarquez qu'une solution à partir de MONAD42 et YAGNI17 est faisable (l'avion serait loué sans interruption de 0 à 14) mais non optimale car le bénéfice serait que de 17.
> 
> ### Précisions
> 
> L'identifiant d'un vol ne dépasse jamais 50 caractères, les heures de départs, durée et prix sont des entiers positifs raisonnablement grands.
> 
> ### Serveur
> 
> Votre serveur doit répondre aux requêtes http POST de la forme `http://serveur/jajascript/optimize` avec un payload de la forme :
> 
{% highlight json %}
  [
    { "VOL": "NOM_VOL", "DEPART": HEURE, "DUREE": DUREE, "PRIX": PRIX }, ...
  ]
{% endhighlight %}
>
>En reprenant l'exemple ci dessus :
>
{% highlight json %}
  [
    { "VOL": "MONAD42", "DEPART": 0, "DUREE": 5, "PRIX": 10 },
    { "VOL": "META18", "DEPART": 3, "DUREE": 7, "PRIX": 14 },
    { "VOL": "LEGACY01", "DEPART": 5, "DUREE": 9, "PRIX": 8 },
    { "VOL": "YAGNI17", "DEPART": 5, "DUREE": 9, "PRIX": 7 }
  ]
{% endhighlight %}
>
>Vous devrez répondre le résultat suivant :
>
{% highlight json %}
    {
      "gain" : 18,
      "path" : ["MONAD42","LEGACY01"]
    }
{% endhighlight %}
>
>Le gain représentant la somme optimale, path représentant l'ordre des vols.
>
>Bons calculs !