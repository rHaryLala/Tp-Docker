# 🚀 Express Docker App

Une application Node.js basique avec Express, empaquetée et exécutée dans un conteneur Docker.

## 📁 Structure du projet

```
express-docker-app/
├── Dockerfile
├── index.js
├── package.json
└── .dockerignore
```

## 🧰 Prérequis

- [Node.js](https://nodejs.org/)
- [Docker](https://www.docker.com/)
- (Optionnel) [Docker Compose](https://docs.docker.com/compose/)

## ⚙️ Installation & Lancement

### 1. Cloner le projet

```bash
git clone <lien-du-repo>
cd express-docker-app
```

### 2. Construire l'image Docker

```bash
docker build -t tp-docker .
```

### 3. Lancer le conteneur

```bash
docker run -p 3000:3000 tp-docker
```

### 4. Tester l'application

Ouvre ton navigateur à l'adresse :

```
http://localhost:3000
```

Tu devrais voir :

```
Hello Docker + Express!
```

## 📦 Exemple de `index.js`

```js
const express = require('express');
const app = express();
const PORT = process.env.PORT || 3000;

app.get('/', (req, res) => {
  res.send('Hello Docker + Express!');
});

app.listen(PORT, () => {
  console.log(`Server is running on port ${PORT}`);
});
```

---

> Développé par Hary Lala RABENAMANA
