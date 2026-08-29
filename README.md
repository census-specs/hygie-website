# Hygie — Portail Web Officiel & Guide Pédagogique

[![R Package](https://img.shields.io/badge/R_Package-Hygie-1b365d.svg?logo=r&logoColor=white)](https://github.com/census-specs/hygie)
[![License: MIT](https://img.shields.io/badge/License-MIT-8b1e2d.svg)](LICENSE)
[![GitHub Pages](https://img.shields.io/badge/Deployment-GitHub_Pages-2e7d32.svg?logo=github)](https://census-specs.github.io/hygie/)
[![Bilingual](https://img.shields.io/badge/Language-FR%20%7C%20EN-blue.svg)](#fonctionnalités-clés)
[![Zero Dependency](https://img.shields.io/badge/Dependencies-0%20(Pure%20HTML%2FCSS%2FJS)-005f73.svg)](#architecture-technique)

> **Portail de référence et centre de ressources pour le package R `hygie`**  
> Une application R Shiny conçue pour simplifier l'audit, le nettoyage, le prétraitement et l'analyse exploratoire des données d'enquêtes statistiques, de santé publique et socio-économiques avec génération de code R 100% reproductible.

---

## 📌 Sommaire

- [Aperçu du Projet](#-aperçu-du-projet)
- [Fonctionnalités Clés du Site](#-fonctionnalités-clés-du-site)
- [Architecture & Contenu](#-architecture--contenu)
  - [1. Accueil (Home)](#1-accueil-home)
  - [2. Guide d'utilisation (User Guide)](#2-guide-dutilisation-user-guide)
  - [3. Formation & Cas Pratiques (Training & Use Cases)](#3-formation--cas-pratiques-training--use-cases)
  - [4. À propos (About)](#4-à-propos-about)
- [Installation Rapide du Package R](#-installation-rapide-du-package-r)
- [Déploiement sur GitHub Pages](#-déploiement-sur-github-pages)
- [Structure du Dépôt](#-structure-du-dépôt)
- [Auteur & Crédits](#-auteur--crédits)
- [Licence](#-licence)

---

## 🔬 Aperçu du Projet

Le package R **Hygie** (nommé en hommage à la déesse gréco-romaine de la santé et de la propreté) a été développé pour éliminer les frictions lors du nettoyage et du prétraitement des données tabulaires et d'enquêtes.

Ce site web constitue le **portail officiel d'accueil et d'apprentissage** du projet. Il offre aux chercheurs, statisticiens, data analysts et étudiants un point d'accès unifié pour :
1. **Comprendre et installer** le package `hygie`.
2. **Consulter la documentation** étape par étape.
3. **Se former par la pratique** à travers 5 cas d'usage thématiques avec jeux de données réels téléchargeables, vidéos intégrées et scripts R Tidyverse.

---

## ✨ Fonctionnalités Clés du Site

- 🌐 **Bilinguisme Intégral (Français / Anglais)** : Bascule instantanée de la langue via le sélecteur `FR | EN` dans l'en-tête, avec mémorisation de la préférence dans le `localStorage`.
- 🎓 **Design Académique Haute Précision** : Esthétique soignée inspirée des publications scientifiques *Quarto*, *LaTeX* et du *Journal of Statistical Software* :
  - **Couleurs institutionnelles** : Bleu nuit académique (`#1b365d`), bordeaux classique (`#8b1e2d`), fond texturé doux (`#fcfcfc`).
  - **Typographie rigoureuse** : Titrages à empattements (Serif) pour l'autorité académique et police monospace fine (`SFMono`, `Consolas`) pour le code.
- 🌊 **Arrière-Plan Animé en Filigrane (Canvas)** : Animation JavaScript native et ultra-discrète faisant flotter des symboles mathématiques et du langage R (`∑`, `{}`, `%>%`, `R`, `µ`, `σ`, `f(x)`, `<-`, `β`, `λ`).
- ⚡ **Architecture 100% Autonome (Single File)** : Le site repose sur un fichier `index.html` unique sans framework lourd ni dépendance externe CDN, garantissant un chargement instantané et une portabilité maximale.
- 📋 **Blocs de Code avec Copie en 1 Clic** : Chaque extrait de code R dispose d'un bouton de copie interactif avec retour visuel contextuel (*Copié !* / *Copied!*).
- 📱 **Conception Responsive & Accessible** : Adapté à toutes les résolutions d'écran (mobiles, tablettes, ordinateurs de bureau) avec respect des normes de contraste WCAG AA.

---

## 📑 Architecture & Contenu

Le site est structuré en 4 grands modules accessibles via la barre de navigation :

### 1. Accueil (`Home`)
- **Présentation synthétique** du package et de ses objectifs.
- **Bloc d'installation en 1 ligne** depuis GitHub via `remotes`.
- **4 piliers méthodologiques** :
  - *Sans Code (No Code)* : Interface graphique intuitive pour démocratiser l'analyse.
  - *Reproductible (Reproducible)* : Export automatique des scripts R sous-jacents (Tidyverse).
  - *Multi-formats (Multi-format)* : Support natif CSV, Excel, SAS, SPSS et Stata.
  - *Historique Dynamique (Dynamic History)* : Traçabilité complète de chaque transformation de données.

### 2. Guide d'utilisation (`User Guide`)
- **Workflow en 3 étapes** : Importation & Typage $\rightarrow$ Nettoyage & Filtrage $\rightarrow$ Export & Rapports.
- **Options de lancement avancées** : Configuration du port (`launch.browser = TRUE`, `port = 3838`, `host = "0.0.0.0"`).
- **Format du rapport d'audit** : Structure des exports reproductibles générés par l'outil.

### 3. Formation & Cas Pratiques (`Training & Use Cases`)
Cinq modules thématiques complets comprenant chacun le **téléchargement direct du jeu de données**, un **lecteur vidéo tutoriel** et le **script R Tidyverse documenté** :

| Cas Pratique | Thématique | Jeu de Données | Outils R Démontrés |
| :--- | :--- | :--- | :--- |
| **Cas n°1** | Nettoyage d'une enquête de santé publique | `enquete_sante_2023.csv` | Recodage, valeurs manquantes (`naniar`), doublons |
| **Cas n°2** | Audit des données sociodémographiques | `recensement_extrait.xlsx` | Standardisation des libellés, typage de variables |
| **Cas n°3** | Analyse descriptive & tableaux croisés | `enquete_nutrition.csv` | Statistiques bivariées, exports de tableaux de contingence |
| **Cas n°4** | Détection et traitement des outliers | `mesures_biometriques.csv` | Méthodes IQR, z-score, seuils physiologiques |
| **Cas n°5** | Fusion et harmonisation de tables | `suivi_cohorte_v1.csv` & `v2` | Jointures relationnelles (`left_join`), gestion des doublons |

### 4. À propos (`About`)
- **Vision du projet** et engagements en faveur de la science ouverte et de la reproductibilité.
- **Fiche développeur** : Coordonnées et affiliation de Pierre Valdeze MBOM MBOM.
- **Licence open-source MIT**.

---

## 💻 Installation Rapide du Package R

Pour installer et exécuter l'application **Hygie** dans votre environnement R ou RStudio :

```r
# 1. Installer le gestionnaire de packages distants (si nécessaire)
if (!requireNamespace("remotes", quietly = TRUE)) {
  install.packages("remotes")
}

# 2. Installer le package Hygie depuis GitHub
remotes::install_github("census-specs/hygie")

# 3. Lancer l'application interactive
hygie::run_hygie()
```

---

## 🚀 Déploiement sur GitHub Pages

Le déploiement du site sur GitHub Pages est entièrement automatisé grâce au workflow GitHub Actions inclus dans `.github/workflows/deploy.yml`.

### Procédure de configuration (1 minute) :

1. Accédez à votre dépôt sur GitHub : `https://github.com/census-specs/hygie`.
2. Cliquez sur l'onglet **Settings** (Paramètres).
3. Dans la barre latérale gauche, sélectionnez **Pages** (sous *Code and automation*).
4. Dans la section **Build and deployment** :
   - Sous **Source**, sélectionnez **GitHub Actions**.
5. Effectuez un `git push` sur la branche `main` : le site sera automatiquement déployé à l'adresse :
   ```
   https://census-specs.github.io/hygie/
   ```

---

## 📂 Structure du Dépôt

```plaintext
hygie/
├── .github/
│   └── workflows/
│       └── deploy.yml        # Workflow GitHub Actions pour le déploiement automatique
├── assets/                   # Ressources statiques et médias
├── index.html                # Application web complète (HTML5 / CSS3 / JavaScript ES6)
├── README.md                 # Documentation officielle du site web
├── LICENSE                   # Licence open-source (MIT)
└── package.json              # Métadonnées de build et d'outillage
```

---

## 👤 Auteur & Crédits

- **Conception & Développement** : **Pierre Valdeze MBOM MBOM**
- **Organisation / Projet** : [census-specs](https://github.com/census-specs)
- **Spécialité** : Statistique appliquée, science des données, ingénierie R & Shiny

---

## 📄 Licence

Ce projet est distribué sous licence **MIT**. Vous êtes libre de l'utiliser, l'étudier, le modifier et le redistribuer, à condition de conserver la mention d'auteur originale. Consultez le fichier [LICENSE](LICENSE) pour plus de détails.
