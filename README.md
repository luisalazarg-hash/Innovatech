# Innovatech - Sistema de Gestión Microservicios (AWS & Docker)

Este proyecto consiste en una plataforma web para la gestión de **Ventas** y **Despachos** de la empresa Innovatech. La solución está completamente contenerizada utilizando Docker y desplegada de forma persistente en una instancia **AWS EC2**.

---

## 🛠️ Arquitectura y Tecnologías Utilizadas

El sistema está compuesto por 4 contenedores independientes que se comunican a través de una red interna de Docker:

* **Frontend:** Desarrollado en **React** (Puerto `3000`).
* **Backend Ventas:** Microservicio desarrollado en **Java Spring Boot** (Puerto `8081`).
* **Backend Despachos:** Microservicio desarrollado en **Java Spring Boot** (Puerto `8082`).
* **Base de Datos:** Motor **MySQL 8.0** de forma persistente (Puerto `3306`).

---

## 🚀 Despliegue en Producción (AWS)

La aplicación se encuentra actualmente desplegada y corriendo en segundo plano de forma permanente en la siguiente dirección:

* **URL del Sistema:** `http://54.157.110.95:3000`

### Comandos de Gestión Utilizados en el Servidor:

Para levantar y verificar el ecosistema completo en AWS se utilizaron los siguientes comandos:

```bash
# Descargar imágenes y levantar contenedores en segundo plano (Detached)
sudo docker compose up -d

# Verificar el estado de los contenedores activos
sudo docker ps
