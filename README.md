# Mi Proyecto

## Descripción
Este proyecto es una aplicación web que integra un backend en Node.js con Express y un frontend basado en HTML, CSS y JavaScript. 
Además, maneja una base de datos para gestionar usuarios, sensores, contacto y servicios.

## Estructura del Proyecto

```
/mi-proyecto
│-- /backend/                # Todo el backend organizado aquí
│   │-- server.js            # Punto de entrada del servidor
│   │-- /config/             # Configuración del proyecto
│   │   ├── db.js            # Conexión a la base de datos
│   │-- /routes/             # Rutas de la API
│   │   ├── users.js         # Rutas para usuarios
│   │   ├── sensors.js       # Rutas para sensores
│   │   ├── contact.js       # Rutas para contacto
│   │   ├── services.js      # Rutas para servicios
│   │-- /controllers/        # Lógica de las rutas (controladores)
│   │   ├── usersController.js
│   │   ├── sensorsController.js
│   │   ├── contactController.js
│   │   ├── servicesController.js
│   │-- /models/             # Modelos de la base de datos
│   │   ├── usersModel.js
│   │   ├── sensorsModel.js
│   │   ├── contacModel.js
│   │   ├── servicesModel.js
│   │-- /middlewares/        # Middlewares (autenticación, logs, validaciones)
│   │   ├── authMiddleware.js
│   │   ├── logger.js
│   │-- /utils/              # Utilidades y funciones reutilizables
│   │   ├── helpers.js
│   │-- package.json         # Dependencias del backend
│   │-- .env                 # Variables de entorno (credenciales, puertos, etc.)
│
│-- /frontend/               # Todo el frontend organizado aquí
│   │-- /public/             # Archivos estáticos (CSS, JS, imágenes)
│   │   ├── /css/            # Estilos
│   │   ├── /js/             # Scripts frontend
│   │   ├── /img/            # Imágenes
│   │-- /views/              # Vistas HTML
│   │   ├── index.html
│   │   ├── users.html
│   │   ├── sensors.html
│   │   ├── contact.html
│   │   ├── services.html
│   │   ├── /components/     # Componentes reutilizables
│   │   │   ├── navbar.html  # Navbar
│   │   │   ├── footer.html  # Footer
│   │   │   ├── sidebar.html # Sidebar
│   │-- package.json         # Dependencias del frontend (si usas npm para frontend)
│
│-- /database/               # Archivos relacionados con la base de datos
│   │-- esquema.sql          # Script SQL para crear la base de datos
│   │-- datos_prueba.sql     # Datos de prueba
│
│-- /tests/                  # Pruebas unitarias y de integración
│   │-- backend.test.js      # Pruebas del backend
│   │-- frontend.test.js     # Pruebas del frontend
│
│-- .gitignore               # Archivos y carpetas a ignorar en Git
│-- README.md                # Documentación del proyecto
```
## Descripción detallada estructura
📂 /backend/
Aquí va toda la lógica del servidor.

server.js → Punto de entrada del backend.
/config/ → Contiene la configuración del servidor y la base de datos.
/routes/ → Define las rutas de la API.
/controllers/ → Aquí va la lógica de negocio de cada ruta.
/models/ → Define cómo se estructuran los datos en la base de datos.
/middlewares/ → Contiene autenticación, validaciones, logs, etc.
/utils/ → Funciones de utilidad para no repetir código.

📂 /frontend/
Aquí va todo lo relacionado con la interfaz de usuario.

/public/ → Contiene CSS, JS y archivos estáticos.
/views/ → Aquí van los archivos HTML.
    /components/  → Componentes reutilizables

📂 /database/
Aquí guardamos archivos relacionados con la base de datos.

esquema.sql → Script SQL para crear las tablas.
datos_prueba.sql → Datos de prueba para hacer test.

📂 /tests/
Aquí van las pruebas automatizadas del backend y frontend.

## Instalación

### Requisitos previos
- Node.js superior a la 18 y npm
- Workbench 8.0
- Base de datos (MySQL)

### Clonar el repositorio
```sh
git clone https://github.com/usuario/mi-proyecto.git
cd mi-proyecto
```

### Configuración del Backend
```sh
cd backend
npm install
cp .env.example .env  # Configurar variables de entorno
node server.js  # Iniciar el servidor
```

### Configuración del Frontend
```sh
cd frontend
npm install
npm start  # Iniciar el servidor de desarrollo
```

## Uso
- Acceder a la API en `http://localhost:3000`
- Acceder a la interfaz en `http://localhost:8080`
- puerto 3306 || 3400

## Pruebas
Ejecutar pruebas unitarias y de integración:
```sh
cd tests
npm test
```

## Contribución
1. Hacer un fork del repositorio (crear una copia del repositorio en tu propia cuenta.)
2. Crear una rama (`feature-nueva`)
3. Realizar cambios y hacer commit
4. Crear un pull request

## Licencia
Este proyecto está bajo la licencia MIT.
