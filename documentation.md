# Comment se servir de ces documents?

Le travail effectué est séparé en plusieurs dossiers.
```text
Actuel
    -- database.json
    -- plan.blend
    -- problemes.md
Preconisations
    Scenario_grand_effort
        -- database.json
        -- plan.blend
        -- problemes.md
    Scenario_peu_effort
        -- database.json
        -- plan.blend
        -- problemes.md
documentation.md
```

Dans le dossier "Actuel", vous trouverez une représentation actuelle de l'entrepot. Le fichier database.json contient un inventaire de l'entrepot avec des informations sur les espaces de stockage comme leur dimension, le nombre de pallettes trouvées ect... Ce fichier est au format JSON, il est entièrement constitué de texte et peut donc être lu avec n'importe quel application qui peut lire des fichiers textes (par exemple notepad sur Windows). Le fichier plan.blend contient un plan de l'entrepot. Ce fichier est au format .blend donc il n'est que lisible par le logiciel Blender. Le logiciel Blender est libre et open source, il peut être téléchargé gratuitement depuis [leur site officiel](https://www.blender.org/download/) sur toutes les plateformes (Windows, MacOS, Linux). Le fichier problèmes.md est une liste des problèmes rencontrés pour chaque zone. Ce fichier est au format Markdown, il est entièrement constitué de texte et peut donc être lu avec n'importe quel application qui peut lire des fichiers textes (par exemple notepad sur Windows).
Dans le dossier Preconisations, vous trouverez une représentation de l'entrepot une fois les préconisations appliquées, ainsi que les étapes à effectuer afin d'arriver à cette configuration. Pour plus d'informations sur les préconisations voir la section Préconisations plus bas.

# Terminologie

L'entrepot est divisé en **zones** (ex: Zone A). Chaque zone est divisé en **espaces de stockage** (ex: A01). Chaque espace de stockage est divisé en **racks** (ex: A01A). Chaque rack est divisé en **emplacements** (ex: A01A01).

> Un espace de stockage peut avoir comme "type": "etagere simple", "etagere double", "placard", "stockage pallettes" ou "stockage masse"
    - Une "etagere double" est une étagère qui a été séparée en deux allées.
    - Une "etagere simple" est une étagère qui n'a pas été séparée en deux allées
    - Un espace de stockage de masse est un espace ou les objets sont déposés par terre, sans pallette

# Contexte

Actuellement, chaque objet est censé être référencé dans le logiciel ERP Syllobe9. On indique pour chaque objet l'espace de stockage où il est rangé. Seulement, un espace de stockage peut être très grand. Par exemple, l'étagère C04 fait 7,50 mètres de large et contient 42 emplacements de stockage dans lesquels il y a plusieurs objets. Donc, pour pouvoir retrouver rapidement un objet, les objets sont rangés par catégorie.

Le stockage par catégorie a les conséquences suivantes:
- Un exemple simple: j'ai un petit objet Bosch à placer. L'étagère Bosch ne contient que des grands emplacements. L'étagère Siemens ne contient que des petits emplacements. Je ne peut pas stocker mon petit objet Bosch dans l'étagère Siemens parce que ce n'est pas la bonne catégorie. Donc, certaines étagères manquent de place tandis que d'autres sont vides.
- L'espace alloué à une catégorie est fixe. Or, Globe est une entreprise qui évolue et qui décide parfois d'acheter et de stocker de nouvelles références. Si l'étagère de la catégorie est déjà pleine, on a un problème.
- Les objets les plus utilisés ne sont pas placés au emplacements les plus accessibles.
- Les objets les plus lourds ne sont pas forcémment placés au emplacements les plus appropriés (au sol).

Actuellement, quand il n'y a plus de place dans une étagère et qu'il faut y ranger des objets soit:
1. Les objets sont déposés à coté de l'étagère ou sur le dessus de l'étagère.
2. Les objets sont déposés dans un autre emplacement dit de "réserve" et une étiquette indiquant l'emplacement de réserve choisit est collé sur l'emplacement de stockage plein.

Le choix 1. engendre les problèmes suivants:
- Il y a des objets non référencés dans Sylobe. Donc, la prochaine fois que quelqu'un cherche l'objet cette personne va probablement perdre du temps avant de demander à la personne qui a rangée l'objet qui, de mémoire, lui indiquera l'emplacement.
- Les passages sont encombrés et la circulation peut devenir plus difficile, surtout avec les chariots. L'encombrement des passages pose également un risque de sécurité. Si les objets sont déposés au dessus de l'étagère, il y a un risque de chute des objets. De plus, les étagères sont hautes et il n'est pas pratique de déplacer les objets en haut.
Le choix 2. engendre les problèmes suivants:
- Perte de temps à se déplacer dans l'entrepot.
- Stockage souvent mal référencé.
- Les étiquettes ne sont pas forcémment enlevés une fois que le stock est épuisé et donc il reste des étiquettes trompeuses ou qui n'indiquent rien.

Le résultat de la non-optimisation du stockage est de la frustration et de la perte de temps pour les employés et un ralentissement des opérations de vente qui sont parfois mises en attente faute de stockage disponible pour passer les commandes.
Par exemple, le manque de stockage entraine parfois Alain, qui travaille sur la mezzanine de l'actuelle zone AA sur la fabrication de filtres à descendre des filtres de la mezzanine vers un espace de stockage temporaire au sol avant de les remonter pour appliquer une deuxième étape de fabrication des filtres.

Le constat est clair, il ne faut plus stocker par catégorie.

