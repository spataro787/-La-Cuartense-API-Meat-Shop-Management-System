# 🥩 La Cuartense API — Meat Shop Management System

![Node.js](https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white)
![Express](https://img.shields.io/badge/Express-000000?style=for-the-badge&logo=express&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white)
![Swagger](https://img.shields.io/badge/Swagger-85EA2D?style=for-the-badge&logo=swagger&logoColor=black)
![Vitest](https://img.shields.io/badge/Vitest-6E9F18?style=for-the-badge&logo=vitest&logoColor=white)

API RESTful backend desarrollada para **Carnicería La Cuartense**, orientada a la gestión integral de productos cárnicos, cortes, listas de precios y control de stock.

El sistema permite administrar el catálogo de productos, organizar la información comercial y gestionar el inventario mediante una base de datos relacional PostgreSQL.

Implementa una arquitectura por capas, consultas SQL parametrizadas, validación de datos, documentación interactiva con OpenAPI/Swagger y pruebas automatizadas de integración.

## 📌 Funcionalidades principales

- **Gestión de productos cárnicos:** operaciones CRUD para administrar cortes de carne y productos del catálogo.
- **Gestión de precios:** administración de precios de los productos para mantener actualizada la información comercial.
- **Control de stock:** gestión del inventario y disponibilidad de productos.
- **Persistencia relacional:** almacenamiento y organización de datos mediante PostgreSQL.
- **Seguridad de datos:** consultas SQL parametrizadas para prevenir inyecciones SQL.
- **Validación de entradas:** control y validación de datos recibidos mediante `express-validator`.
- **Documentación interactiva:** endpoints y esquemas documentados con OpenAPI/Swagger.
- **Testing:** pruebas automatizadas de integración con Vitest y Supertest.
- **Inicialización de datos:** scripts para creación y carga segura de información en la base de datos.

## 🏗️ Arquitectura del proyecto

El backend está organizado bajo una arquitectura por capas, separando responsabilidades para facilitar el mantenimiento, la escalabilidad y la reutilización del código.

```text
la-cuartense-api/
├── src/
│   ├── controllers/      # Controladores HTTP y lógica de respuesta
│   ├── db/               # Conexión y verificación de PostgreSQL
│   ├── middleware/       # Validaciones y manejo de errores
│   ├── models/           # Acceso a datos y consultas SQL
│   ├── routes/           # Definición de endpoints y Swagger
│   ├── scripts/          # Inicialización y carga segura de datos
│   ├── app.js            # Configuración de Express
│   └── server.js         # Punto de entrada del servidor
└── tests/                # Pruebas unitarias y de integración
```

## 🛠️ Tecnologías utilizadas

| Tecnología | Aplicación |
|---|---|
| Node.js | Entorno de ejecución |
| Express | Desarrollo de API REST |
| PostgreSQL | Base de datos relacional |
| node-postgres (pg) | Conexión con PostgreSQL |
| express-validator | Validación de datos |
| Swagger / OpenAPI | Documentación de endpoints |
| Vitest | Pruebas automatizadas |
| Supertest | Pruebas de integración HTTP |
| Git / GitHub | Control de versiones |

## 💻 Requisitos del sistema

- Node.js v18 o superior.
- PostgreSQL instalado y en ejecución.
- Git.

## ⚙️ Instalación y configuración

### 1. Clonar el repositorio

```bash
git clone https://github.com/spataro787/la-cuartense-api.git

cd la-cuartense-api
```

### 2. Instalar dependencias

```bash
npm install
```

### 3. Configurar variables de entorno

Copiar el archivo `.env.example` y crear un archivo `.env`:

```bash
cp .env.example .env
```

Configurar las credenciales de PostgreSQL:

```env
DATABASE_URL="postgresql://postgres:TU_PASSWORD@127.0.0.1:5432/la-cuartense"
PORT=3000
NODE_ENV=development
```

### 4. Inicializar la base de datos

Crear la base de datos y cargar los datos iniciales:

```bash
node src/scripts/create-and-seed.js
```

### 5. Verificar la conexión

```bash
node src/db/test-db.js
```

## ▶️ Ejecución de la API

Modo desarrollo:

```bash
npm run dev
```

Modo producción:

```bash
npm start
```

**Acceso local:**

```text
http://localhost:3000
```

## 📖 Documentación Swagger

Con el servidor iniciado, acceder a la documentación interactiva:

```text
http://localhost:3000/api-docs
```

Swagger UI permite consultar los endpoints disponibles, visualizar sus esquemas y probar las solicitudes HTTP.

## 🧪 Pruebas automatizadas

El proyecto incorpora pruebas automatizadas para verificar el funcionamiento de los componentes y endpoints de la API.

Ejecutar la suite de pruebas:

```bash
npm test -- --run
```

Modo interactivo:

```bash
npm test
```

## 🎯 Objetivo del desarrollo

Desarrollar una solución backend para un negocio del rubro cárnico, centralizando la administración de productos, precios y stock mediante una API RESTful.

El proyecto permitió aplicar conocimientos de desarrollo backend, modelado de bases de datos relacionales, consultas SQL, validaciones, documentación de servicios y testing automatizado en un contexto de aplicación real.

## 👨‍💻 Desarrollador

**Agustín Spataro**  
Backend & Full Stack Developer

- 🌐 [Portfolio](https://agustin-spataro.vercel.app/)
- 💼 [LinkedIn](https://www.linkedin.com/in/agustin-spataro-dev/)
- 💻 [GitHub](https://github.com/spataro787)
