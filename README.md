# User Management API

Esta es una API robusta construida con **Node.js** y **Express** para gestionar usuarios. Permite realizar operaciones CRUD (Crear, Listar, Actualizar y Eliminar) de forma sencilla.

## 🚀 Tecnologías Utilizadas

- **Node.js**: Entorno de ejecución para JavaScript.
- **Express**: Framework web para Node.js.
- **Sequelize**: ORM para facilitar la interacción con la base de datos.
- **SQLite**: Base de datos SQL local (por defecto).
- **PostgreSQL**: Soporte listo para producción (opcional).
- **Dotenv**: Gestión de variables de entorno.
- **CORS**: Habilita peticiones desde otros dominios (útil para integración con Flutter/Web).

## 📌 Funcionalidades

La API permite gestionar usuarios con los siguientes campos:
- `id`: Identificador único (autoincremental).
- `name`: Nombre del usuario.
- `job`: Puesto de trabajo o profesión.

### Endpoints
- `GET /users`: Obtiene la lista de todos los usuarios.
- `POST /users`: Crea un nuevo usuario. (Requiere `name` y `job` en el cuerpo de la petición).
- `PUT /users/:id`: Actualiza la información de un usuario existente.
- `DELETE /users/:id`: Elimina un usuario por su ID.

## ⚙️ Configuración y Puertos

El servidor corre por defecto en el puerto: **3000**.

Puedes cambiar el puerto o la base de datos editando el archivo `.env`:
```env
PORT=3000
DB_DIALECT=sqlite
DB_STORAGE=./database.sqlite
```

## 🛠️ Cómo Ejecutar la Aplicación

1. **Instalar dependencias**:
   Asegúrate de estar en la raíz del proyecto y ejecuta:
   ```bash
   npm install
   ```

2. **Ejecutar el servidor**:
   Puedes usar el script de inicio preconfigurado:
   ```bash
   npm start
   ```
   O directamente con node:
   ```bash
   node index.js
   ```

3. **Verificar**:
   Abre tu navegador o herramienta de pruebas (Postman/Insomnia) en:
   `http://localhost:3000/users`
