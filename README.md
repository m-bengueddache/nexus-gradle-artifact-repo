# Nexus Artifact Repository — Gradle

> **FR** — Déploiement de Sonatype Nexus et intégration avec un projet Spring Boot Gradle pour publier des artefacts JAR dans un dépôt Maven snapshots privé. Interaction avec l'API REST Nexus.
>
> **EN** — Deployment of Sonatype Nexus and integration with a Spring Boot Gradle project to publish JAR artifacts to a private Maven snapshots repository. Interaction with the Nexus REST API.

---

## Stack

![Java](https://img.shields.io/badge/Java-17-blue?logo=openjdk)
![Spring Boot](https://img.shields.io/badge/Spring%20Boot-3-green?logo=springboot)
![Gradle](https://img.shields.io/badge/Gradle-9-02303A?logo=gradle)
![Nexus](https://img.shields.io/badge/Sonatype-Nexus-1B1C30)
![Docker](https://img.shields.io/badge/Docker-Nexus%20host-blue?logo=docker)

---

## FR — Description

Ce projet couvre la mise en place d'un gestionnaire d'artefacts privé avec Sonatype Nexus et son intégration avec Gradle.

**Ce qui a été réalisé :**
- Déploiement de Nexus sur un serveur cloud via Docker
- Création d'un dépôt Maven snapshots dans l'interface Nexus
- Création d'un utilisateur dédié avec les droits de publication
- Plugin `maven-publish` configuré dans `build.gradle`
- Credentials stockées dans `gradle.properties` (hors versioning en production)
- Publication vers Nexus avec `./gradlew publish`
- Interaction avec l'API REST Nexus (liste et téléchargement d'artefacts)

## EN — Description

This project covers setting up a private artifact manager with Sonatype Nexus and its integration with Gradle.

**What was done:**
- Deployed Nexus on a cloud server via Docker
- Created a Maven snapshots repository in the Nexus UI
- Created a dedicated user with publish rights
- Configured the `maven-publish` plugin in `build.gradle`
- Credentials stored in `gradle.properties` (not versioned in production)
- Publishing to Nexus with `./gradlew publish`
- Interacting with the Nexus REST API (listing and downloading artifacts)

---

## Project Structure

```
.
├── build.gradle        # Gradle build with maven-publish plugin
├── gradle.properties   # Nexus credentials (replace with your values)
├── settings.gradle
└── src/                # Spring Boot application (Java 17)
```
