# Utilise une version récente de Node.js
FROM node:latest

# Définir le répertoire de travail dans le conteneur
WORKDIR /app

# Copier uniquement package.json et package-lock.json pour optimiser la mise en cache
COPY package*.json ./

# Nettoyer le cache npm et installer les dépendances en contournant les conflits
RUN npm install --force

# Copier le reste des fichiers de l'application
COPY . .


ENV REDIS_URL=redis://redis:6379

# Exposer le port (à adapter selon ton app)
EXPOSE 8080

# Définir la commande de démarrage
CMD ["node", "main.js"]

