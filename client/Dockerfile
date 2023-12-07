
# Étape de production, serveur Nginx
FROM nginx:alpine

# Copie des fichiers de build de l'étape de construction vers le répertoire de Nginx
COPY ./build /usr/share/nginx/html

COPY nginx.conf /etc/nginx/conf.d/default.conf



# Exposez le port 80 pour que l'application soit accessible
EXPOSE 8080

# Commande pour démarrer Nginx
CMD ["nginx", "-g", "daemon off;"]
