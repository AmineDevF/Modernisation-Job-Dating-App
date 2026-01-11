# Job Dating – Framework PHP MVC Minimaliste

## 📌 Contexte du Projet

Ce projet vise à construire un **framework PHP minimaliste**, inspiré des meilleures pratiques, tout en restant **léger, rapide et facile à utiliser**.  

Il répond aux besoins d'applications modernes avec des dépendances minimales, tout en proposant des fonctionnalités puissantes telles que :

- Gestion des routes
- Intégration avec **Eloquent ORM** **(BONUS)**
- Système de validation des données sécurisé

---

## 🎯 Objectifs du Projet

- Développer une **architecture MVC claire et modulaire**
- Implémenter un **routeur personnalisé** pour gérer les URL de l'application
- Intégration sécurisée avec **Eloquent ORM** pour la gestion des bases de données **(BONUS)**
- Sécuriser l’application contre les attaques :
  - XSS
  - CSRF
  - SQL Injection
- Offrir des outils pratiques :
  - Validation des données
  - Système de sessions
  - Gestion des erreurs
- Séparer fonctionnellement le **Front Office** et le **Back Office**
- Utiliser **Composer** pour l'autoloading des classes

---

## ⚙️ Fonctionnalités Principales

- Gestion avancée des routes
- Connexion à la base de données
- Séparation **Front Office / Back Office**
- Système d’authentification sécurisé avec permissions utilisateurs
- Gestion des rôles et autorisations (**ACL**)
- Protection contre :
  - SQL Injection
  - XSS
  - CSRF
- Classes utilitaires :
  - `Validator`
  - `Security`
  - `Session`
- Autoloading dynamique avec Composer

---

## 🗂️ Structure MVC Proposée

```text
/job_dating
├── public/
│   ├── index.php
│   ├── .htaccess
│   └── assets/
├── app/
│   ├── controllers/
│   │   ├── front/
│   │   └── back/
│   ├── models/
│   ├── views/
│   └── core/
│       ├── Router.php
│       ├── Controller.php
│       ├── Model.php
│       ├── View.php
│       ├── Database.php
│       ├── Auth.php
│       ├── Validator.php
│       ├── Security.php
│       └── Session.php
├── config/
│   ├── config.php
│   └── routes.php
├── logs/ # Bonus
├── vendor/
├── .env
├── composer.json
└── .gitignore

```


---

## ✅ Bonnes Pratiques à Suivre

### 🔹 Séparation stricte des responsabilités

- **Front Office** : partie publique accessible à tous  
- **Back Office** : réservé aux administrateurs authentifiés

---

### 🔹 Sécurisation des données

- Protection CSRF via tokens sécurisés
- Validation des entrées utilisateurs avec `Validator.php`
- Protection contre les attaques **XSS** et **SQL Injection** via `Security.php`

---

### 🔹 Modularité

- Utilisation de classes abstraites pour réutiliser le code
- Intégration facile avec d'autres bases de données
- Code maintenable et évolutif

---

### 🔹 Gestion des sessions et authentification

- Gestion des sessions avec `Session.php`
- Authentification des utilisateurs via `Auth.php`
- Gestion des rôles et permissions

---

### 🔹 Autoloading avec Composer

- Création et gestion automatique des classes via Composer
- Respect des standards PSR
- Gestion centralisée des dépendances

---

## 🚀 Fonctionnalités BONUS

### 🧩 ORM (Eloquent)

- Connexion à la base de données via un ORM
- Modèles héritant d’une classe `Model`
- Aucune requête SQL directe dans les contrôleurs

---

### 🎨 Twig (Template Engine)

- Remplacement des vues PHP par des templates **Twig**
- Héritage de layouts
- Séparation totale :
  - Logique métier
  - Affichage

---

