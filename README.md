# Reto InmoHouse

# InmoHouse - Plataforma Inmobiliaria

Una aplicación web full-stack para la gestión moderna de propiedades, clientes y agentes.

[https://github.com/karentarchb/inmohousebcl](https://www.notion.so/%3Ca%20class=)">**Explorar el código »**

---

### 📝 Sobre el Proyecto

InmoHouse es una solución diseñada para modernizar y optimizar la gestión de una empresa inmobiliaria. El sistema reemplaza los procesos manuales, ofreciendo una plataforma centralizada, eficiente y segura para administrar propiedades, clientes y agentes. La aplicación cuenta con un sistema de roles y permisos que garantiza que cada usuario tenga acceso únicamente a la información y funcionalidades que le corresponden.

---

### ✨ Características Principales

- 
    
    **Autenticación Segura:** Sistema de registro y login basado en Tokens JWT con tiempo de expiración.
    
- 
    
    **Gestión por Roles:** Tres roles predefinidos (Administrador, Agente, Cliente) con permisos específicos.
    
- **Panel de Administración:**
    - Dashboard con estadísticas y gráficos sobre el estado del negocio.
    - Gestión completa (CRUD) de todos los usuarios del sistema.
- **Gestión de Propiedades:**
    - CRUD completo de propiedades para Administradores y Agentes.
    - Visualización de propiedades para Clientes.
- 
    
    **Seguridad en el Backend:** Rutas de API protegidas por middleware que verifica la autenticación y autorización del usuario.
    
- 
    
    **Interfaz Moderna:** Frontend responsivo desarrollado con Angular y Angular Material, enfocado en la usabilidad.
    

---

### 🛠️ Tecnologías Utilizadas

Este proyecto fue construido utilizando un stack de tecnologías moderno y robusto:

| Categoría | Tecnología |
| --- | --- |
| **Frontend** | Angular v17+, Angular Material, Standalone Components |
| **Backend** | Node.js, Express.js |
| **Base de Datos** | PostgreSQL |
| **Autenticación** | JSON Web Tokens (JWT), bcrypt.js |
| **Entorno de Desarrollo** | Docker (para la base de datos) |

Exportar a Hojas de cálculo

---

### 🏗️ Arquitectura y Estructura del Proyecto

El proyecto está organizado en un monorepo con dos carpetas principales: `frontend` y `backend`.

### Estructura del Backend

`/backend
├── /config           # Configuración de la base de datos (db.js)
├── /controllers      # Lógica de negocio (authController, userController, etc.)
├── /middleware       # Middlewares de Express (authMiddleware)
├── /routes           # Definición de las rutas de la API (authRoutes, userRoutes, etc.)
├── .env              # (Local) Archivo con variables de entorno (NO SUBIR A GIT)
├── index.js          # Punto de entrada del servidor Express
└── package.json      # Dependencias y scripts del backend`

### Estructura del Frontend

`/frontend
├── /src
│   ├── /app
│   │   ├── /core         # Lógica central (guards, interceptors)
│   │   ├── /features     # Módulos de funcionalidades (auth, dashboard, properties)
│   │   ├── /shared       # Componentes y servicios compartidos
│   │   └── app.config.ts # Configuración principal de la app
│   └── /assets         # Imágenes, iconos y otros recursos estáticos
├── .env.local        # (Local) Variables de entorno para el frontend
├── angular.json      # Configuración del workspace de Angular
└── package.json      # Dependencias y scripts del frontend`

---

### 🚀 Instalación y Ejecución Local

Sigue estos pasos para configurar y ejecutar el proyecto en tu máquina local.

### **1. Prerrequisitos**

Asegúrate de tener instalados:

- Node.js (v18 o superior)
- Docker Desktop
- Git

### **2. Instalación**

Bash

`# 1. Clona este repositorio
git clone https://github.com/karentarchb/inmohousebcl.git

# 2. Navega a la carpeta del proyecto
cd inmohousebcl`

### **3. Configuración del Backend**

Bash

`# 1. Navega a la carpeta del backend
cd backend

# 2. Instala las dependencias
npm install

# 3. Crea el archivo .env y configúralo (usa el que creamos en nuestro desarrollo)
# El archivo debe contener DB_USER, DB_PASSWORD, DB_DATABASE, DB_HOST, DB_PORT y JWT_SECRET`

### **4. Configuración del Frontend**

Bash

`# 1. Desde la raíz del proyecto, navega a la carpeta del frontend
cd frontend

# 2. Instala las dependencias
npm install`

### **5. Ejecución**

> ℹ️ Nota: Necesitarás 2 o 3 terminales abiertas para ejecutar toda la aplicación.
> 
1. **Iniciar la Base de Datos (Docker):**
En una terminal, desde la **raíz del proyecto**, ejecuta:Bash
    
    `docker compose up -d`
    
2. **Iniciar el Servidor Backend:**
En una segunda terminal, navega a la carpeta `backend` y ejecuta:Bash
    
    `node index.js`
    
    > El backend estará corriendo en http://localhost:3000
    > 
3. **Iniciar la Aplicación Frontend:**
En una tercera terminal, navega a la carpeta `frontend` y ejecuta:Bash
    
    `ng serve -o`
    
    > La aplicación se abrirá en tu navegador en http://localhost:4200
    >
