
# Utiliser une image Node.js en tant qu'image de base
FROM node:14-alpine

# Créer et définir le répertoire de travail dans le conteneur
WORKDIR /usr/src/app

# Copier les fichiers de dépendances du projet dans le répertoire de travail
COPY package*.json ./

# Installer les dépendances
RUN npm install

# Copier les fichiers package.json et package-lock.json dans le répertoire de travail
COPY package*.json .
COPY now.json .
COPY apollo.config.js .
COPY Procfile .
COPY .env.example .
COPY store.sqlite .


# Copier les dossiers bin et src dans le répertoire de travail
COPY bin/ ./bin
COPY src/ ./src

# Exposer le port sur lequel votre serveur Node.js s'exécute par défaut
EXPOSE 4000

# Commande pour démarrer votre serveur Node.js
CMD ["npm", "start"]

