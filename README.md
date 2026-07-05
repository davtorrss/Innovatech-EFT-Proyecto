#  Innovatech Chile - Plataforma Logística y de Ventas (EFT CI/CD & AWS ECS)

Este repositorio contiene la arquitectura de microservicios para la gestión de ventas y despachos de Innovatech Chile, contenerizada con Docker y orquestada en AWS ECS mediante un pipeline CI/CD automatizado con GitHub Actions.

##  Estructura del Sistema
* **Frontend:** Aplicación web desarrollada en Node/React y servida de forma ligera y segura mediante Nginx (Puerto 80).
* **Microservicio Ventas:** API REST en Spring Boot 3 / Java 17 para registro y control de ventas (Puerto 8082 local / 8080 contenedor).
* **Microservicio Despachos:** API REST en Spring Boot 3 / Java 17 para trazabilidad logística (Puerto 8081 local / 8080 contenedor).
* **Base de Datos:** Motor relacional MySQL 8.0 persistido con volúmenes de Docker.

##  Ejecución Local (Docker Compose)
Para levantar todo el entorno localmente, ejecuta en la raíz del proyecto:
```bash
docker-compose up --build -d