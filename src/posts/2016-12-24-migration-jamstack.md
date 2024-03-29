---
title: Migration vers la jamstack
date: 2016-12-24 04:19:00 +01:00
tags:
- domaine
- jamstack
- CDN
- OVH
- SSL
- https
- Netifly
- registrar
- indieweb
- engagements
---

Officiellement en vacances sur le "free-lancing", pause en famille et déconnexion sociale jusqu'à lundi pour penser ma stratégie 2017 à valider avec mes trois enfants...

La nouvelle interface de publication (Siteleaf)  m'ouvre ici un chemin facile pour déposer un point technique rapide afin de

- valider mon plan de route 2017 avec les dévs de [JamStatic](https://jamstatic.fr)
- raffiner [deux premiers engagements pris sur l'indieweb](https://indieweb.org/2017-01-01-commitments#Commitments) (deadline 2016-12-31)

![Roadmap - bertrand keller jamstatic-fr 2016-12-20](/images/Roadmap%20-%20jamstatic-fr%202016-12-20.png)

Après un [gros mal de crâne vécu avant-hier](http://ducamp.me/2016-357) pour me simplifier la vie en 2017 (domaine, admin serveurs, performance/sécurité et activation d'un certificat SSL sur ce domaine),... très heureux de recevoir une bonne nouvelle de la part du "registrar" OVH :

> Concerne le transfert du nom de domaine : christopheducamp.com, OVH a reçu une notification le 2016-12-24 indiquant que vous aviez demandé le transfert de votre nom de domaine vers un autre registrar (Gandi SAS (IANA xxxx xx xx)).<br>Si vous souhaitez CONFIRMER cette demande de transfert, **vous n'avez rien à faire**.

## Statut à date

Pointage du domaine de OVH sur le [CDN](http://ducamp.me/CDN) Netifly :

![OVH 2016-12-24.png](/img/ovh-2016-12-24.png)

### Résultats du "Speedtest" proposé par Netifly

Ce test [https://testmysite.io](https://testmysite.io) me semble être une pure auto-promotion pour Netifly et sa jamstack (jargon à vérifier)...

![Netlify Speedtest 2016-12-24 06-.png](/images/netlify-speedtest-2016-12-24.png)

## Performance et Progressive Web Apps : 49/100

@[DirtyF](https://twitter.com/DirtyF) : Un grand merci pour l'image, les liens. Si je comprends bien, le test ci-dessus est bien invalidé par la communauté JamStatic. Concentré à cette heure sur les fondamentaux. Très motivé pour plonger l'année prochaine dans la check-list de Google [LightHouse](http:ducamp.me/LightHouse).

## Check-list

Le chantier est en cours : beaucoup d'erreurs à corriger. Un travail immense s'ouvre pour réaménager les premières briques de construction indieweb avant de parvenir à réaliser un site professionnel.

Je me réjouis néanmoins d'avancer en 2017 par petites itérations sur le plan de route décrit tout en haut et traduit en bas dans un planning.

Encore un grand merci à Bertrand et Frank pour l'accompagnement en douceur.

Bon Noël à tous.

## Planning tentatif

- 2016-12-29 [Réglages DNS à faire chez Gandi pour pointer sur le CDN Netifly ou CloudFlare](http://ducamp.me/2016-357#SSL_sur_domaine_apex_christopheducamp.com) et partir sereinement en 2017 étudier d'autres interfaces-utilisateurs dans la **JAMstack**.
- 2016-12-31 rédiger et déposer [un engagement indieweb 2017](https://indieweb.org/2017-01-01-commitments) : "redéposer mes notes de statut sur mon propre site".
- 2017-01 [Tester les performances et évaluer la qualité](https://medium.com/@JeremyRaffin/site-web-statique-optimis%C3%A9-avec-github-pages-partie-4-tester-les-performances-et-%C3%A9valuer-la-f42ed88a5d44#.w7clu8fbq).
- 2017-01 Schéma URL : étudier l'architecture d'URL revenue avec `www`. [Arguments `nowww` sur la sécurité en cours d'étude](http://ducamp.me/Nowww) et à raffiner avec des experts.
- 2ème semestre 2017 : étudier les Progressive Web Apps.