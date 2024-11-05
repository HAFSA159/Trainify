# Trainify - Gestion de Centre de Formation

## Contexte du Projet
Trainify est une API REST développée pour un centre de formation dans le but de digitaliser la gestion de ses formations. Cette application facilite la gestion des apprenants, des formateurs, des formations et des classes. Elle fournit une interface sécurisée et performante pour effectuer les opérations CRUD (Create, Read, Update, Delete) nécessaires.

## Fonctionnalités Principales
- **Gestion des Apprenants** : Inscription, modification, suppression, et affichage.
- **Gestion des Formateurs** : Création, modification, suppression, et affichage.
- **Gestion des Formations** : Planification, modification, suppression, et affichage.
- **Gestion des Classes** : Création, modification, suppression, et affichage.

## Structure des Classes Principales
- **Apprenant** : nom, prénom, email, niveau, formation, classe.
- **Formateur** : nom, prénom, email, spécialité, formation, classe.
- **Classe** : nom, numSalle.
- **Formation** : titre, niveau, prérequis, capacitéMin, capacitéMax, dateDebut, dateFin, formateur, apprenants, statut (PLANIFIÉE, EN_COURS, TERMINÉE, ANNULÉE).

## Architecture du Projet
Le projet est organisé en différentes couches pour favoriser une bonne séparation des responsabilités :
1. **Entités** : Modèles de données avec annotations JPA et validations.
2. **Repositories** : Interfaces qui étendent `JpaRepository` pour l'accès aux données.
3. **Services** : Logique métier de l'application.
4. **Contrôleurs (REST)** : Expose les endpoints de l’API pour les opérations CRUD.
5. **Exceptions** : Gestion des erreurs et exceptions personnalisées.
6. **Utilitaires** : Fonctions et helpers.
7. **Tests** : Tests unitaires et d'intégration.

## Technologies Utilisées
- **Backend** : Spring Boot
- **Gestion des Dépendances** : Maven
- **Bases de Données** :
    - H2 pour le développement et les tests.
    - PostgreSQL pour l’environnement de production.
- **API Documentation** : Swagger
- **Testing** : JUnit et Mockito
- **Code Quality** : JaCoCo pour la couverture du code
- **Logging** : Utilisation de LOGGER
- **Gestion des Branches** : Git et JIRA pour le suivi de projet

## Endpoints REST
- **Apprenants** : CRUD pour la gestion des apprenants.
- **Formateurs** : CRUD pour la gestion des formateurs.
- **Formations** : CRUD pour la planification et gestion des formations.
- **Classes** : CRUD pour l’organisation des classes.

## Configuration des Profils
- **application-dev.properties** : Configuration pour le profil de développement (H2).
- **application-prod.properties** : Configuration pour le profil de production (PostgreSQL).

## Exigences Techniques
- **Java 8** : Utilisation de Java 8 pour le développement avec :
    - Stream API
    - Lambda expressions
    - Java Time API
    - Collection API et HashMaps
    - Optional
- **Annotations Spring** : Utilisation des annotations pour l'inversion de contrôle (IoC) et injection de dépendances (DI).
- **Design Patterns** : Repository et Singleton.
- **Spring Data JPA** : Pour les opérations CRUD avec JpaRepository.
- **Gestion des Exceptions** : Gestion centralisée des erreurs.
- **Annotation Validation** : Utilisation de `@Valid`, `@NotNull`, etc., pour valider les entrées.

## Outils de Développement
- **Lombok** : Pour générer automatiquement des getters/setters.
- **Spring Boot DevTools** : Pour le rechargement automatique lors du développement.
- **SonarLint** : Outil d'analyse de qualité de code.
- **Debugger** : Utilisation d’un débogueur pour l’analyse de l’application.

## Utilisation de l'API
1. Cloner le dépôt Git : `git clone JavaAura/Hafsa_Elmoatassim_Billah_S3B2_Trainify`
2. Configurer les bases de données (H2 pour dev et PostgreSQL).
3. Lancer l'application avec `mvn spring-boot:run`.
4. Tester les endpoints via Postman ou un autre outil similaire.
5. Accéder à la documentation Swagger à l'adresse : `http://localhost:8080/swagger-ui.html`.


