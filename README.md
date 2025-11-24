# TP 8 : Authentification en mémoire avec Spring Security

##  Description
Ce TP consiste à implémenter un système d'authentification en mémoire utilisant Spring Security, avec gestion des rôles et restrictions d'accès.

##  Objectifs
- Découvrir le fonctionnement fondamental de Spring Security
- Configurer une authentification en mémoire
- Créer des utilisateurs et rôles statiques
- Restreindre l'accès aux pages selon les rôles
- Personnaliser les pages de connexion et d'erreur

##  Technologies utilisées
- **Spring Boot 3.3.2**
- **Spring Security 6.3.1**
- **Thymeleaf** (templating)
- **Maven** (gestion des dépendances)
- **Java 21**

##  Structure du projet
```
spring-security-tp/
│
├── pom.xml
├── README.md
│
├── src/
│   ├── main/
│   │   ├── java/
│   │   │   └── ma/
│   │   │       └── fstg/
│   │   │           └── security/
│   │   │               │   SpringSecurityDemoApplication.java
│   │   │               │
│   │   │               ├── config/
│   │   │               │       SecurityConfig.java
│   │   │               │
│   │   │               └── web/
│   │   │                       HomeController.java
│   │   │
│   │   └── resources/
│   │       ├── application.properties
│   │       │
│   │       └── templates/
│   │               admin-dashboard.html
│   │               error-403.html
│   │               home.html
│   │               login.html
│   │               user-dashboard.html
│   │
│   └── test/
│       └── java/
│
└── target/
    ├── classes/
    │   ├── ma/
    │   │   └── fstg/
    │   │       └── security/
    │   │           │   SpringSecurityDemoApplication.class
    │   │           │
    │   │           ├── config/
    │   │           │       SecurityConfig.class
    │   │           │
    │   │           └── web/
    │   │                   HomeController.class
    │   │
    │   └── templates/
    │           admin-dashboard.html
    │           error-403.html
    │           home.html
    │           login.html
    │           user-dashboard.html
    │
    └── generated-sources/
        └── annotations/


```
##  Tests de fonctionnement

### Scénario 1 : Utilisateur standard
1. Se connecter avec \`user/1111\`
2. Accéder à \`/user/dashboard\` →  **Accès autorisé**
3. Tenter d'accéder à \`/admin/dashboard\` →  **Erreur 403**

### Scénario 2 : Administrateur
1. Se connecter avec \`admin/1234\`
2. Accéder à \`/admin/dashboard\` →  **Accès autorisé**
3. Accéder à \`/user/dashboard\` →  **Accès autorisé**

### Scénario 3 : Déconnexion
- Cliquer sur \"Déconnexion\" →  **Redirection vers login**



##  Bonnes pratiques respectées

- Séparation des couches (config, web, templates)
- Configuration centralisée de la sécurité
- Pages d'erreur personnalisées
- Interface utilisateur responsive
- Code clair et commenté

## Démonstration



https://github.com/user-attachments/assets/b3daf66e-7073-4442-a9d2-b2758eccf876


## Encadrement & Auteur
**Réalisée par**: BENZIAT hana
<br>
**Encadré par**: Mr.LACHGAR mohammed

