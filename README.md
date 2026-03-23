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

<img width="1652" height="582" alt="userLogin" src="https://github.com/user-attachments/assets/61cc5aac-9693-4c13-b333-e6cdc10e3cc5" />

<img width="510" height="168" alt="connexion" src="https://github.com/user-attachments/assets/73ad6540-32d7-4155-9845-721389013202" />

---

### 2️⃣ Connexion avec le compte `admin`

<img width="1628" height="593" alt="adminLogin" src="https://github.com/user-attachments/assets/c4f19432-47a4-4995-bc20-f67f37c62519" />

<img width="510" height="168" alt="connexion" src="https://github.com/user-attachments/assets/60c17a9c-96c2-4602-ad1e-3c2c7706f952" />

---

### 3️⃣ Accès au tableau de bord utilisateur `/user/dashboard`

<img width="647" height="162" alt="userDash" src="https://github.com/user-attachments/assets/2d2d59be-b89a-4711-9fe2-c6a64e72814d" />


---

### 4️⃣ Accès au tableau de bord administrateur `/admin/dashboard`

<img width="535" height="152" alt="adminDash" src="https://github.com/user-attachments/assets/5b887a09-1803-4895-b4c9-17a562071b53" />


---

### 5️⃣ Accès refusé à `/admin/dashboard` depuis le compte `user`

<img width="746" height="292" alt="accesUserAdmin" src="https://github.com/user-attachments/assets/28efe7a9-470a-43ea-8ab5-48bbc9764e46" />

---

# 👩‍💻 Auteur

- Nom : Malak El Mallouky
- Filière : SIR
