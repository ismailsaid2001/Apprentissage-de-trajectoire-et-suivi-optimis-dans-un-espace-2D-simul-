

Apprentissage de Trajectoire et Suivi Optimisé dans un Espace 2D Simulé
Présentation
Ce projet explore l'utilisation de réseaux de neurones informés par la physique (PiNNs) pour modéliser et prédire la trajectoire d'un volant de badminton dans un espace euclidien 2D. L'objectif principal est de développer un modèle capable de prédire avec précision la position 
(
𝑥
(
𝑡
)
,
𝑦
(
𝑡
)
)
(x(t),y(t)) du volant en tenant compte des forces physiques (gravité, traînée, etc.) et de traiter des données bruitées ou incomplètes.

Approches Utilisées
1. Modélisation Physique et Génération de Données
Trajectoire simulée : Les données sont générées à l'aide des équations de mouvement régissant le déplacement d'un volant sous l'effet de la gravité et de la résistance de l'air.
Ajout de bruit gaussien : Pour simuler les imperfections du monde réel.
Gestion des données manquantes : Tests de robustesse en cas d'observations incomplètes.
2. Architecture du Modèle
Modèle initial : Réseau de neurones avec une seule couche cachée de 256 neurones et une activation sigmoïde.
Optimisations successives :
Cross-validation (k-fold) : Pour éviter le surapprentissage et obtenir des estimations robustes.
Recherche d’hyperparamètres (Grid Search via Optuna) : Optimisation du nombre de neurones, du learning rate, et de la fonction d'activation.
Régularisation L1 et L2 : Pour limiter la complexité du modèle et améliorer la généralisation.
3. Techniques de Visualisation
Tracés des trajectoires prédites vs trajectoires simulées.
Analyse des écarts pour évaluer la précision des prédictions.
Résultats
Modèle Final
Architecture optimale :
512 neurones dans la couche cachée.
Fonction d'activation : Tangente hyperbolique.
Learning rate : 
5.919
×
1
0
−
5
5.919×10 
−5
 .
Entraînement sur 4000 époques.
Performance
Le modèle final a démontré une excellente capacité à prédire des trajectoires cohérentes avec les lois de la physique, même en présence de bruit ou de données manquantes.
Réduction significative des erreurs grâce aux optimisations (L1/L2, Optuna).
Installation
Cloner le dépôt ou télécharger le fichier .zip.
Installer les dépendances nécessaires avec :
bash
Copier
Modifier
pip install -r requirements.txt
Lancer le notebook dans Google Colab pour reproduire les résultats.
Utilisation
Simulation des données : Lancer la cellule de génération pour obtenir des trajectoires bruitées ou incomplètes.
Entraînement : Exécuter l’entraînement du modèle avec les hyperparamètres optimisés.
Visualisation : Observer les trajectoires simulées et prédites.
À Propos
Ce projet a été conçu pour démontrer l’efficacité des réseaux de neurones informés par la physique dans le cadre de l’apprentissage de trajectoires complexes. Il met en lumière l'importance d’intégrer des principes physiques dans les modèles d’apprentissage machine pour améliorer la robustesse et la précision.

Auteur : Ismail
