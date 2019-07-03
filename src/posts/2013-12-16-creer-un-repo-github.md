---
title: Créer un Dépôt sur GitHub
date: 2013-12-16 11:19:00 +01:00
tags:
- github
- git
- repo
- remote
- howto
- tutoriel
subtitle: Pour poser un projet sur GitHub, il faut créer un repository. Créons-le
  !
author: christophe ducamp
slug: creer-un-repo-github
---

Lien de référence : <span class="h-cite"><cite class="p-name u-url">[Create A Repo](https://help.github.com/articles/create-a-repo)</cite></span>

Vous pouvez stocker une variété de projets dans des référentiels GitHub, y compris des projets open source. Avec les projets open source, vous pouvez partager du code pour créer un logiciel plus fiable et de meilleure qualité.

## Produire un nouveau dépôt sur GitHub

Chaque fois que vous produisez un *commit* (instantané) avec Git, il est stocké dans un dépôt (aussi appelé "repo"). Pour déposer votre projet sur GitHub, vous devrez disposer d'un dépôt GitHub pour le faire vivre.

*Plus sur les dépôts* : Git stocke tous vos fichiers projets dans un dépôt. Si vous pouvez voir les fichiers cachés sur votre système, vous verrez un sous-répertoire appelé ".git" dans le répertoire du projet où vous avez lancé `git init`. C'est l'endroit où Git stocke tous vos commits avec tout ce dont il a besoin. En plus de votre répertoire local, vous pouvez avoir aussi des dépôts distants (comme les dépôts sur GitHub). Les dépôts distants sont les mêmes que votre dépôt local, mais ils sont juste stockés sur un serveur ou un ordinateur distant pour faciliter la collaboration, les sauvegardes et d'autres trucs géniaux.

### 1. Dans le coin en haut et à droite, cliquez sur [+](https://github.com/repositories/new).

![image](/images/repo-create.png "cliquez sur New Repository")

### 2. Tapez un nom court, mémorisable pour votre repo, par exemple "Hello-world" : 

![image](/images/create-repository-name.png "nom de votre repo")

Félicitations ! Vous avez créé avec brio votre premier "repo" (référentiel en français.) !

### 3. Facultatif : ajoutez une description de votre repo. Par exemple "Mon premier référentiel sur GitHub"

![](/images/create-repository-desc.png "Description de votre repo sur GitHub")

### 4. Choisissez si votre référentiel est public ou privé. 
Les repos publics sont visibles pour tout le monde, alors que les privés ne sont accessibles que pour vous, et les personnes avec qui vous le partagerez  un README pour votre dépôt. Pour plus d'information, regardez  [Setting repository visibility](https://help.github.com/en/articles/setting-repository-visibility).


![](/images/create-repository-public-private.png "créer un repo public ou privé")

### 5. Sélectionnez "Initialize this repository with a README"

![](/images/create-repository-init-readme.png "créez un fichier readme")

Bien qu'un fichier README ne soit pas un élément obligatoire d'un repo GitHub, c'est une très bonne habitude à prendre que d'en placer un. Les READMEs sont un endroit génial pour décrire vore projet ou ajouter un peu de documentation comme savoir comment installer ou utiliser votre projet. Vous pourriez y ajouter une information de contact — si votre projet devient populaire, les personnes voudront vous aider.

##### 5.1. Plus sur les READMEs

Si vous ajoutez un fichier avec le nom de fichier "README" dans votre repo, il sera automatiquement affiché sur la page d'accueil de votre repo. Cool non ? GitHub supporte différents formats de fichiers README. Celui dans ce tutoriel donnera un fichier texte basique mais les autres formats comme `.markdown` ou `.textile` peuvent être utilisés pour restituer du contenu HTML comme des liens et des titres. Pour plus d'informations sur les formats de marquage supportés, regardez [https://github.com/github/markup](https://github.com/github/markup).

### 6. Cliquez sur "Create Repository"

Bravo. Vous avez créé votre premier référentiels, et l'avez initialisé avec un fichier *README*.

### 7. Committez votre première modificaiton

Pensez à un commit comme un instantané de votre projet - code, fichiers, tout - à un instant t. Après votre premier commit, git ne sauvegardera que les fichiers qui ont été modifiés, d'où le gain d'espace.

Attention : git fera de son mieux pour compresser vos fichiers, mais les gros fichiers et les binaires peuvent amener un dépôt à devenir obèse et peu maniable. Essayez d'éviter de committer des choses comme des ficihers compressés (zips, rars, jars), du code compilé (fichiers object, bibliothèques, exécutables), sauvegardes de database et fichiers média (flv, psd, musique, films)


Un _[commit](https://help.github.com/en/articles/github-glossary#commit)_ est comme un instantané de tous les fichiers de votre projet à un point donné dans le temps.

Quand vous avez votre nouveau référentiel, vous l'avez initialisé avec un fichier _README_. Les fichiers _README_ sont un endroit génial pour décrire en détail votre projet, ou ajouter un peu de documentation comme la manière d'installer ou d'utiliser votre projet. Les contenus de votre fichier _README_ sont affichés automatiquement sur la page d'accueil de votre référentiel.

Commitons un changement au fichier _README_.

  1. Dans la liste de votre repo de fichiers, cliquez sur **_README.md_**.

![Fichier Readme dans la liste de fichiers](/images/create-commit-open-readme.png "ouvrir readme pour créer un commit")

  2. Au dessus du contenu du fichier et à droite, cliquez sur le crayon .

  3. Sur l'onglet **Edit file**, tapez un peu d'information vous concernant.

![Nouveau contenu dans le fichier](/images/edit-readme-light.png "Nouveau contenu dans le fichier")

  4. Au-dessus du nouveau contenu, cliquez sur **Preview changes**.

![Bouton de prévisualisation de fichier](/images/edit-readme-preview-changes.png "Bouton de prévisualisation de fichier")

  5. Révisez les modifications que vous avez faites au fichier. Vous verrez le nouveau contenu en vert.

![Voir la prévisualisation de fichier](/images/create-commit-review.png "voir la prévisualisation du commit")

  6. En bas de la page, tapez un message court, ayant du sens de commit, qui décrit la modification que vous avez produite au fichier. Vous pouvez attribuer le commit à plus d'un auteur dans le message de commit. Pour plus d'informations, regardez l'article "[Créer un commit avec plusieurs co-auteurs](https://help.github.com/en/articles/creating-a-commit-with-multiple-authors)."

![Message de Commit pour votre modification](https://help.github.com/assets/images/help/repository/write-commit-message-quick-pull.png)

  7. Sous les champs de message de commit, décidez si vous ajoutez votre commit à la branche en cours ou sur une nouvelle branche. Si votre branche en cours est `master`, vous devriez choisir une nouvelle branche pour votre commit et [créer ensuite une  pull request](https://help.github.com/en/articles/creating-a-pull-request).

![Options de Commit sur branche](https://help.github.com/assets/images/help/repository/choose-commit-branch.png)

  8. Cliquez sur **Propose file change**.

![Bouton de proposition de modification de fichier](https://help.github.com/assets/images/help/repository/propose-file-change-quick-pull.png)

  
## Fêtez ça ! 

Félicitations ! Vous avez maintenant créé un repo sur GitHub, créé un fichier *README*, avez créé votre premier *commit* sur GitHub. Que voulez-vous faire ensuite ?

- [Installer Git](/2013/12/10/installer-git/)
- **Créer un Repo**
- [Forker un Repo](/2013/12/16/forker-un-repo-github/)
- [Être Social](/2013/12/16/github-etre-social/)

## Ailleurs 
- [Les bases de Git - Démarrer un dépôt Git](http://git-scm.com/book/fr/Les-bases-de-Git-D%C3%A9marrer-un-d%C3%A9p%C3%B4t-Git) - pour réviser et apprendre à cloner un dépôt existant.

![image](http://imgs.xkcd.com/comics/git_commit.png)