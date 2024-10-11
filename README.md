Pour entraîner un réseau de neurones à détecter le genre musical d'un morceau, on :

- génère un spectrogramme (représentation visuelle des caractéristiques acoustiques)
- attribue un label au spectrogramme (par exemple : ce spectrogramme représente un morceau de Rock)
- entraîne le modèle à attribuer les bons labels

Le spectrogramme est une image qu'on peut voir sous l'angle d'un tableau de valeurs (pour chaque pixel). L'IA aime les tableaux.

Le CNN (Convolutional Neural Network) va créer un « espace vectoriel » qui est un espace multidimensionnel. Au fur et à mesure de son entraînement, il va essayer de générer des représentations numériques (les vecteurs ou embeddings) qu'on peut voir comme des coordonnées dans l'espace vectoriel et placer ces représentations d'une manière qui fait sens pour lui (pas pour nous).

Une fois entraîné, si je lui donne un morceau de « Rock » puis un morceau de « Lounge », le modèle générera des embeddings assez différents pour les représenter. Si maintenant, je lui donne un morceau de « Punk », il va le ranger beaucoup plus proche du morceau de « Rock ».

Le modèle pré-entrainé que j'utilise est [openl3-env-mel128-emb512](https://essentia.upf.edu/models.html).



    Spectrogramme :
        Un spectrogramme est une représentation visuelle des caractéristiques acoustiques d'un signal audio.
        Il montre comment la puissance ou l'amplitude d'un signal varie en fonction du temps et de la fréquence.

    Labels :
        Les labels sont des étiquettes attribuées aux données d'entraînement pour indiquer leur catégorie ou classe.
        Dans ce cas, les labels correspondent aux genres musicaux. Le modèle va être entrainer à reproduire la performance / qualité des labels posés sur les données d'entrainement. On comprends donc l'interet de soignée la partie data du process.

    CNN et espace vectoriel :
        Les Convolutional Neural Networks (CNN) sont particulièrement efficaces pour traiter des données visuelles comme les images.
        L'espace vectoriel créé par le modèle est un espace multidimensionnel où chaque dimension représente une caractéristique du signal audio.

    Embeddings :
        Les embeddings sont des représentations numériques compactes de données complexes dans un espace à faible dimensionnalité.
        Ils permettent au modèle de capturer des relations entre les différents éléments de la base de données.

    Modèle EmbeddingsOpenL3 :
        C'est un modèle pré-entraîné spécifiquement conçu pour l'analyse audio.
        Il utilise une architecture OpenL3 (Large-scale Audio Classification) modifiée pour produire des embeddings.