Plutot que de stocker par catégorie, il serait plus efficace de dire dans Syllobe pour chaque objet l'emplacement *précis* où il rangé. De plus, cette méthode offre possibilité d'utiliser des codes barres pour automatiser le rangement. On colle une étiquette code-barre sur chaque emplacement, on colle des étiquettes code-barre sur les objets et à chaque fois que l'on range un objet à un emplacement on peut scanner le code barre de l'objet et le code barre de l'emplacement pour indiquer que l'on à rangé l'objet à cet emplacement, plutot que de remplir un papier.

Pour faire celà, il faut commander des étiquettes avec pour chaque emplacement de stockage un label et un code barre. Pour pouvoir commander ces étiquettes, il faut avoir un inventaire de tous les emplacements de stockage de l'entrepot.
Un inventaire des espaces et emplacements de stockage de l'entrepot a donc été effectué. Quand un espace de stockage sans label a été trouvé, le label suivant lui est assigné: "Sans label *nombre*".

# Préconisations

Une fois l'inventaire fait, des nouveaux labels sont proposés pour les emplacements.
Seulement, quand les nouvelles étiquettes seront mises en place, un problème risque de se produire. Imaginez la chose suivante:
"Un Objet pomme est actuellement placé en A01. Dans Syllobe, il est marqué que l'Objet pomme est en A01. Puis, on installe les nouvelles étiquettes, ce qui fait que l'ancien A01 est maintenant nommé A03. Dans Syllobe, l'Objet pomme est toujours marqué comme étant en A01, mais en réalité il est maintenant en A03."

Pour éviter ce problème, il y a deux choix possibles:
1. Actualiser le placement des objets dans Syllobe en même temps de placer les nouvelles étiquettes. Vu le nombre d'objets stockés, cette solution apparait très fastidieuse. Cependant, elle offre l'avantage de pouvoir renommer les emplacements de stockage comme on l'entends, en donc d'avoir un nommage qui se suit spatiallement (le A01 est à coté du A02 ect...). Il faut également noter que ce choix impliquera surement un temps de réadaptation pour les employés qui devront apprendre la nouvelle position des labels. Malgré tout, ce peut être un choix judicieux si un inventaire de l'entrepot va être fait juste après la pose des nouvelles étiquettes, puisque lors de l'inventaire, les emplacements de tous les objets seront de toute façon remis à zéro. Le nommage à adopter pour ce scénario se trouve dans le dossier [Scenario_grand_effort].
2. Renommer les emplacements de stockage de façon à garder le plus possible la disposition actuelle. Le nombre d'objets dont il faudra actualiser l'emplacement dans Sylobe sera minimisé. La position des labels restera familière pour les employés. Cependant, les labels ne se suivront pas spatialement pour les étagères qui auront été renommées. Le nommage à adopter pour ce scénario se trouve dans le dossier [Scenario_peu_effort].

Le renommage peut également se faire petit à petit, une zone après l'autre. Si l'on commence à renommer une zone, il faut la renommer en entier d'un coup pour éviter les problèmes.

Dans le dossier de chaque scenario se trouve un fichier [preconisations.md] qui récapitule tous les changements à faire. Dans ce fichier, vous remarquerez des listes numérotées. Celles-ci font référence aux listes de problèmes constatés dans le fichier [Actuel/problemes.md].
Par exemple:
```markdown
problemes.md

# Zone A

1. Il y a une étagère sans label (Sans label 01).
```
```markdown
preconisations.md

# Zone A

1. Renommer Sans label 01 en A24.
```

## Explication des choix faits pour les préconisations

Certains problemes de labels (voir problemes.md #Zone B 1, 2; #Zone D 2; #Zone L 1;) sont survenus suite à une reconfiguration des étagères. Par exemple, si l'on a trois étagères A01, A02, A03 et que l'on déplace la A01 en zone B, il faut renommer les étagères A02 et A03. Dans ces conditions, il peut etre interressant d'avoir des etiquettes facilement déplaçables ou renommables afin d'éviter d'avoir à recommander de nouvelles étiquettes à chaque changement de configuration. Apres discussion avec Eric Leconte, il semble etre plus simple de prendre des etiquettes génériques et de changer les etiquettes quand l'entrepot est reconfiguré étant donné que cela n'arrive que rarement, de l'ordre de 1 à 2 fois par an.

Pour le stockage des pallettes, actuellement, les pallettes sont stockées en bloc. Le désavantage de cette disposition est que si l'on veut accéder à une pallette individuelle qui est au millieu du bloc, il faut déplacer des pallettes avant de pouvoir y accéder. L'avantage de cette disposition est qu'elle est efficace en terme de stockage puisque l'on ne perd pas de place à espacer les pallettes entre elles.
Pour les préconisations, il fallait donc faire un choix entre volume de stockage et temps d'accès au stockage.
Après discussion avec Eric, il a été choisi de stocker les pallettes en block: pour pouvoir récupérer une pallette individuelle, il faut au moins 2,50 metres derrière la pallette donc c'est inenvisageable car il n'y aurait que très peu de place pour stocker les pallettes.
Les contraintes sont donc les suivantes: avoir assez d'espace pour que quelqu'un puisse se glisser entre les pallettes pour en faire l'inventaire (environ 30-40 centimetres) et avoir assez d'espace entre le stockage pallettes et les etageres alentours pour que quelqu'un puisse s'accroupire et récupérer un objet dans l'étagere.

# Note sur les mesures

Les mesures de l'entrepot sont au mètre près.
Les mesures d'une zone sont au decimètre près.
Les mesures d'un espace de stockage sont au decimètre près.
Les mesures d'un rack et d'un emplacement de stockage sont au centimètre près.

Les mesures de la zone A n'ont pas été effectuées avec ces règles de précision, elle seront à refaire si il y a du temps disponible.
Pour les emplacements de la zone C c'est l'espace minimal qui est mesuré.

La hauteur des espaces de stockage de masse et de pallette à été mesurée avec celle de la plus haute boite.
