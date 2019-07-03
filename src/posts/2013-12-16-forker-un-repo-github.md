---
title: Forker un Repo sur GitHub
date: 2013-12-16
tags:
- github
- git
- repo
- fork
- howto
- tutoriel
slug: forker-un-repo-github
subtitle: Un fork (bifurcation) est une copie d'un référentiel. Ce peut être une bonne base pour démarrer.
author: Christophe Ducamp
---

Lien de référence : <span class="h-cite"><cite class="p-name u-url">[Fork A Repo](https://help.github.com/articles/fork-a-repo/)</cite></span>

## Forker un Repo

*Un fork est une copie d'un dépôt. Forker un dépôt vous permet d'expérimenter librement des modifications sans toucher au projet original.*

Plus communément, les forks sont utilisés soit pour proposer des modifications sur le projet de quelqu'un d'autre ou pour utiliser le projet de quelqu'un d'autre comme point de départ pour une nouvelle idée.

####  Proposer des modifications sur le projet de quelqu'un d'autre

Un exemple génial d'utilisation des forks est de proposer des modifications sur le projet de quelqu'un d'autre ou d'utiliser le projet de quelqu'un d'autre comme point de départ pour votre propre idée. Plutôt que de signaler un problème que vous trouvez, vous pouvez : 
- Forker le repository
- Réparer le bug
- Proposer une *pull request* au propriétaire du projet.

Si le propriétaire du projet aime votre travail, il pourrait prendre votre réparation pour la ramener dans le dépôt original !

#### Utiliser le projet de quelqu'un d'autre comme point de départ d'une nouvelle idée. 

Au [coeur de l'open source](http://opensource.org/about) il y a l'idée qu'en partageant du code, nous pouvons produire un logiciel meilleur et de confiance.

Au moment de créer un dépôt public à partir d'un fork du projet de quelqu'un d'autre, assurez-vous d'inclure un [fichier de licence](http://choosealicense.com/) qui déterminera comment vous voulez que votre projet soit partagé avec d'autres.

Pour plus d'information sur l'open source, spécifiquement sur la façon de créer et faire grandir un projet open source, nous avons créé les [Guides Open Source](https://opensource.guide/) qui  vous aideront à vous aideront à développer une communauté open source saine en recommandant les meilleures pratiques pour la création et l'entretien de dépôts pour votre projet open source.

## Forker un repository d'exemple 

Forker un repository est un processus très simple en deux étapes. Nous avons créé un repository pour vous entraîner. 

1. Sur GitHub, naviguez vers le dépôt [spoon-knife](https://github.com/octocat/Spoon-Knife)
2. Dans le coin en haut et à droite de la page, cliquez sur **Fork**

Voilà, c'est fait ! Vous disposez désormais d'un *fork* du dépôt   original `octocat/Spoon-Knife repository`

![](/images/fork_button.png "bouton fork")

## Maintenez votre fork synchronisé 

Vous pourriez avoir forké un projet afin de proposer des modifications vers l'*upstream*, ou le dépôt original. Dans ce cas, c'est une bonne pratique que de synchroniser régulièrement votre fork avec le repository original. Pour faire ça, vous devrez utiliser Git à la ligne de commande. Vous pouvez pratiquer le réglage du dépôt upstream en utilisant le même repository `[octocat/Spoon-Knife](https://github.com/octocat/Spoon-Knife) que vous venez de forker. 

### Étape 1 : Installez et Paramétrez Git 

Si ce n'est déjà fait, vous devez d'abord [installer et régler Git](/installer-git/). N'oubliez pas non plus de [régler l'authentification vers GitHub à partir de Git](https://help.github.com/articles/set-up-git#next-steps-authenticating-with-github-from-git).


### Étape 2 : Créez un clone local de votre fork

À ce stade, vous avez un fork du repository Spoon-Knife, mais vous n'avez pas les fichiers dans ce repository sur votre ordinateur. Créons localement un *clone* de votre fork sur votre ordinateur.

1. Sur GitHub, naviguez vers **votre fork** du dépôt Spoon-Knife.
2. Sous le nom du dépôt, cliquez sur **Clone or download** 
![](/images/clone-repo-clone-url-button.png "bouton clone or download")
3. Dans le Clone avec la section HTTPs, cliquez sur l'icône fléchée pour copiez l'URL de clone du dépôt. 
![](https://help.github.com/assets/images/help/repository/https-url-clone.png "cliquez sur l'icône fléchée pour copier l'URL du dépôt")
4. Ouvrez la fenêtre de Terminal
5. Tapez `git clone`, et collez ensuite l'URL que vous avez copiée à l'étape 2. Cela ressemblera à cela, avec votre nom d'utilisateur GitHub au lieu de `VOTRE-NOMUTILISATEUR`:
```bash
git clone https://github.com/VOTRE-NOMUTILISATEUR/Spoon-Knife
```
6. Pressez la touche **Retour**. Votre clone local sera créé.

```bash
git clone https://github.com/YOUR-USERNAME/Spoon-Knife
Cloning into `Spoon-Knife`...
remote: Counting objects: 10, done.
remote: Compressing objects: 100% (8/8), done.
remove: Total 10 (delta 1), reused 10 (delta 1)
Unpacking objects: 100% (10/10), done.
```

Vous avez désormais une copie locale de votre fork du repository Spoon-Knife !

### Étape 3 : Configurer Git pour synchroniser votre fork avec le dépôt original Spoon-Knife

Quand vous forkez un projet afin de proposer des modifications sur le repository original, vous pouvez configurer Git pour tirer les modifications à partir du dépôt original, ou *upstream*, à l'intérieur du clone local de votre fork. 

1. Sur GitHub, naviguez vers le dépôt [octocat/Spoon-Knife](https://github.com/octocat/Spoon-Knife).
2. Sous le nom de votre dépôt, cliquez **Clone or download** 
![](/images/clone-repo-clone-url-button.png "bouton clone url")
3. Dans le Clone avec la section HTTPs, cliquez sur l'icône fléchée "copy to clipboard" pour copier l'URL clone du repository. 
![](/images/https-url-clone.png "cliquez sur l'icône fléchée")
4. Ouvrez le Terminal.
5. Changez de répertoire" (`cd`) pour aller à l'endroit du fork que vous avez cloné à l'étape 2 
	1. Pour aller à votre répertoire d'accueil, tapez juste `cd` sans autre texte.
	2. Pour lister les fichiers et répertoires dans votre répertoire actuel, tapez `ls`.
	3. Pour aller dans l'un de vos répertoires listés, tapez `cd votre_liste_repertoire`.
	4. Pour remonter d'un répertoire, tapez `cd ..`
6. Tapez `git remote -v`et pressez la touche **Retour**. Vous verrez le dépôt distant actuel configuré pour votre fork.
```bash
git remote -v
origin  https://github.com/VOTRE_NOMUTILISATEUR/VOTRE_FORK.git (fetch)
origin  https://github.com/VOTRE_NOMUTILISATEUR/VOTRE_FORK.git (push)
```
7. Tapez `git remote add upstream`, puis collez l'URL que vous avez copiée à l'étape 2 et pressez **Retour**. Cela ressemblera à ça : 
```bash
git remote add upstream https://github.com/octocat/Spoon-Knife.git
```
8. Pour vérifier le nouveau dépôt "upstream" que vous avez spécifié pour votre fork, tapez de nouveau `git remote -v`. Vous devriez voir l'URL de votre fork sous `origin`, et l'URL pour le dépôt  original sous `upstream`.

```bash
git remote -v
origin    https://github.com/VOTRE_NOMUTILISATEUR/VOTRE_FORK.git (fetch)
origin    https://github.com/VOTRE_NOMUTILISATEUR/VOTRE_FORK.git (push)
upstream  https://github.com/PROPRIETAIRE_ORIGINAL/REPO_ORIGINAL.git (fetch)
upstream  https://github.com/PROPRIETAIRE_ORIGINAL/REPO_ORIGINAL.git (push)
``` 

Maintenant, vous pouvez maintenir votre fork synchronisé avec le dépôt upstream à l'aide de quelques commandes Git. Pour plus d'information, voir "[Synchroniser un fork](https://help.github.com/articles/syncing-a-fork)."

## Prochaines étapes

Le ciel est la limite avec les modifications vous pouvez produire un fork, incluant :

- la **Création de Branches** : les branches vous permettent de construire de nouvelles fonctionnalités ou de tester des idées sans mettre votre projet principal en péril.
- **Ouvrir des pull requests** : Si vous espérez contribuer en retour sur le dépôt original, vous pouvez envoyer une demande à l'auteur original de tirer votre fork dans son dépôt en lui proposant une *[pull request](https://help.github.com/articles/about-pull-requests)*.

## Trouver un autre repository à forker 

Chaque repository public peut être forké, aussi à vous de trouver un autre projet qui vous intéresse et de le forker ! Pour plus d'informations, regardez "[About forks](https://help.github.com/en/articles/about-forks) sur GitHub"


Vous pouvez [Explorez Github](https://github.com/explore) pour trouver des sujets et commencer à contribuer à des dépôts open source. Pour en savoir plus, regardez comment "[Trouver des projets open source sur GitHub](https://help.github.com/en/articles/finding-open-source-projects-on-github)."

![](https://help.github.com/assets/images/help/repository/fork-repo-explore.png "explore github")

### Célébrez 

Vous avez désormais forké un dépôt, mis en pratique le clonage de votre fork, et configuré un repository upstream. Que voulez-vous faire ensuite ?

* [Installer Git](/2013/12/10/installer-git/)
* [Créer un Repo](/2013/12/16/creer_un_repo_GitHub/)
* **Forker un Repo**
* [Etre Social](/2013/12/16/github-etre-social/)
