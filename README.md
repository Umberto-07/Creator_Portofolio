# Creator Portfolio

**Creator Portfolio** est une application web conçue pour aider les créateurs, développeurs, designers et autres professionnels à créer et présenter leur portfolio en ligne.

La plateforme vise à offrir une manière simple et structurée de créer un portfolio professionnel en permettant aux utilisateurs de gérer leurs informations personnelles, leurs compétences, leurs projets, leur formation, leur expérience et les autres éléments pertinents de leur profil.

---

## Présentation

Créer un portfolio professionnel peut demander du temps et des connaissances techniques. Creator Portfolio vise à simplifier ce processus en proposant une interface intuitive permettant aux utilisateurs de renseigner leurs informations et de construire leur portfolio sans avoir à créer manuellement chaque page.

L'application est développée progressivement, en commençant par l'interface frontend puis en évoluant vers une application web complète avec un backend Python/Flask et une intégration avec une base de données.

---

## Fonctionnalités principales

Creator Portfolio est conçu pour proposer les fonctionnalités suivantes :

* Inscription et authentification des utilisateurs
* Gestion du profil utilisateur
* Gestion des informations personnelles
* Gestion des compétences
* Gestion des projets
* Gestion de la formation et de l'expérience
* Création et personnalisation du portfolio
* Prévisualisation du portfolio
* Génération du portfolio
* Partage du portfolio
* Interface adaptée aux différentes tailles d'écran

---

## Structure du projet

Le projet est organisé selon une architecture frontend/backend destinée à évoluer au fur et à mesure de l'ajout de nouvelles fonctionnalités.

```text
Creator_Portfolio/
│
├── app.py
├── requirements.txt
├── README.md
├── .gitignore
│
├── templates/
│   ├── index.html
│   ├── connexion.html
│   ├── inscription.html
│   ├── creer_portfolio.html
│   ├── informations.html
│   ├── generation.html
│   ├── profil.html
│   ├── projets.html
│   ├── competences.html
│   └── portfolio.html
│
├── static/
│   ├── css/
│   │   ├── style.css
│   │   ├── connexion.css
│   │   ├── inscription.css
│   │   ├── creer_portfolio.css
│   │   ├── informations.css
│   │   ├── generation.css
│   │   ├── profil.css
│   │   ├── projets.css
│   │   ├── competences.css
│   │   └── portfolio.css
│   │
│   ├── js/
│   │   ├── main.js
│   │   ├── connexion.js
│   │   ├── inscription.js
│   │   ├── creer_portfolio.js
│   │   ├── generation.js
│   │   └── portfolio.js
│   │
│   └── images/
│
├── database/
│   ├── database.db
│   └── schema.sql
│
├── models/
│   ├── user.py
│   ├── portfolio.py
│   ├── projet.py
│   └── competence.py
│
└── routes/
    ├── auth.py
    ├── user.py
    ├── portfolio.py
    └── projets.py
```

> Cette structure représente l'architecture prévue de l'application. Les fichiers et dossiers seront ajoutés progressivement au cours du développement.

---

## Frontend

Le frontend est responsable de l'interface utilisateur et des interactions avec la plateforme.

### HTML

Le dossier `templates/` contient les différentes pages HTML de l'application.

Les principales pages comprennent :

* `index.html` — Page d'accueil
* `connexion.html` — Page de connexion
* `inscription.html` — Page d'inscription
* `creer_portfolio.html` — Interface de création du portfolio
* `informations.html` — Informations personnelles
* `generation.html` — Génération du portfolio
* `profil.html` — Profil utilisateur
* `projets.html` — Gestion des projets
* `competences.html` — Gestion des compétences
* `portfolio.html` — Portfolio généré

### CSS

Le dossier `static/css/` contient les feuilles de style responsables de l'apparence de l'application.

Les feuilles de style sont séparées en fonction des différentes pages et composants afin de conserver un projet organisé et facilement maintenable.

### JavaScript

Le dossier `static/js/` contient la logique JavaScript nécessaire aux fonctionnalités interactives telles que :

* Validation des formulaires
* Gestion dynamique du contenu
* Personnalisation du portfolio
* Gestion des projets
* Gestion des compétences
* Prévisualisation du portfolio

---

## Backend

Le backend sera développé avec **Python et Flask**.

Il permettra de gérer la logique de l'application, les routes, l'authentification, le traitement des données et la communication avec la base de données.

Les principaux composants du backend seront les suivants :

### `app.py`

Le point d'entrée principal de l'application Flask.

Il sera notamment responsable de :

* Initialiser l'application Flask
* Configurer l'application
* Enregistrer les routes
* Connecter les différents composants du backend
* Lancer le serveur de développement

