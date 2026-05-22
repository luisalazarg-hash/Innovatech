# Etapa 1: Construcción (Build)
FROM node:18-alpine AS builder
WORKDIR /app
COPY package*.json ./
RUN npm install
COPY . .
RUN npm run build

# Etapa 2: Producción (Servir con Nginx No-Root)
FROM nginxinc/nginx-unprivileged:alpine
# Esta imagen ya viene limpia y con el usuario no-root configurado
COPY --from=builder /app/dist /usr/share/nginx/html

EXPOSE 8080