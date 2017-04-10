+++
date = "2017-04-10T06:33:00+02:00"
draft = false
title = "Presque prêt !"
+++

Après plusieurs mois de recherches, d'expérimentations, de modification de design... J'ai enfin progressé sur la nouvelle configuration de matériel devant aller dans l'observatoire.

Le principal problème était la gestion de l'alimentation électrique des différents équipements : en effet, chaque appareil était alimenté par son propre câble qui descendait jusqu'à une multiprise contrôlée par des relais, mais celle-ci étant positionnée sur le mur de l'observatoire, il y avait beaucoup de câbles _suspendus_ au télescope, augmentant le risque que ceux-ci se prennent dans la monture lors des déplacements.

Pour résoudre ce problème, l'objectif était de faire en sorte de n'avoir que deux câbles qui montent jusqu'au télescope : un d'alimentation, et un USB, le câble d'alimentation devant véhiculer trois tensions différentes : 5V pour le hub USB, 7,5V pour l'appareil photo, et 12V pour le moteur de mise au point.

Voici le schéma de cette nouvelle installation :

[<img src="/images/sothisv2_schema.png" style="width: 800px !important">](/images/sothisv2_schema.png)

Un Raspberry Pi 2, faisant tourner [Jeedom](https://www.jeedom.com/) un logiciel de domotique, contrôle via ses ports GPIO une carte 8 relais (liaison orange). Cette carte envoie les trois tensions nécessaires, fournies par une alimentation de PC (couplée à un petit transformateur réglable pour le 7,5V), au travers de la liaison rouge vers la boite de distribution qui est attachée sous le télescope. Une liaison 12V part également vers la monture.

Concernant les liaison USB (en bleu), un hub USB alimenté par la boite de distribution est fixée sur celle-ci, et permet de connecter le couvercle motorisé, la caméra de guidage, l'appareil photo et le moteur de mise au point. La monture a son propre câble USB qui la relie au PC.

Je posterai quelques photos du tout une fois installé dans l'observatoire !