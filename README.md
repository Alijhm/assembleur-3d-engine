# Moteur de Rendu 3D (Assembleur x86-64)

Ce projet implémente un pipeline de rendu 3D "fil de fer" (wireframe) en **assembleur x86-64** pour Linux. En partant d'une base fournie pour la gestion de l'affichage graphique (X11), l'objectif a été de développer toute la logique mathématique et géométrique du moteur.

Ce projet d'architecture matérielle met en valeur des compétences clés directement transposables au calcul intensif et à la data :
* **Algèbre linéaire :** Codage de matrices de rotation 3D et de produits vectoriels, constituant la base mathématique des algorithmes de *Deep Learning*.
* **Optimisation CPU (Instructions SSE) :** Exploitation des capacités vectorielles du processeur (SIMD) pour paralléliser les calculs sur les nombres flottants, une compétence cruciale pour le traitement de volumes de données massifs (*Big Data*).
* **Gestion mémoire :** Manipulation directe de structures de données plates en mémoire (tableaux de sommets et de faces sous forme de blocs de mémoire).

## 🛠️ Fonctionnalités implémentées

1. **Rotations 3D :** Application de formules trigonométriques matricielles sur les axes X, Y, Z.
2. **Projection Perspective :** Transformation des points de l'espace 3D (X, Y, Z) en coordonnées planes 2D (X', Y') adaptées à l'écran via le théorème de Thalès.
3. **Calcul des Faces Cachées (Backface Culling) :** Optimisation par produit vectoriel (calcul de la normale) permettant de masquer les polygones invisibles afin de fluidifier le rendu.
