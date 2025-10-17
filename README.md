# Evaluación Parcial 2 - DevOps y CI/CD con Node.js y Docker

## Autor

**Nombre:** Carlos Moil Alvarado
**Carrera:** Ingenieria en Informática

## Descripción General

Este proyecto tiene como objetivo configurar un **pipeline de integración y entrega continua (CI/CD)** utilizando **GitHub Actions**, junto con un entorno **Docker Compose** que levanta una aplicación **Node.js**, una base de datos **MySQL** y **phpMyAdmin** para su administración.

El workflow automatiza el proceso de:
1. Instalación de dependencias (`npm install`).
2. Ejecución de tests (`npm test`).
3. Análisis de código con **ESLint**.
4. Análisis de dependencias con **Snyk**.
5. Revisión de calidad de código con **SonarCloud**.
6. Construcción de la imagen Docker.
7. Publicación automática de la imagen en **Docker Hub**.

---

## Estructura del Proyecto

Evaluacion-Parcial-2-Devops
├── .github/
│ └── workflows/
│ └── ci.yml # Workflow de GitHub Actions
├── docker-compose.yml # Configuración para levantar los servicios
├── src/ # Código fuente de la aplicación Node.js
├── package.json
├── README.md
└── CONTRIBUTING.md

## Variables y Secrets necesarios

En el repositorio de GitHub, agrega los siguientes Secrets:

 `DOCKERHUB_USERNAME` = Usuario de Docker Hub
 `DOCKERHUB_TOKEN` = Token de acceso personal de Docker Hub
 `SONAR_TOKEN` = Token de autenticación de SonarCloud
 `SONAR_ORGANIZATION` = Nombre de la organización en SonarCloud
 `SNYK_TOKEN` = Token de autenticación de Snyk


 ## Cómo levantar los contenedores

Desde la raíz del proyecto (donde está `docker-compose.yml`):

### Construir e iniciar en segundo plano
```bash
docker compose up -d --build
```

### Ver estado
```bash
docker ps
docker compose ps

### Detener
```bash
docker compose down
```