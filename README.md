## FRAMEWORK SPRING
Cette application est un système de gestion d'utilisateurs 
construit avec Spring Core (sans Spring Boot), 
Spring MVC, et Spring Data JPA. Elle permet aux utilisateurs d'effectuer des opérations CRUD 
comme la création, la consultation, la mise à jour et la suppression d'utilisateurs via une interface web.

## Table des matières
- [Structure du projet](#structure-du-projet)
- [Injection de dépendances (DI)](#injection-de-dépendances-di)
- [Inversion de contrôle (IoC)](#inversion-de-contrôle-ioc)
- [Beans Spring](#beans-spring)
- [Portées des beans](#portées-des-beans)
- [ApplicationContext](#applicationcontext)
- [Scan des composants et annotations](#scan-des-composants-et-annotations)
- [Spring Data JPA](#spring-data-jpa)
- [Spring MVC](#spring-mvc)
- [Installation et configuration](#installation-et-configuration)

### Aperçu du Framework Spring
Spring est un framework puissant pour développer des applications Java, particulièrement des applications web. Il simplifie le développement en fournissant des outils comme l'injection de dépendances, la programmation orientée aspect (AOP), et une architecture flexible, facilitant ainsi la gestion du code et l'amélioration de l'efficacité.

### Structure du projet
```sh
.
├── src/
│   ├── main/
│   │   ├── java/
│   │   │   └── fr/
│   │   │       └── monprojet/
│   │   │           └── web/
│   │   │               ├── controller/
│   │   │               │   └── UtilisateurController.java
│   │   │               ├── entity/
│   │   │               │   └── Utilisateur.java
│   │   │               ├── repository/
│   │   │               │   └── UtilisateurRepository.java
│   │   │               ├── services/
│   │   │               │   └── UtilisateurService.java
│   │   │               └── Main.java
│   │   ├── webapp/
│   │   │   └── WEB-INF/
│   │   │       └── views/
│   │   │           └── utilisateurs.jsp
│   │   │       ├── applicationContext.xml
│   │   │       ├── dispatcher-servlet.xml
│   │   │       └── web.xml
├── pom.xml
└── README.md
```

### Dependency Injection (DI)
Lorsqu’une classe (A) a besoin d’une autre classe (B) pour fonctionner, on dit que (A) a une dépendance vers (B) et que (B) est une dépendance pour (A).
lorsqu’il devient nécessaire de modifier une des classes. En effet, avec le jeu des dépendances, il peut être alors nécessaire de modifier tout ou partie des classes qui dépendent de la classe modifiée.
### Inversion of Control (IoC)
est un processus qui définit les dépendances d'un objet sans avoir à les créer.
Il crée les objets, configure et assemble leurs dépendances, gère l'intégralité de leur cycle de vie. Le conteneur utilise l'injection de dépendances (DI) pour gérer les composants qui composent l'application.
### Spring Beans
Un Bean est un objet qui est instancié, assemblé et géré par Spring IoC Containe
### Bean Scopes

### ApplicationContext

### Component Scanning and Stereotype Annotations

### Spring Data JPA

### Spring MVC

### Installation and Setup
