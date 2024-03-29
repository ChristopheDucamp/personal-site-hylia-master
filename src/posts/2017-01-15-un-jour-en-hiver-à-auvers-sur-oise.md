---
title: Un Jour en Hiver à Auvers-sur-Oise
date: 2017-01-15 09:48:00 +01:00
tags:
- 100DaysOfPhotos
- Jekyll
- SiteLeaf
- CloudCannon
- jamstatic
- indieweb
subtitle: Promenade dans les Interfaces pour déposer mon flux de travail Photo sur la JAMstack
author: xtof
header-img: uploads/2017-015-JATP-Kenny-Barron-2.jpg
---
*Promenade dans les Interfaces pour déposer mon flux de travail Photo sur la JAMstack*

Jolie promenade [hier](http://ducamp.me/2017-014) à Auvers-sur-Oise sur les traces de Vincent Van Gogh. Je me suis simplement *placé dans les yeux de Barbara* avec un simple Canon 50 mm/1.8 pour tenter de capter quelques émotions de ce village bien mort en hiver. Je viens de [poser sur Flickr quelques photos stimulantes](https://www.flickr.com/search/?sort=date-taken-desc&amp;safe_search=1&amp;tags=auverssuroise&amp;user_id=37996578526%40N01&amp;view_all=1) afin d'organiser quelques promenades photographiques au Printemps.

## Démarrage avec un PhotoFlow basé sur un export Adobe LightRoom et SiteLeaf

Bonne occasion pour tester de nouveau un export de "PhotoFlow" sur la [JamStack](http://ducamp.me/jamstack). Un PhotoFlow cohérent avec les valeurs de l'indieweb. La diffusion de mes photos se fait chez moi sur mon propre domaine. 

Depuis plus d'un mois, j'utilise le système de gestion de contenu [SiteLeaf](https://siteleaf.com) (tant pour accéder à une interface-utilisateur de *mise à jour de post* que pour *déposer quelques fichiers images*). Malheureusement, ce matin je me retrouve en dépassement du quota maximal de 100Mo offert dans le plan gratuit...

Rapide récapitulatif avant de m'engager sur un plan payant chez SiteLeaf :

1. dérushage et sélection de quelques photos dans Adobe Lightroom avec les raccourcis-clavier "P" et "X"
2. pose de mots-clés sur les photos sélectionnés
3. optimisation de quelques photos pour bascule en N&B avec les outils de [Google Nik collection](https://www.google.com/intl/fr/nikcollection/)
4. exportation dans un dossier (renommage)
5. téléversement des fichiers directement dans l'interface du syst&egrave;me de gestion de contenu SiteLeaf
6. Les photos sont **stockées** sur le CMS SiteLeaf et facilement accessibles dans l'interface-utilisateur.
7. Elles peuvent être insérées une par une dans la fenêtre de publication. Pas de dépose possible de galerie.

Plus bas, je me contenterai donc de déposer une sélection de quelques photos prises hier à l'aide de l'**interface-utilisateur image** placée au-dessus de la fenêtre de publication.

## Prévisualisation dans SiteLeaf : erreur et gem absente.

Essai de g&eacute;n&eacute;ration de pr&eacute;-visualisation SiteLeaf… Erreur, [Siteleaf](https://www.siteleaf.com/) me r&eacute;clame de passer sur un plan payant pour augmenter mon quota de stockage limit&eacute; &agrave; 100Mo sur le plan gratuit. Après paiement, le "build" est refus&eacute; sous pr&eacute;texte d'absence d'une gem de Jekyll "jekyll-paginate" d&eacute;j&agrave; install&eacute;e…

```bash
Deprecation: You appear to have pagination turned on, but you haven't included the `jekyll-paginate` gem. Ensure you have `gems: [jekyll-paginate]` in your configuration file. (RuntimeError)
```
&Eacute;trange car le build fonctionne ailleurs. Grosse fatigue. Mais rien de grave à cette heure : 

1. Il existe plusieurs CMS permettant de travailler sur un repo de site statique d&eacute;pos&eacute; chez GitHub
1. La synchronisation fonctionne avec [mon repo GitHub](https://github.com/ChristopheDucamp/xtof-clean-blog).

## Premiers pas dans l'UI de CloudCannon

[CloudCannon](https://cloudcannon.com) est un autre CMS r&eacute;put&eacute; sur la JamStack et recommandé par certains membres de la communauté JamStatic.

Essai de connexion sur l'interface-web de CloudCannon et synchronisation avec mon dépôt GitHub. Rassuré de retrouver le contenu de ce m&ecirc;me post dans la fenêtre de publication proposée par CloudCannon. 

Je poursuivrai ces tests avec quelques nouvelles photos comme Auvers et ses environs, la transe vécue sur les prochaines jam-session du JATP, etc..

![photowalk-auvers-14.jpg](/images/auvers/photowalk-auvers-14.jpg)

![photowalk-auvers-.jpg](/images/auvers/photowalk-auvers.jpg)

![photowalk-auvers-2198.jpg](/images/auvers/photowalk-auvers-2198.jpg)

Si ce type de promenade à Auvers vous intéresse, faites-moi signe. Je serai ravi de vous inviter pour un Safari-Photo dans un village qui a tous les atouts pour attirer les touristes en hiver. Après la balade (comptez 2 bonnes heures), je vous offrirai un thé dans le salon pour vous faire essayer quelques interfaces de CMS encore assez "geeks" de mon point de vue.

Mon offre est purement intéressée : à défaut de trouver le *photoflow*, je cherche le truc facile à proposer aux artisans,  photographes, musiciens, chanteurs et artistes non geeks qui pourraient aimer publier sur la *jamstack*.

![2017-015-JATP-Kenny-Barron.jpg](/images/2017-015-jatp-kenny-barron.jpg)
(Transe au&nbsp;[J.A.T.P. du 2017-015](http://ducamp.me/2017-015#Here_.26_Now_JATP.C2.A0) - *photoflow*&nbsp;<span class="h-card p-author">[xtof.me](http://xtof.me)</span>)

Bonne semaine à tous.