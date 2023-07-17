Horaires 8h 10 fin 16h 45, 15h~ vendredi. Attention le magazin ferme a 16h15, faut eviter de se faire enfermer.

Actuellement, les Objets sont rangés par catégorie. Meme problème que pour l'allocation de mémoire quand on veut rajouter des objets et que la catégorie est pleine il faut tout bouger.
- Il faut pouvoir stocker les objets de façon non contigue.
- Il faut pouvoir optimiser l'occupation de l'espace. Mettre les objets de petite taille dans des petits espaces de stockage.
    + Mesurer le taux d'occupation approximatif
- Il faut pouvoir mettre les objets à haute utilisation dans des espaces accessibles rapidement (stockage chaud) tandis que les objets les moins utilisés peuvent remplir les espaces moins accessibles comme les étagères du haut.

# Besoins

Il faudrait ensuite ajouter du détail en ajoutant les racks et ensuite les emplacements sur le plan. Peut etre utiliser des assets pour les etageres sur le plan, rajouter les escaliers, mieux modeliser l'entrepot avec le toit en pente ect...

# Ce qu'il reste à faire

Ajouter les etageres des espaces de stockage perdus au fond du sous-sol.
A8A: les racks et emplacements. Le placard est fermé, il faut demander les clées pour ouvrir -> Georges. La salle au 1er etage fermée. Le sous-sol pres du monte-charges fermé. Le sous-sol au fond fermé.
S'assurer que on ne compte pas les emplacements au dessus des etageres.
Peut-etre remesurer certains emplacements qui ont des contraintes spéciales, par exemple ceux avec une poutre qui passe au milieu.
Ajouter la collection sécurité.
Ajouter portes, escaliers, barrierres. Ajouter la mezzanine et sa hauteur zone M, N.
Ajouter des modèles pour distinguer visuellement les etageres des emplacements de stockage de masse / pallettes.
Ajouter le détail des racks et des emplacements.
Ajouter de la texture. (peut-etre en prenant des photos avec mon téléphone)
Noter quelles etageres qui sont déplaçables.

Zone M - Mesurer et ajouter le M10

Ajouter les préconisations. Il y a pleins de racks a relabelliser ect...
Séparer les labels qui ont plusieurs etageres en plusieurs entrées, comme ça on peut avoir les valeurs de longueur largeur hauteur plus accurate. Soit ça soit on rentre dans le detail sur le plan avec les racks et les emplacements.
Régulariser la zone P.

Noter les dimensions max des etiquettes pour chaque étagère.

Une fois les préconisations faites, il faudra ajouter les emplacements dans Syllobe, via importation d'un fichier csv.

Faire un beau rapport récapitulatif du travail fait avec de la doc, des stats sur le stockage et des préconisations.
Demander à Eric si je peux récupérer un des vieux pc en haut.

Constat: Dans Sylobe actuellement c'est rangé par référence. On peut chercher une référence et voir son emplacement. Mais si on ne stocke plus par catégorie, c'est à chaque objet qu'il faut assigner un emplacement. Non, pas forcemment, on peut avoir un emplacement par référence mais les références ne se suivent pas.

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
