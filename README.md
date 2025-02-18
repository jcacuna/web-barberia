# Barbería - Sistema de Gestión

Este es un proyecto para la gestión de una barbería que incluye un sistema de reservas, administración de clientes y servicios.
El sistema consta de:
- **Frontend**: Desarrollado en Vue.js.
- **Backend**: Desarrollado en Node.js con Express y MongoDB.

## Características del Proyecto
- Registro y autenticación de usuarios.
- Gestión de citas y servicios.
- Listado de barberos y disponibilidad (Proxima funcionalidad).
- Integración con MongoDB para almacenamiento de datos.

---

## Tecnologías Utilizadas
### Frontend:
- Vue.js 3
- Vue Router
- Pinia
- Axios
- Tailwind CSS

### Backend:
- Node.js
- Express.js
- MongoDB con Mongoose
- JWT para autenticación
- CORS

---

## Instalación y Configuración

### 1. Clonar el repositorio
```sh
https://github.com/jcacuna/web-barberia
cd www.barberia.com
```

### 2. Configuración del Backend
```sh
cd backend
npm install
```
#### Variables de entorno (`.env`):
Crea un archivo `.env` en la carpeta `backend` y agrega:
```env
PORT=5000
MONGO_URI=mongodb+srv://usuario:password@cluster.mongodb.net/barberia
JWT_SECRET=clave_secreta
```
#### Ejecutar el servidor
```sh
npm start
```
El backend estará disponible en: `http://localhost:5000`

---

### 3. Configuración del Frontend
```sh
cd frontend
npm install
```
#### Configurar variables de entorno (`.env`):
Crea un archivo `.env` en la carpeta `frontend` y agrega:
```env
VITE_API_URL=http://localhost:5000
```
#### Ejecutar el frontend
```sh
npm run dev
```
El frontend estará disponible en: `http://localhost:5173`
---
## Deploy del Proyecto


---

## Contacto y Contribuciones
Si deseas contribuir, por favor abre un **pull request** o reporta un **issue** en GitHub.

¡Gracias por usar nuestro sistema de gestión para barberías! 💈✂️

