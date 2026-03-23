# Authentification en mémoire avec Spring Security

Ce projet est une application **Spring Boot** permettant de mettre en place une **authentification en mémoire** avec Spring Security.  
L'application protège les routes selon les rôles des utilisateurs et propose un formulaire de connexion personnalisé avec **Thymeleaf**.

Le projet utilise plusieurs technologies du framework Spring :

- **Spring Web** pour créer les endpoints REST
- **Spring Security** pour l'authentification et le contrôle d'accès
- **Thymeleaf** pour le rendu des vues HTML côté serveur

---

# 📌 Objectif du TP

À travers ce projet, j'ai appris à :

- Générer un projet **Spring Boot avec Spring Initializr**
- Comprendre le modèle d'**authentification de Spring Security**
- Créer des utilisateurs et rôles **statiques en mémoire**
- Restreindre l'accès à certaines pages selon les **rôles**
- Personnaliser la **page de connexion** avec Thymeleaf

---

# 🛠️ Technologies utilisées

- Java 17
- Spring Boot 3.x
- Spring Web
- Spring Security 
- Thymeleaf
- Maven

---

## 1️⃣ Création du projet Spring Boot

Création du projet avec **Spring Initializr** en sélectionnant les dépendances nécessaires :

- Spring Web
- Spring Security
- Thymeleaf

Le projet généré suit la structure standard d'une application **Spring Boot avec Maven**.

---

## 2️⃣ Configuration par défaut de Spring Security

Au premier lancement sans configuration, Spring Security protège toutes les routes et génère un utilisateur par défaut visible dans la console :
```apacheUsing generated security password: 2a3c41d7-8c5b-4d5a-a145-5e6f8c9fbd14```

Cela montre que sans configuration explicite, **toutes les routes sont protégées** par défaut.

---

## 3️⃣ Configuration personnalisée – SecurityConfig

Création de la classe `SecurityConfig` dans le package `ma.fstg.security.config`.

---

## 4️⃣ Création du contrôleur

Création de la classe `HomeController` dans le package `ma.fstg.security.web`.

--- 

## 5️⃣ Page de connexion personnalisée

Création du fichier `login.html` dans `src/main/resources/templates/`.

---

## 6️⃣ Lancement de l'application

Depuis l'IDE :
Run SpringSecurityDemoApplication

Une fois démarrée, l'application écoute sur le port : http://localhost:8080

---

## 7️⃣ Tests et validation

### 1️⃣ Connexion avec le compte `user`



---

### 2️⃣ Connexion avec le compte `admin`



---

### 3️⃣ Accès au tableau de bord utilisateur `/user/dashboard`



---

### 4️⃣ Accès au tableau de bord administrateur `/admin/dashboard`



---

### 5️⃣ Accès refusé à `/admin/dashboard` depuis le compte `user`


---

# 👩‍💻 Auteur

- Nom : *[Ton nom]*
- Filière : *[Ta filière]* Sonnet 4.6