### `routes/`

Ce dossier contiendra les différentes routes de l'application.

* `auth.py` — Authentification et gestion des comptes
* `user.py` — Opérations liées aux utilisateurs
* `portfolio.py` — Gestion des portfolios
* `projets.py` — Gestion des projets

### `models/`

Ce dossier contiendra les modèles de données de l'application.

* `user.py` — Modèle utilisateur
* `portfolio.py` — Modèle portfolio
* `projet.py` — Modèle projet
* `competence.py` — Modèle compétence

---

## Base de données

Une base de données sera utilisée pour stocker et gérer les données de l'application.

La base de données devrait notamment contenir les informations suivantes.

### Utilisateurs

* Identifiant utilisateur
* Nom
* Adresse e-mail
* Mot de passe
* Informations personnelles

### Portfolios

* Identifiant du portfolio
* Identifiant de l'utilisateur
* Titre
* Description
* Présentation
* Informations de contact
* Liens vers les réseaux sociaux

### Projets

* Identifiant du projet
* Identifiant du portfolio
* Nom du projet
* Description
* Technologies utilisées
* Image du projet
* Lien du projet

### Compétences

* Identifiant de la compétence
* Identifiant du portfolio
* Nom de la compétence
* Catégorie
* Niveau

La structure de la base de données évoluera au fur et à mesure de l'implémentation du backend.

---

## Authentification

Le système d'authentification permettra aux utilisateurs de :

1. Créer un compte
2. Se connecter
3. Accéder à leur espace personnel
4. Gérer leurs informations
5. Gérer leur portfolio
6. Se déconnecter

L'authentification et les données des utilisateurs seront gérées par le backend avec Flask.

---

## Création du portfolio

Les utilisateurs pourront créer leur portfolio en renseignant différentes informations telles que :

* Informations personnelles
* Présentation
* Compétences
* Projets
* Formation
* Expérience professionnelle
* Informations de contact
* Liens externes

Les informations saisies par l'utilisateur seront ensuite enregistrées dans la base de données et utilisées pour générer le portfolio.

---

## Prévisualisation et génération du portfolio

Avant de finaliser leur portfolio, les utilisateurs pourront prévisualiser le résultat et vérifier les informations saisies.

Le système de génération permettra ensuite d'organiser les informations de l'utilisateur afin de produire un portfolio complet.

L'objectif à terme est de permettre aux utilisateurs d'obtenir un portfolio professionnel sans avoir à construire manuellement l'intégralité du site.

---

## Technologies

| Technologie | Utilisation                        |
| ----------- | ---------------------------------- |
| HTML5       | Structure des pages web            |
| CSS3        | Mise en forme et design responsive |
| JavaScript  | Interactivité frontend             |
| Python      | Développement backend              |
| Flask       | Framework web                      |
| SQL         | Gestion de la base de données      |
| Git         | Gestion des versions               |
| GitHub      | Hébergement du code source         |

---

## Installation

### Cloner le dépôt

```bash
git clone URL_DU_REPOSITORY
```

### Accéder au projet

```bash
cd Creator_Portfolio
```

### Créer un environnement virtuel

```bash
python -m venv venv
```

### Activer l'environnement virtuel

Sous Windows :

```bash
venv\Scripts\activate
```

### Installer les dépendances

```bash
pip install -r requirements.txt
```

### Lancer l'application

```bash
python app.py
```

L'application sera ensuite accessible à l'adresse locale indiquée par Flask.

---

## Feuille de route

### Frontend

* Page d'accueil
* Page de connexion
* Page d'inscription
* Interface de création du portfolio
* Page d'informations
* Interface de génération du portfolio
* Prévisualisation du portfolio

### Backend

* Mise en place de l'application Flask
* Création des routes
* Gestion des formulaires
* Connexion frontend/backend
* Système d'authentification
* Gestion des utilisateurs

### Base de données

* Mise en place de la base de données
* Gestion des utilisateurs
* Gestion des portfolios
* Gestion des projets
* Gestion des compétences

### Finalisation

* Tests
* Correction des bugs
* Design responsive
* Amélioration des performances
* Amélioration de la sécurité
* Déploiement

---

## État du projet

**Creator Portfolio est actuellement en cours de développement.**

Les premières pages frontend, notamment les pages **Accueil**, **Connexion** et **Inscription**, ont été réalisées en HTML.

Les prochaines étapes du développement consistent à connecter le frontend à Flask, mettre en place le backend, intégrer la base de données et ajouter progressivement les fonctionnalités de gestion du portfolio.

---

## Auteur

**Creator Portfolio**

Projet de développement web réalisé pour l'apprentissage (Personnel)
