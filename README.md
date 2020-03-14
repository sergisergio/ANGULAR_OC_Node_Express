# Project Title

Full stack JS

## Basé sur ce

* [Cours](https://openclassrooms.com/fr/courses/6390246-passez-au-full-stack-avec-node-js-express-et-mongodb) - Node.js, Express et MongoDB

### Configurer l'environnement

1) Installer [Node](https://nodejs.org/en/)
2) Installer Angular
```
npm install -g @angular/cli
```
3) Cloner l'application front-end
```
git clone https://github.com/OpenClassrooms-Student-Center/go-fullstack-fr-frontend.git frontend
```
```
cd frontend
npm install
ng serve
```
4) Accéder à [http://localhost:4200](http://localhost:4200)
5) Créer un sous-répertoire pour y créer l'application Express.

### Démarrer le serveur node

- Node est le runtime qui permet d'écrire les tâches côté serveur.
- Express est un framework reposant sur Node et facilite la création et la gestion de serveurs Node.

### Initialiser le projet et démarrer un serveur basique

- Exécuter dans le dossier backend
```
npm init
```
- Cela génère un ficheir package.json
```
git init
```
- inclure un fichier .gitignore contenant la ligne node_modules
- créer un fichier server.js dans le dossier backend.
- importer le package HTTP natif de Node
- démarrer le serveur
```
node server
```
- Accéder à [http://localhost:3000](http://localhost:3000)
- Installer nodemon
```
npm install -g nodemon
```
- Au lieu d'utiliser "node server", on fera "nodemon server".

### Créer une application Express

- dans le dossier backend.
```
npm install --save express
```
- créer un fichier app.js dans lequel on place l'application Express.
- modifier le fichier server.js
- une application Express est une série de fonctions appelées middleware.
- chaque élément de middleware reçoit les objets request et response.
- on crée les routes GET et POST dans le fichier app.js
- ajouter du code pour éviter les erreurs CORS.

### Recevoir des éléments de l'application front-end

```
npm install --save body-parser
```
- cela permet d'extraire l'objet JSON de la demande
- l'importer dans le fichier app.js

### Configurer la BDD

- Accéder au [site Web de MongoDB](https://www.mongodb.com/download-center/community?initial=true)
- s'inscrire
- créer un cluster (option AWS et uniquement les options gratuites)
- onglet Database Access: choisir Read and write to any database
- connecter l'API au cluster MongoDB
```
npm install --save mongoose
```
- importer mongoose dans le fichier app.js et mettre le mot de passe.

### Créer un schéma de données, enregistrer et récupérer

- créer un schéma Thing
- dossier backend: créer un dossier models puis un fichier thing.js
- l'importer dans le fichier app.js
- remplacer la logique de la route POST
- remplacer la logique de la route GET
- mettre en place tout le CRUD

### Optimiser le backend

- configurer le routage (dossier routes)
- configurer les contrôleurs (dossier controllers)

### Préparer la BDD pour les informations d'authentification

- s'assurer que 2 utilisateurs  n'utilisent pas la même adresse mail
```
npm install --save mongoose-unique-validator
```
- créer un modèle utilisateur
- configurer les routes pour l'authentification (controllers/users.js et routes/users.js)
- créer des utilisateurs
```
npm install --save bcrypt
```
- utiliser bcrypt dans la logique métier
- implémenter la fonction login
- créer des tokens d'authentification
```
npm install --save jsonwebtoken
```
- l'importer dans le contrôleur utilisateur
- utiliser ce token dans la fonction login

### Implémenter le middleware d'authentification

- créer un dossier middleware et un fichier auth.js
- cela permet de sécuriser les routes dans notre API.

### Téléchargement de fichiers

- Utilisation de multer
```
npm install --save multer
```
- créer le dossier images dans le dossier backend
- créer le middleware multer-config.js dans le dossier middleware
- modifier la route POST
- modifier la route PUT
- modifier la route DELETE avec le package fs de Node



