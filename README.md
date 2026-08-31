# Hygie — Site officiel et ressources pédagogiques

[![R Package](https://img.shields.io/badge/R_Package-Hygie-1b365d.svg?logo=r&logoColor=white)](https://github.com/census-specs/hygie)
[![License: MIT](https://img.shields.io/badge/License-MIT-8b1e2d.svg)](LICENSE)
[![GitHub Pages](https://img.shields.io/badge/Deployment-GitHub_Pages-2e7d32.svg?logo=github)](https://census-specs.github.io/hygie/)

> **Hygie** est une application R Shiny de préparation, nettoyage, inspection et transformation des données avec une interface graphique et un pipeline reproductible.

## Le projet

Hygie aide à passer d'un fichier brut à un jeu de données prêt pour l'analyse, sans imposer l'écriture immédiate de toutes les commandes R.

Le projet met l'accent sur trois idées :

- **Comprendre** : inspecter la structure et la qualité des données avant de les modifier.
- **Transformer** : réaliser les opérations de nettoyage et de préparation étape par étape.
- **Reproduire** : conserver l'historique, générer le code R et sauvegarder le travail dans un projet `.hygie`.

## Fonctionnalités récentes

### Inspection de la qualité

Hygie permet d'inspecter directement le jeu de données pour repérer :

- les valeurs manquantes ;
- les valeurs potentiellement aberrantes ;
- les doublons ;
- les lignes concernées par ces problèmes.

Pour les variables numériques, l'inspection des valeurs aberrantes s'appuie sur un boxplot et la règle IQR × 1,5. L'utilisateur peut examiner les observations concernées avant de décider quoi faire.

### Pipeline et reproductibilité

Les opérations effectuées dans l'interface sont enregistrées dans un pipeline. Le code R correspondant peut être récupéré afin de poursuivre le travail dans R ou RStudio.

L'objectif est que l'interface soit un **pont vers R**, et non une boîte noire.

### Projets `.hygie`

Un travail peut être sauvegardé dans un fichier `.hygie` puis rouvert pour retrouver le jeu de données et les étapes du pipeline.

## Installation et lancement

Depuis R ou RStudio :

```r
if (!requireNamespace("remotes", quietly = TRUE)) {
  install.packages("remotes")
}

remotes::install_github("census-specs/hygie")
```

Puis :

```r
library(hygie)
hygie()
```

> **Important :** la fonction de lancement publique est `hygie()`. Le site et la documentation doivent utiliser cette commande.

## Formation

Une page pédagogique dédiée est disponible dans le dépôt :

**[Formation Hygie — `formation.html`](formation.html)**

Elle propose un parcours court pour comprendre :

1. pourquoi inspecter les données avant de les nettoyer ;
2. comment importer et découvrir un jeu de données ;
3. comment interpréter les valeurs manquantes, doublons et aberrantes ;
4. comment construire un pipeline de transformations ;
5. comment comprendre le boxplot et la règle IQR ;
6. comment sauvegarder un projet `.hygie` ;
7. comment passer progressivement de l'interface au code R.

La formation est volontairement orientée **compréhension + pratique**, plutôt qu'une simple liste de fonctionnalités.

## Site web

Le site est volontairement léger : HTML, CSS et JavaScript natifs, sans framework lourd ni dépendance CDN. Il propose notamment :

- une présentation du projet ;
- un guide d'utilisation ;
- des cas pratiques ;
- des exemples de code R copiables ;
- une page de formation ;
- une présentation du projet et de son auteur ;
- un mode clair/sombre et une version française/anglaise.

## Développement

Le dépôt du site est :

https://github.com/census-specs/hygie-website

Le code de l'application R est :

https://github.com/census-specs/hygie

Le site est déployé sur GitHub Pages via GitHub Actions.

## Structure

```text
hygie-website/
├── .github/workflows/deploy.yml
├── Images/
│   ├── auteur.png
│   ├── hygie-import-donnees.png
│   ├── hygie-interface-principale.png
│   └── hygie-transformation.png
├── formation.html
├── index.html
├── README.md
└── LICENSE
```

## Auteur

**Pierre Valdeze MBOM MBOM**  
Ingénieur agro-statisticien · Développeur d'outils pour les données

GitHub : https://github.com/census-specs  
WhatsApp : +237 698 38 90 30  
Email : pierrembom@outlook.com

## Licence

Le projet est distribué sous licence MIT. Voir [LICENSE](LICENSE).
