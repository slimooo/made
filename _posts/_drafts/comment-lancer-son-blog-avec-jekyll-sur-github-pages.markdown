---
layout: post
title: Comment lancer son blog avec Jekyll sur GitHub Pages ?
tags:
- blog
---

Dans cet article, je vais vous montrer comment créer un blog simple, rapide et personnalisable avec [Jekyll](https://jekyllrb.com/) et [GitHub Pages](https://pages.github.com/). Jekyll est un générateur de sites statiques, c'est-à-dire qu'il transforme des fichiers texte en fichiers HTML. GitHub Pages est un service d'hébergement gratuit de pages web, qui utilise Jekyll en arrière-plan pour générer et publier votre site.

Avec cette combinaison, vous n'aurez besoin que d'un compte GitHub et d'un éditeur de texte. Vous pourrez écrire vos articles en Markdown, un langage de balisage facile à apprendre et à utiliser. Vous pourrez également choisir parmi de nombreux thèmes disponibles pour personnaliser l'apparence de votre blog. Et vous bénéficierez de la sécurité, de la performance et de la fiabilité de GitHub.

Prêt à vous lancer ? Alors suivez les étapes ci-dessous !

## Prérequis

Avant de commencer, vous devez avoir :

- Un compte GitHub : si vous n'en avez pas encore, vous pouvez en créer un gratuitement sur [github.com](https://github.com/).
- Un éditeur de texte : vous pouvez utiliser celui que vous voulez, mais je vous recommande [Visual Studio Code](https://code.visualstudio.com/), qui est gratuit, puissant et facile à utiliser.

## Choix du thème

La première étape consiste à choisir un thème pour votre blog. Un thème est un ensemble de fichiers qui définissent l'apparence et le fonctionnement de votre site. Il existe de nombreux thèmes pour Jekyll, que vous pouvez trouver sur [GitHub](https://github.com/topics/jekyll-theme) ou sur [Jekyll Themes](https://jekyllthemes.io/).

Pour ce tutoriel, nous allons utiliser le thème [Minimal Mistakes](https://github.com/mmistakes/minimal-mistakes), qui est un thème flexible, responsive et riche en fonctionnalités. Vous pouvez voir une démo du thème sur [ce site](https://mmistakes.github.io/minimal-mistakes/).

Pour utiliser ce thème, vous devez le copier (forker) sur votre compte GitHub. Pour cela, suivez ces instructions :

- Connectez-vous à votre compte GitHub et rendez-vous sur la page du thème : [https://github.com/mmistakes/minimal-mistakes](https://github.com/mmistakes/minimal-mistakes).
- Cliquez sur le bouton "Fork" en haut à droite.
- Choisissez votre compte comme destination du fork.
- Attendez que le fork soit terminé.

Voilà, vous avez copié le thème sur votre compte GitHub ! Il se trouve maintenant dans un dépôt nommé minimal-mistakes.

## Configuration du dépôt

La deuxième étape consiste à configurer le dépôt qui contient le thème pour qu'il devienne votre blog. Pour cela, vous devez modifier le nom du dépôt, les paramètres du site et les fichiers du thème.

Suivez ces instructions :

- Rendez-vous sur la page du dépôt minimal-mistakes sur votre compte GitHub.
- Cliquez sur le bouton "Settings" en haut à droite.
- Dans la section "Repository name", changez le nom du dépôt en "Blog" ou autre nom que vous souhaitez.
- Cliquez sur le bouton "Rename".
- Dans la section "GitHub Pages", choisissez la branche master comme source et cliquez sur le bouton "Save".
- Notez l'URL de votre site qui s'affiche sous la forme https://utilisateur.github.io. Par exemple, si votre nom d'utilisateur est gaia, l'URL de votre site est https://gaia.github.io/blog/.

Voilà, vous avez configuré le dépôt qui contiendra votre blog ! Il est accessible à l'URL que vous avez notée. Il se peut qu'il faille attendre quelques minutes avant que le site soit généré et publié par GitHub.

## Modification des paramètres du site

La troisième étape consiste à modifier les paramètres du site pour le personnaliser. Les paramètres du site sont définis dans le fichier \_config.yml, qui se trouve à la racine du dépôt. Ce fichier contient des informations telles que le titre du site, la description, l'URL, le langage, le thème, les plugins, les menus, les réseaux sociaux, etc.

Pour modifier les paramètres du site, vous devez éditer le fichier \_config.yml sur GitHub. Pour cela, suivez ces instructions :

Rendez-vous sur la page du dépôt sur votre compte GitHub.

Cliquez sur le fichier \_config.yml pour l'ouvrir.

Cliquez sur l'icône en forme de crayon en haut à droite pour passer en mode édition.

Modifiez les paramètres selon vos préférences. Vous pouvez consulter la [documentation du thème](https://mmistakes.github.io/minimal-mistakes/docs/configuration/) pour connaître les options disponibles et leurs valeurs possibles. Voici quelques exemples de paramètres que vous pouvez modifier :

`title` : le titre de votre site. Par exemple : `title: Mon super blog`.

`description` : la description de votre site. Par exemple : `description: Un blog où je partage mes passions et mes découvertes`.

`url` : l'URL de votre site. Par exemple : `url: https://gaia.github.io/blog/`.

`locale` : le code du langage de votre site. Par exemple : `locale: fr-FR`.

`author` : les informations sur l'auteur du site. Par exemple :

    author:
      name: Gaïa
      bio: "Je suis une développeuse web passionnée par les nouvelles technologies."
      avatar: "/assets/images/avatar.jpg"
      links:
        - label: "Email"
          icon: "fas fa-fw fa-envelope-square"
          url: "mailto:gaia@example.com"
        - label: "Twitter"
          icon: "fab fa-fw fa-twitter-square"
          url: "https://twitter.com/gaia"
        - label: "GitHub"
          icon: "fab fa-fw fa-github-square"
          url: "https://github.com/gaia"

`theme` : le nom du thème utilisé. Par défaut, il s'agit de `minimal-mistakes-jekyll`. Vous pouvez le changer si vous voulez utiliser un autre thème compatible avec GitHub Pages.

`plugins` : la liste des plugins utilisés par le site. Par défaut, il s'agit de :

    plugins:
      - jekyll-paginate
      - jekyll-sitemap
      - jekyll-gist
      - jekyll-feed
      - jemoji

Vous pouvez ajouter ou supprimer des plugins selon vos besoins. Vous pouvez consulter la [liste des plugins compatibles avec GitHub Pages](https://pages.github.com/versions/) pour connaître les options disponibles.

`navigation` : les menus de navigation du site. Par défaut, il y a deux menus : un menu principal (`main`) et un menu des réseaux sociaux (`social`). Vous pouvez modifier les éléments de ces menus ou ajouter d'autres menus selon vos besoins. Par exemple :

    navigation:
      main:
        - title: "Accueil"
          url: /
        - title: "À propos"
          url: /about/
        - title: "Contact"
          url: /contact/
      social:
        - title: "Twitter"
          url: https://twitter.com/gaia
        - title: "GitHub"
          url: https://github.com/gaia
        - title: "Email"
          url: mailto:gaia@example.com

Une fois que vous avez terminé de modifier les paramètres du site, cliquez sur le bouton "Commit changes" en bas de la page pour enregistrer vos modifications.

Voilà, vous avez modifié les paramètres du site ! Il se peut qu'il faille attendre quelques minutes avant que les changements soient visibles sur votre site.

## Modification des fichiers du thème

La quatrième étape consiste à modifier les fichiers du thème pour personnaliser davantage votre blog. Les fichiers du thème sont les fichiers qui définissent la structure, le style et le comportement de votre site. Ils se trouvent dans les dossiers \_layouts, \_includes, \_sass et assets.

Pour modifier les fichiers du thème, vous devez les éditer sur GitHub. Pour cela, suivez ces instructions :

Rendez-vous sur la page du dépôt sur votre compte GitHub.

Cliquez sur le dossier ou le fichier que vous voulez modifier pour l'ouvrir.

Cliquez sur l'icône en forme de crayon en haut à droite pour passer en mode édition.

Modifiez le contenu du fichier selon vos préférences. Vous pouvez consulter la [documentation du thème](https://mmistakes.github.io/minimal-mistakes/docs/quick-start-guide/) pour connaître les options disponibles et leurs valeurs possibles. Voici quelques exemples de fichiers que vous pouvez modifier :

- `_layouts/home.html` : le modèle de la page d'accueil du site. Vous pouvez changer le type de pagination, le nombre d'articles par page, l'affichage des images, des extraits, des catégories, des tags, etc.
- `_layouts/single.html` : le modèle des pages individuelles du site. Vous pouvez changer l'affichage du titre, de la date, de l'auteur, des commentaires, des liens de partage, des articles relatifs, etc.
- `_includes/head.html` : le fichier qui contient les éléments du head de chaque page du site. Vous pouvez ajouter ou supprimer des métadonnées, des liens vers des feuilles de style ou des scripts externes, etc.
- `_includes/footer.html` : le fichier qui contient les éléments du footer de chaque page du site. Vous pouvez ajouter ou supprimer des liens vers des pages ou des réseaux sociaux, des mentions légales, etc.
- `_sass/minimal-mistakes/_variables.scss` : le fichier qui contient les variables de style du thème. Vous pouvez changer les couleurs, les polices, les tailles, les espacements, les bordures, les ombres, les transitions, etc.
- `assets/css/main.scss` : le fichier qui importe les feuilles de style du thème. Vous pouvez ajouter ou supprimer des feuilles de style selon vos besoins. Vous pouvez également créer vos propres feuilles de style dans le dossier assets/css et les importer dans ce fichier.

Une fois que vous avez terminé de modifier les fichiers du thème, cliquez sur le bouton "Commit changes" en bas de la page pour enregistrer vos modifications.

Voilà, vous avez modifié les fichiers du thème ! Il se peut qu'il faille attendre quelques minutes avant que les changements soient visibles sur votre site.

## Écriture des articles

La cinquième et dernière étape consiste à écrire les articles de votre blog. Les articles sont des fichiers au format Markdown qui se trouvent dans le dossier \_posts. Chaque article doit avoir un nom sous la forme AAAA-MM-JJ-titre.md, où AAAA-MM-JJ est la date de publication et titre est le titre de l'article.

Pour écrire un article, vous devez créer un nouveau fichier Markdown dans le dossier \_posts sur GitHub. Pour cela, suivez ces instructions :

- Rendez-vous sur la page du dépôt d'utilisateur.github.io sur votre compte GitHub.
- Cliquez sur le dossier \_posts pour l'ouvrir.
- Cliquez sur le bouton "Add file" en haut à droite et choisissez "Create new file".
- Donnez un nom à votre fichier sous la forme AAAA-MM-JJ-titre.md. Par exemple : 2023-03-27-mon-premier-article.md.
- Écrivez le contenu de votre article en utilisant la syntaxe Markdown. Vous pouvez consulter la [documentation de Markdown](https://daringfireball.net/projects/markdown/syntax) pour connaître les règles de formatage.

Au début de votre fichier, vous devez ajouter des métadonnées appelées “front matter”. Il s’agit d’un bloc de texte délimité par trois tirets (---) qui contient des informations sur votre article, telles que le titre, la date, les catégories, les tags, etc. Vous pouvez consulter la documentation du thème pour connaître les options disponibles et leurs valeurs possibles. Voici un exemple de front matter :

    ---
    title: Mon premier article
    date: 2023-03-27
    categories:
      - Blog
    tags:
      - Jekyll
      - GitHub Pages
    ---

Une fois que vous avez terminé d’écrire votre article, cliquez sur le bouton “Commit new file” en bas de la page pour enregistrer votre fichier.

Voilà, vous avez écrit votre premier article ! Il se peut qu’il faille attendre quelques minutes avant que l’article soit visible sur votre site.

Félicitations ! Vous avez réussi à créer votre blog avec Jekyll et GitHub Pages ! Vous pouvez maintenant ajouter d’autres articles, modifier le thème ou ajouter des fonctionnalités à votre site selon vos envies.

Si vous voulez approfondir vos connaissances sur Jekyll et GitHub Pages, vous pouvez vous inscrire à notre formation en visioconférence intitulée “Publier son blog avec Jekyll”. Cette formation vous permettra de :

- Apprendre les bases de Jekyll et de GitHub Pages.
- Créer et personnaliser votre blog avec Jekyll et GitHub Pages.
- Ajouter des fonctionnalités à votre blog, comme des commentaires, un formulaire de contact, une newsletter, etc.
- Optimiser votre blog pour le référencement et la performance.
