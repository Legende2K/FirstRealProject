# Rhymni - Outil de Gestion de Projets

Rhymni est un outil de gestion de projets développé pour une école d'ingénieurs. L'application est divisée en un frontend Svelte et un backend Spring Boot.

## Structure du Projet

Le projet est structuré en deux dossiers principaux :

- `rhymni-back` : Contient le code source pour le backend de l'application.
- `rhymni-front` : Contient le code source pour le frontend de l'application.

## Configuration de l'Environnement

### Backend

Le backend est une application Spring Boot qui utilise Maven comme système de build. Pour configurer l'environnement de développement, vous devez installer Java 11 et Maven.

### Frontend

Le frontend est une application Svelte qui utilise Vite comme outil de build. Pour configurer l'environnement de développement, vous devez installer Node.js et PM2.

## GitHub Actions

Des workflows GitHub Actions sont configurés pour le build, le test, l'analyse et le déploiement des applications frontend et backend.

Chaque partie de l'application a son propre workflow :

- `rhymni-backend-workflow.yml` : Déclenché lors de modifications dans le dossier `rhymni-back`.
- `rhymni-frontend-workflow.yml` : Déclenché lors de modifications dans le dossier `rhymni-front`.

Ces workflows vérifient que le code peut être construit correctement et que tous les tests passent avant de permettre la fusion d'une pull request.

## Déploiement

Le déploiement est géré par les workflows GitHub Actions. L'application est déployée sur un environnement de développement lors d'une pull request sur la branche dev, et sur un environnement de production lors d'une pull request sur la branche main.
