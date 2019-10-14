---
title: "CMS versus JAM Stack"
date: 2019-10-14T11:36:42+02:00
draft: false
---
Aujourd’hui les CMS telle que Wordpress ou Drupal sont au coeur du développement de site web. Leur prise en main ainsi que leur facilité d’utilisation en font des incontournables dans le domaine du web. Pour tous non-initiés au développement, l’utilisation de CMS est indispensable si l’on veut que le client puisse administrer lui-même son site. Mais ceux-ci posent de nombreux problèmes de performance, point crucial à l’heure du développement éco-responsable, où l’on cherche à réduire le nombre de ressource utilisés par les machines.
Avec les CMS actuels, l’on retrouve un schéma de génération de pages qui fait appel à la base de données (BDD). Elle envoie ses données au fichier PHP, qui génère alors une page HTML affichée par le navigateur web. Ce système permet de rendre le tout dynamique (par opposition au sites statiques dont le contenu ne changera jamais). 
Cependant, ce système pose problème si les pages à afficher son statiques car cette approche nous montre qu'à chaque rechargement de page, l’on refait des appels à la base de données et que cela peut s’avérer inutile. En effet la plupart du temps les données reçues seront les mêmes que précédemment. 


Un concept alternatif apparaît alors pour modifier la vision du développement, le JAMstack. JAM, ou Javascript API Markup, est une vision du développement qui met l’emphase sur la non-utilité d’un site à régénérer ses pages à chaque requête qu’il reçoit. C’est alors que JAM pose la conjecture suivante : si ces pages sont vouées à rester les mêmes, pourquoi ne pas les rendre statiques ? L’idée est alors de rendre chaque pages statiques en amont, générant ainsi un site complet. Elles seront transmises au navigateur pour être mises en cache (stocker sur sa propre machine), épargnant ainsi nombre d’étape de génération de page et améliorant les performances de rendu. L'interaction vient alors des informations reçues par une API. Par conséquent, toute la couche logique se situe côté client grâce à javascript.

Plusieurs points vont alors influencer le choix de l’approche JAMStack :

Le SEO, car les pages statiques possèdent des URL simplifiées, améliorant le référencement auprès des algorithmes Google. Cela limite également le problème des duplications de page et donc de duplication de contenu, bête noir du référencement.
La vitesse, les pages statiques sont globalement plus rapide à charger d’une page dynamique. Une page généré dynamiquement effectue obligatoirement une requête pour sa création. 
La sécurité car une page statique est, par définition, sans base de données. Par conséquent si aucune base de données n’y est liée, aucune base de données ne peut-être volée.
