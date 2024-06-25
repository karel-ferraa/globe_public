Horaires 8h 10 fin 16h 45, 15h~ vendredi. Attention le magazin ferme a 16h15, faut eviter de se faire enfermer.

Actuellement, les Objets sont rangés par catégorie. Meme problème que pour l'allocation de mémoire quand on veut rajouter des objets et que la catégorie est pleine il faut tout bouger.
- Il faut pouvoir stocker les objets de façon non contigue.
- Il faut pouvoir optimiser l'occupation de l'espace. Mettre les objets de petite taille dans des petits espaces de stockage.
    + Mesurer le taux d'occupation approximatif
- Il faut pouvoir mettre les objets à haute utilisation dans des espaces accessibles rapidement (stockage chaud) tandis que les objets les moins utilisés peuvent remplir les espaces moins accessibles comme les étagères du haut.

# Ce qu'il reste à faire

Définir une hauteur maximale pour tous les espaces de stockage de pallettes et stockage de masse. Apres discussion avec Eric, la hauteur maximale est celle du plafond / 3m.
Définir des espaces de stockage en BRA, BRB, BRC. Il serait bien d'y mettre des étagères (a ajouter dans les precos).
Stockage des pallettes, apres discussion avec Eric: pour pouvoir récupérer une pallette individuelle, il faut au moins 2,50 metres derriere la pallette donc c'est inenvisageable car il n'y aurait que tres peu de place pour stocker les pallettes. 
Les contraintes sont donc les suivantes: avoir assez d'espace pour que quelqu'un puisse se glisser entre les pallettes pour en faire l'inventaire (environ 30-40 centimetres). 
Avoir assez d'espace entre le stockage pallettes et les etageres alentours pour que quelqu'un puisse s'accroupire et récupérer un objet dans l'étagere.
Ajouter les étagères proches du bureau de Fred. Ajouter toutes les étageres qui trainent dans la database. (et les rajouter sur la database Actuel, en Sans label. Il faudra changer des precos).
Ajouter couleurs zones.
Vérifier que rien n'a été oublié dans la database, notamment les racks.
S'assurer que on ne compte pas les emplacements au dessus des etageres.
Noter les dimensions max des etiquettes pour chaque étagère.

Peut-etre remesurer certains emplacements qui ont des contraintes spéciales, par exemple ceux avec une poutre qui passe au milieu.
Ajouter portes, escaliers, barrierres.
Ajouter le détail des racks et des emplacements.
Ajouter de la texture. (peut-etre en prenant des photos avec mon téléphone)
Ajouter des modèles pour distinguer visuellement les etageres des emplacements de stockage de masse / pallettes.
Noter quelles etageres qui sont déplaçables.

Une fois les préconisations faites, il faudra ajouter les emplacements dans Syllobe, via importation d'un fichier csv.

Faire un beau rapport récapitulatif du travail fait avec de la doc, des stats sur le stockage et des préconisations.
Demander à Eric si je peux récupérer un des vieux pc en haut.

Constat: Dans Sylobe actuellement c'est rangé par référence. On peut chercher une référence et voir son emplacement. Mais si on ne stocke plus par catégorie, c'est à chaque objet qu'il faut assigner un emplacement. Non, pas forcemment, on peut avoir un emplacement par référence mais les références ne se suivent pas.

Si on a du temps, replacer les espaces de stockage [41-47] et mesurer la hauteur du plafond dans cette salle.

## Preconisations

### Zone B

Séparer le B01 en deux espaces de stockages dans la database.
Pointer le fait qu'il n'y a peut-etre pas tant de différences que ça entre le scénario peu efforts et le scénario grands efforts

## Documentation

Expliquer comment se servir de Blender de façon basique / ou trouver des tuto.

### Pour les utilisateurs avancés

Je peux donner acces au repo git, qui est privé pour des raisons de sécurité étant donné qu'il y a l'emplacement de tous les détecteurs sur le plan.
Expliquer git diff pour avoir la diff entre la database actuelle et les préconisations.

## Plan

Ajouter les racks sur le plan. Cela veut dire qu'il faudra séparer les labels qui ont plusieurs etageres.
Utiliser des assets pour que l'on puisse visuellement distinguer les types d'espaces de stockage.

# Lessons / découvertes

Couple: Force appliquée.
Logiciels de gestion de magasin.

Chez Lautrette, ils creent des bougies qui servent a filtrer l'oxygene dans les hauts fourneaux. Ces bougies sont envoyées pour être dégraissées chez un partenaire, car l'oxygene sous pression s'enflamme et explose avec la graisse. [./Images/bougie_oxygene.jpg]

Travail des personnes qui étaient dans le bureau avec moi: préparent des visseuses qui sont controlées par des cartes électroniques et qui servent ensuite à automatiser le montage de véhicules chez Opel en Allemagne. Ils montent les cartes électroniques et développent les programmes de vissage.
Sur la visseuse [./Images/visseuse_electronique.png], on peut voir le réducteur, pièce qui sert à augmenter le couple en baissant les tours par minute. On peut aussi voir le capteur qui rapporte le couple appliqué à la carte éléctronique par le fil. Cela permet de controller que le vissage a bien été effectué. La mesure est transmise en digital car cela permet de detecter les perturbations (par exemple un gros aimant à coté) et d'arreter le cycle en rapportant une erreur plutot que de rapporter une fausse valeur.
Sur [./Images/boitier_visseuse_electronique.png], chaque visseuse est controllée par une carte qui peut avoir plusieurs programmes de vissage. Toutes les cartes sont ensuite controllées par une carte maitre qui va controller quelles programme de vissage va etre lancer sur chaque visseuse.
