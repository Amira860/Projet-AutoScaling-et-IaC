# Étape 1 : Utiliser une image Node.js pour construire l'application
FROM node:16-alpine AS build
WORKDIR /app
COPY package.json yarn.lock ./
RUN npm install
COPY . .
RUN npm run build

# Étape 2 : Utiliser une image Nginx pour servir les fichiers statiques
FROM nginx:alpine
RUN rm -rf /usr/share/nginx/html/*
COPY --from=build /app/build /usr/share/nginx/html
EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]

