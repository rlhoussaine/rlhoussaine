---
permalink: /fr/
lang: fr
title: "Academic Pages : modèle GitHub Pages prêt à l’emploi pour sites académiques personnels"
author_profile: true
---

Il s’agit de la page d’accueil d’un site propulsé par le [modèle Academic Pages](https://github.com/academicpages/academicpages.github.io) et hébergé sur GitHub Pages. [GitHub Pages](https://pages.github.com) est un service gratuit grâce auquel des sites sont générés et hébergés à partir du code et des données stockés dans un dépôt GitHub, avec mise à jour automatique à chaque nouveau commit. Ce modèle est issu du thème Jekyll [Minimal Mistakes](https://mmistakes.github.io/minimal-mistakes/) de Michael Rose, puis enrichi pour le contenu typique des chercheurs : publications, exposés, enseignement, portfolio, billets de blog et CV généré dynamiquement. Ces mêmes fonctionnalités en font aussi un excellent choix pour toute personne souhaitant présenter un site professionnel soigné !

 Vous pouvez forker [ce modèle](https://github.com/academicpages/academicpages.github.io) dès maintenant, modifier la configuration et les fichiers Markdown, ajouter vos propres PDF et contenus, et obtenir votre site gratuitement, sans publicité !

Un site personnel piloté par les données
======
Comme beaucoup de modèles Jekyll pour GitHub Pages, Academic Pages sépare le **contenu** de la **présentation**. Le contenu et les métadonnées sont dans des fichiers Markdown structurés ; le thème (autres fichiers) indique comment les transformer en pages HTML. Vous conservez ces fichiers Markdown (.md), YAML (.yml), HTML et CSS dans un dépôt GitHub public. À chaque push, le service [GitHub Pages](https://pages.github.com/) régénère les pages statiques hébergées gratuitement sur les serveurs de GitHub.

Une grande partie des possibilités des CMS (type Wordpress) est accessible ainsi, avec bien moins de ressources et une surface d’attaque réduite (piratage, DDoS). Vous pouvez adapter le thème à volonté sans toucher au contenu. Si vous cassez Jekyll, HTML ou CSS au-delà de réparation, vos Markdown (exposés, publications, etc.) restent sûrs : annulez les changages ou repartez d’un dépôt neuf en sauvegardant surtout les Markdown ! Vous pouvez aussi écrire des scripts sur les données du site, par exemple [celui-ci](https://github.com/academicpages/academicpages.github.io/blob/master/talkmap.ipynb) qui exploite les métadonnées des exposés pour afficher [une carte des lieux où vous avez présenté](https://academicpages.github.io/talkmap.html).

Pour les besoins plus avancés, le modèle prend en charge notamment :
- [MathJax](https://www.mathjax.org/) pour les formules mathématiques
- [Mermaid](https://mermaid.js.org/) pour les diagrammes
- [Plotly](https://plotly.com/javascript/) pour les graphiques interactifs

Pour commencer
======
1. Créez un compte GitHub si besoin et validez votre e-mail (obligatoire !)
1. Forkez [ce modèle](https://github.com/academicpages/academicpages.github.io) via le bouton « Use this template » en haut à droite.
1. Ouvrez les paramètres du dépôt (onglet à droite de « Code », sous « Unwatch »). Renommez-le en `[votre-identifiant-github].github.io`, ce qui sera aussi l’URL du site.
1. Configurez le site et créez contenu & métadonnées (voir ci-dessous — et [cet ensemble de diffs](https://archive.is/3TPas) montrant les fichiers modifiés pour [un site d’exemple](https://getorg-testacct.github.io) pour l’utilisateur « getorg-testacct »).
1. Déposez vos fichiers (PDF, archives, etc.) dans le dossier `files/`. Ils seront accessibles à l’adresse https://[votre-identifiant].github.io/files/exemple.pdf.
1. Vérifiez l’état dans les paramètres du dépôt, section « GitHub pages ».

Configuration globale du site
------
Le fichier principal de configuration est à la racine : [_config.yml](https://github.com/academicpages/academicpages.github.io/blob/master/_config.yml) (barres latérales et éléments communs). Remplacez les valeurs par défaut par vos informations et l’URL de votre dépôt. Le menu du haut est défini dans [_data/navigation.yml](https://github.com/academicpages/academicpages.github.io/blob/master/_data/navigation.yml). Par exemple, sans portfolio ni blog, retirez les entrées correspondantes de `navigation.yml` pour les masquer dans l’en-tête.

Créer le contenu et les métadonnées
------
Chaque type de contenu correspond à des fichiers Markdown dans `_publications`, `_talks`, `_posts`, `_teaching`, `_pages`, etc. Chaque exposé est par exemple un fichier dans le [dossier _talks](https://github.com/academicpages/academicpages.github.io/tree/master/_talks), avec un en-tête YAML que le thème interprète pour alimenter la [page Exposés](https://academicpages.github.io/talks), les [pages individuelles](https://academicpages.github.io/talks/2012-03-01-talk-1), la section exposés du [CV](https://academicpages.github.io/cv) et la [carte des lieux d’exposés](https://academicpages.github.io/talkmap.html) (si vous exécutez le [script Python](https://github.com/academicpages/academicpages.github.io/blob/master/talkmap.py) ou le [notebook Jupyter](https://github.com/academicpages/academicpages.github.io/blob/master/talkmap.ipynb) qui génère la carte à partir de `_talks`).

**Générateur Markdown**

Le dépôt contient [des notebooks Jupyter](https://github.com/academicpages/academicpages.github.io/tree/master/markdown_generator) qui convertissent un CSV d’exposés ou de présentations en fichiers Markdown au format Academic Pages. Les CSV d’exemple sont ceux utilisés pour le site personnel stuartgeiger.com. Le flux habituel : tableur des publications et exposés → notebooks → fichiers Markdown → commit et push sur GitHub.

Modifier le dépôt du site sur GitHub
------
Beaucoup utilisent un client git en local puis poussent vers GitHub. Sans git, vous pouvez éditer les fichiers sur github.com : ouvrez un fichier (par exemple [celui-ci](https://github.com/academicpages/academicpages.github.io/blob/master/_talks/2012-03-01-talk-1.md)) et cliquez sur l’icône crayon à droite de l’aperçu. Suppression via l’icône corbeille ; nouveaux fichiers ou upload depuis le dossier voulu avec « Create new file » ou « Upload files ».

Exemple : édition d’un Markdown d’exposé
![Édition d’un fichier Markdown pour un exposé](/images/editing-talk.png)

Pour aller plus loin
------
Pour configurer Academic Pages, voir [le guide](https://academicpages.github.io/markdown/), le [wiki](https://github.com/academicpages/academicpages.github.io/wiki), ou [poser une question sur GitHub](https://github.com/academicpages/academicpages.github.io/discussions). Les [guides du thème Minimal Mistakes](https://mmistakes.github.io/minimal-mistakes/docs/configuration/) (dont ce thème est issu) peuvent aussi aider.
