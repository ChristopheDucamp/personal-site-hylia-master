
---
date: "2019-07-02"
title: Régler un schéma URL avec la date dans 11ty
permalink: "/{{ page.date | date: '%Y/%m/%d' }}/index.html"
tags: [schéma URL, 11ty, date]

---

## Schéma URLS 

Migration oblige, je me dois de préserver les URLs telles qu'elles étaient paramétrées sur mon ancien site. À savoir un schéma sous forme de ```https://monsite.com/AAAA/MM/JJ/slug-du-post``` 


## Recherche en cours 

Première consultation de la [documentation 11ty traitant des permaliens](https://www.11ty.io/docs/permalinks/)



```
    ---
    date: "2016-01-01T06:00-06:00"
    permalink: "/{{ page.date | date: '%Y/%m/%d' }}/index.html"
    ---
```

écrira `_site/2016/01/01/index.html`. Il existe une variété de moyens pour régler la variable page.date (utiliser `date` dans le front matter n'est qu'une méthode parmi tant d'autres.) Apprenez en plus sur les [Content dates](https://www.11ty.io/docs/dates/).



