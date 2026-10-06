# 🔐 Proyecto: User Management API (FastAPI)

![Banner Proyectos](https://github.com/user-attachments/assets/94ecebe4-ceba-47ae-8f3c-af14bdfe8606)

## 📋 Planteamiento

Formas parte del equipo de backend de una startup que está lanzando varios productos digitales (una plataforma de cursos, una app de reservas y un marketplace). Todos ellos necesitan lo mismo: registrar usuarios, autenticarlos de forma segura y controlar qué puede hacer cada uno.

En lugar de reimplementar esta lógica en cada producto, el CTO ha decidido construir un **servicio centralizado de gestión de usuarios** que el resto de aplicaciones consumirán a través de una API REST. Tu equipo es el responsable de diseñarlo, desarrollarlo y documentarlo.

## 🎯 Objetivo

Desarrollar una API REST con **FastAPI** que permita gestionar usuarios (alta, consulta, edición y baja) con **autenticación basada en JWT** y **documentación interactiva con Swagger (OpenAPI)**, de forma que cualquier equipo pueda integrarse con ella sin necesidad de leer el código.

## 🛠️ Requisitos Técnicos

1. API REST desarrollada con **FastAPI**
2. Base de datos SQL (PostgreSQL, MySQL, SQLite) gestionada con un ORM (SQLAlchemy, SQLModel, etc.)
3. Validación de datos con **Pydantic**
4. Contraseñas almacenadas con hash (bcrypt, argon2…), **nunca en texto plano**
5. Autenticación con **JWT** (OAuth2 Password Flow)
6. Documentación automática con **Swagger UI** (`/docs`) y ReDoc (`/redoc`)
7. Tests unitarios y de integración (pytest + `TestClient`)
8. Control de versiones con Git y GitHub
9. Gestión del proyecto con metodologías ágiles (SCRUM)

## 📦 Entregables

1. Diagrama ER de la base de datos
2. Repositorio en GitHub con código fuente y README con instrucciones de instalación y uso
3. Documentación de la API accesible en Swagger, con ejemplos de peticiones y respuestas
4. Colección de Postman/Bruno o similar con los endpoints
5. Suite de tests completa y pasando
6. Documento de retrospectiva del proyecto
7. Tablero Kanban (Trello, Jira, GitHub Projects, etc.) con historias de usuario

## 🏆 Niveles de Entrega

### 🟢 Nivel Esencial

- Modelo `User` (id, nombre, email único, contraseña hasheada, fecha de creación, activo)
- CRUD completo de usuarios (`POST`, `GET`, `PUT/PATCH`, `DELETE`)
- Registro (`/auth/register`) y login (`/auth/login`) que devuelve un JWT
- Endpoints protegidos que requieren token válido (ej. `/users/me`)
- Schemas Pydantic separados para entrada y salida (la contraseña nunca se devuelve)
- Swagger funcionando con el botón **Authorize**
- Tests unitarios para cada endpoint
- Variables de entorno para datos sensibles (`SECRET_KEY`, URL de la BBDD…)
- Logging básico y manejo de excepciones con códigos HTTP apropiados (400, 401, 403, 404, 409…)
- Gestión de proyecto con Kanban

### 🟡 Nivel Medio

- Roles de usuario (`admin`, `user`) y permisos: solo un admin puede listar o borrar a otros usuarios
- Cambio de contraseña y actualización del propio perfil
- Filtrado, búsqueda y paginación en `GET /users`
- Expiración del token configurable
- Migraciones de base de datos con **Alembic**
- Documentación Swagger enriquecida (tags, descripciones, ejemplos, respuestas de error)
- Arquitectura por capas (routers, services, repositories, schemas)

### 🟠 Nivel Avanzado

- **Refresh tokens** y logout (lista de tokens revocados)
- Verificación de email y recuperación de contraseña mediante token temporal
- Rate limiting en el endpoint de login para mitigar ataques de fuerza bruta
- Soft delete y auditoría (quién creó/modificó cada usuario y cuándo)
- Cobertura de tests ≥ 80 %
- Pipeline de CI con GitHub Actions (lint + tests en cada PR)

### 🔴 Nivel Experto

- Contenedorización con **Docker** y `docker-compose` (API + base de datos)
- Despliegue en la nube (Render, Railway, AWS, Google Cloud, etc.)
- Login social con OAuth2 (Google, GitHub…)
- Autenticación en dos pasos (2FA / TOTP)
- Interfaz de usuario básica (web o móvil) que consuma la API

## 🌟 Competencias:
- Diseñar y gestionar bases de datos
- Diseñar el back-end de aplicaciones
- Implementar mecanismos de autenticación y seguridad
- Implementar tests de calidad
- Gestionar equipos técnicos
- Configurar y automatizar su entorno de trabajo
