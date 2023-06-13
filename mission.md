Horaires 8h 10 fin 16h 45, 15h~ vendredi

Specifications:

Entrepot
    - Depot
        - Etagères
            - Allées
                - Racks
                    - Lignes (étagères)
                        - Espace de stockage
                            [- Récipient] 
                                - Objets
        - Stockage en masse (au sol)
            - Palletes
                - Espace de stockage

Actuellement, les Objets sont rangés par catégorie. Meme problème que pour l'allocation de mémoire quand on veut rajouter des objets et que la catégorie est pleine il faut tout bouger. Il faut aussi 
- Il faut pouvoir stocker les objets de façon non contigue.

- Il faut pouvoir optimiser l'occupation de l'espace. Mettre les objets de petite taille dans des petits espaces de stockage.
    + Mesurer le taux d'occupation approximatif
- Il faut pouvoir mettre les objets à haute utilisation dans des espaces accessibles rapidement (stockage chaud) tandis que les objets les moins utilisés peuvent remplir les espaces moins accessibles comme les étagères du haut.

# Besoins

- Combiens de depots, lesquels, ou, leur volume
Ensuite on commence par les depots les plus utilises
- Repertorier le nombre, le tag des espaces de stockage
- Volume, occupation
- position, plan 2D/3D

Pour le plan, on met pour chaque depot le volume total. Pour chaque espace de stockage, on met seulement le tag.

Sur le excel, chaque tag a ses mesures.

# Roadmap

Commencer par mesurer la surface totale de l'entrepot

# Echantillon

{
    "Entrepot A": {
        "Longueur": valeur,
        "Largeur": valeur,
        "Surface": valeur,
        "Volume": valeur,
        "Occupation": valeur, # percentage
        "Zones": [
            "Zone A": {
                "Longueur": valeur,
                "Largeur": valeur,
                "Surface": valeur,
                "Volume": valeur,
                "Occupation": valeur, # percentage
                "Etageres": [
                    "Etagere A": {
                        "Longueur": valeur,
                        "Largeur": valeur,
                        "Surface": valeur,
                        "Volume": valeur,
                        "Occupation": valeur, # percentage
                        "Racks": {
                            "Longueur": valeur,
                            "Largeur": valeur,
                            "Surface": valeur,
                            "Volume": valeur,
                            "Occupation": valeur, # percentage
                        }
                    },
                    "Etagere B": {
                        "Longueur": valeur,
                        "Largeur": valeur,
                        "Surface": valeur,
                        "Volume": valeur,
                        "Occupation": valeur, # percentage
                    },
                    "Etagere C": {
                        "Longueur": valeur,
                        "Largeur": valeur,
                        "Surface": valeur,
                        "Volume": valeur,
                        "Occupation": valeur, # percentage
                    }
                ],
                "Palletes": [
                ],
                "Stockage de masse par terre": [
                ]
            },
            "Zone B": {
            },
            "Zone C": {
            },
            "Zone D": {
            },
        ]
    }

