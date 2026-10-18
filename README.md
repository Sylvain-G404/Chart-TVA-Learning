# 📊 Laboratoire d'Apprentissage : Graphiques Dynamiques avec Chart.js

Ce dépôt est un espace d'expérimentation personnel dédié à l'apprentissage du développement frontend et à la manipulation de données visuelles.
L'objectif principal est de s'entraîner à concevoir un tableau de bord interactif, fluide et responsive en utilisant des technologies web standards, sans framework lourd.

Le projet sert de cas pratique pour maîtriser la superposition de courbes, la gestion des échelles complexes (valeurs unitaires vs données de masse) et l'intégration de plugins de rendu.

---

## 🛠️ Concepts Techniques Étudiés

Ce projet a permis de mettre en pratique et de valider plusieurs compétences clés en développement web :

### 1. Intégration et Configuration de Chart.js

- **Multi-datasets :** Manipulation et superposition de 3 courbes distinctes sur un même repère avec des styles de lignes (pleines, transparentes) et des puces personnalisées.
- **Gestion des arrière-plans :** Inversion des zones de remplissage (`fill: true/false`) sous les courbes pour isoler visuellement des plafonds ou des zones de données.
- **Ajustement des repères :** Utilisation de l'option `offset: true` sur l'axe X pour décoller les points des bords du graphique et éviter la superposition avec l'axe Y.

### 2. Rendu de Texte Fixe (Plugin ChartDataLabels)

- **Affichage chirurgical :** Configuration du plugin `chartjs-plugin-datalabels` pour forcer l'affichage de valeurs textuelles brutes au-dessus des nœuds d'une courbe spécifique, tout en masquant les autres pour garder le visuel propre.
- **Formatage dynamique :** Utilisation de fonctions `formatter` personnalisées couplées à `.toLocaleString()` pour injecter dynamiquement des devises (`€`) ou des modificateurs d'échelle (`Md€`).

### 3. Logique JavaScript et Manipulation de Tableaux

- **Automatisation des calculs :** Utilisation de la fonction `.map()` pour générer instantanément des suites de données cumulées sur 25 ans à partir de variables de base.
- **Changement d'échelle mathématique :** Programmation de fonctions de conversion pour transformer des données brutes en milliards de manière fluide (`/ 1 000 000 000` avec arrondi `.toFixed(2)`).

### 4. Structure HTML5 & CSS3 Moderne

- **Mise en page Grid :** Alignement automatique des blocs de graphiques côte à côte sur écran large, se transformant en liste verticale sur mobile (`@media` queries).
- **Effets avancés :** Utilisation de `border-image` combiné avec un dégradé `linear-gradient` pour créer une ligne de transition colorée entre les sections.

---

## 📦 Structure du Projet

Les données injectées dans les graphiques (simulations budgétaires individuelles et multiplicateurs fictifs à grande échelle) ne servent que de support d'entraînement pour tester la résistance du code face aux grands nombres :

- **Volet d'entraînement 1 :** Simulation de cumul linéaire avec variables d'ajustement.
- **Volet d'entraînement 2 :** Simulation de superposition de trois paliers interconnectés (mécanique de flux).
- **Volet d'entraînement 3 :** Simulation de répartition proportionnelle annuelle sous forme de graphique en anneau (Doughnut).

---

## 🚀 Lancement Local

1. Télécharge ou clone ce dépôt.
2. Ouvre directement le fichier `index.html` dans ton navigateur pour observer le comportement des scripts et le rendu des animations.
