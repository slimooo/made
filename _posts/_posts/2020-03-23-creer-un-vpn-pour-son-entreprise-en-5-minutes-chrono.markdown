---
layout: post
title: Comment créer un VPN pour son entreprise en 5 minutes chrono ?
date: '2020-03-23 14:40:47'
tags:
- cybersecurite
---

Un VPN est un outil très pratique pour sécuriser la connexion de vos salariés notamment lorsqu'ils sont en télétravail. N'hésitez pas à lire notre article "[À quoi sert un VPN ?]( __GHOST_URL__ /blog/a-quoi-sert-un-vpn/)" pour en savoir plus.

Vous pouvez installer votre VPN sur un serveur local, un serveur distant ou même un VPS. Dans ce tutoriel on part du postulat que **votre serveur est déjà disponible** et qu'il ne reste qu'à installer votre application VPN.

Nous allons utiliser la **solution libre** Get Outline qui va vous permettre de lancer votre VPN sans prise de tête.

<figure class="kg-card kg-bookmark-card"><a class="kg-bookmark-container" href="https://getoutline.org/"><div class="kg-bookmark-content">
<div class="kg-bookmark-title">Outline VPN - Access to the free and open internet</div>
<div class="kg-bookmark-description">Outline is a VPN software that makes it easy for anyone to create, run, and share access to their own VPN.</div>
<div class="kg-bookmark-metadata">
<img class="kg-bookmark-icon" src="https://getoutline.org/static/img/outline-favicon.png?cache=60b304a" alt=""><span class="kg-bookmark-author">Outline</span>
</div>
</div>
<div class="kg-bookmark-thumbnail"><img src="https://getoutline.org/static/img/outline-logo.svg" alt=""></div></a></figure>
## Installation du VPN

Depuis votre terminal, il faut traditionnellement mettre à jour vos dépôts :

<!--kg-card-begin: markdown-->

`apt-get update`  
`apt-get upgrade`

<!--kg-card-end: markdown-->

Puis c'est parti pour l'installation, pour cela il suffit de taper cette ligne de commande :

<!--kg-card-begin: markdown-->

`sudo bash -c "$(wget -qO- https://raw.githubusercontent.com/Jigsaw-Code/outline-server/master/src/server_manager/install_scripts/install_server.sh)"`

<!--kg-card-end: markdown-->

Si Docker n'est pas installé, on vous demandera si vous souhaitez l'installer. Il suffira de taper " **y**" pour yes et valider.

**C'est fini!** Votre serveur VPN est prêt. Un message de confirmation s'affiche vous communiquant votre clé de connexion. La clé commence par : {"apiUrl". Copiez cette clé et **sauvegardez-la en sécurité**.

## Installation de l'outil de gestion du VPN

Une fois le serveur VPN installé, vous devrez télécharger l'outil de gestion de votre serveur. Cet outil vous permettra de créer les comptes de vos salariés et gérer le quota de données utilisé.

Pour télécharger cet outil : [Windows](https://raw.githubusercontent.com/Jigsaw-Code/outline-releases/master/manager/stable/Outline-Manager.exe) / [Mac](https://raw.githubusercontent.com/Jigsaw-Code/outline-releases/master/manager/stable/Outline-Manager.dmg) / [Linux](https://raw.githubusercontent.com/Jigsaw-Code/outline-releases/master/manager/stable/Outline-Manager.AppImage)

Une fois téléchargé et installé. Un écran vous propose quatre possibilités en fonction de votre configuration. Par défaut, choisissez la quatrième option " **Installer Outline sur n'importe quel serveur cloud**".  
  
Dans le champ numéro 2 " **Collez le résultat de l'installation ici**", il suffit de coller la clé qu'on aura précédemment sauvegardée puis de cliquer sur **OK**.

## Création des clés d'accès

L'outil de gestion va vous permettre de créer les clés d'accès pour chaque utilisateur. C'est **avec ces clés que vos salariés pourront se connecter à votre serveur VPN**. Rien de plus simple, il suffit de cliquer sur " **Ajouter une clé**", et lui attribuer un nom en fonction du salarié.

Le bouton de partage générera alors un **message d'invitation comprenant la clé d'accès**.

## Connexion au serveur VPN

Pour se connecter au serveur VPN, le salarié devra télécharger un client sur son appareil. Le client est disponible sur [Android](https://play.google.com/store/apps/details?id=org.outline.android.client) / [Windows](https://raw.githubusercontent.com/Jigsaw-Code/outline-releases/master/client/stable/Outline-Client.exe) / [iOS](https://apps.apple.com/us/app/outline-app/id1356177741) / [Mac](https://apps.apple.com/us/app/outline-app/id1356178125) / [Linux](https://raw.githubusercontent.com/Jigsaw-Code/outline-releases/master/client/stable/Outline-Client.AppImage).

Et suivre les quelques étapes à partir du message d'invitation qui vous lui avez envoyé.

