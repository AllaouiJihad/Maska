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
Un bean géré par le conteneur possède une portée (scope).

Pour un usage général, Spring propose deux portées :

#### singleton : le conteneur ne peut avoir qu'une seule instance pour un identifiant de bean. Chaque fois qu'une instance du bean sera demandée, c'est cette unique instance qui sera renvoyée par le conteneur
#### prototype : chaque fois qu'une instance du bean sera demandée, le conteneur va créer une nouvelle instance
Spring propose d'autres portées notamment celles dédiées aux applications web (request, session et global-session).

La portée est définie dans le fichier de configuration en utilisant l'attribut scope du tag <bean>. La valeur fournie est celle de la portée souhaitée (singleton ou prototype).

Par défaut, les beans ont une portée singleton : la grande majorité des beans gérés dans un conteneur Spring sont généralement des singletons.


### ApplicationContext
L'application context est une interface permettant d’obtenir différentes informations sur l'application Spring
### Component Scanning and Stereotype Annotations

### Spring Data JPA
Spring Boot Data JPA permettant de créer des requêtes dynamiques avec des combinaisons très fluides.
### Spring MVC
Spring MVC est un framework qui permet d’implémenter des applications selon le design pattern MVC.
### Installation and Setup
