# 💬 Real-Time Chat Application

<p align="center">
  <img src="https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white" alt="Node.js">
  <img src="https://img.shields.io/badge/Express.js-000000?style=for-the-badge&logo=express&logoColor=white" alt="Express">
  <img src="https://img.shields.io/badge/Socket.io-010101?style=for-the-badge&logo=socketdotio&logoColor=white" alt="Socket.io">
  <img src="https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white" alt="MySQL">
</p>

Aplicación de chat en tiempo real desarrollada con **Node.js**, **Express**, **Socket.io** y persistencia en base de datos **MySQL**. Cuenta con una interfaz de usuario moderna tipo SaaS/corporativa y soporte para recuperación de estado de conexión.


## 🚀 Características Principales

* **Comunicación en Tiempo Real:** Envío y recepción instantánea de mensajes utilizando WebSockets (`Socket.io`).
* **Persistencia de Datos:** Almacenamiento seguro de los historiales de mensajes en una base de datos MySQL local mediante promesas (`mysql2/promise`).
* **Recuperación de Conexión:** Implementación de `connectionStateRecovery` para evitar la pérdida de mensajes ante microcortes de red.
* **Sesiones Dinámicas:** Generación automática de nombres de usuario únicos e independientes por pestaña utilizando `sessionStorage`.
* **Interfaz Moderna:** Diseño oscuro de estilo ejecutivo, limpio y responsivo con burbujas de chat diferenciadas (mensajes entrantes y salientes).


## 🛠️ Tecnologías Utilizadas

* **Backend:** Node.js, Express, Socket.io
* **Base de Datos:** MySQL
* **Frontend:** HTML5, CSS3 Moderno (Variables CSS, Flexbox)


## ⚙️ Instalación y Configuración

Sigue estos pasos para poner en marcha el proyecto de manera local:

### 1. Clonar el repositorio
```bash
git clone [https://github.com/ferzincal/realtime-chat-js.git](https://github.com/ferzincal/realtime-chat-js.git)
cd realtime-chat-js

```

### 2. Instalar dependencias

Asegúrate de tener Node.js instalado en tu equipo y ejecuta:

```bash
npm install

```

### 3. Configurar la base de datos

Crea una base de datos en tu servidor MySQL local y asegúrate de tener una tabla para los mensajes. Puedes ejecutar el siguiente script SQL:

```sql
CREATE DATABASE IF NOT EXISTS tienda;
USE tienda;

CREATE TABLE IF NOT EXISTS messages (
    id INT AUTO_INCREMENT PRIMARY KEY,
    content TEXT NOT NULL,
    user VARCHAR(100) NOT NULL
);

```

### 4. Configurar las credenciales

Verifica la conexión a tu base de datos dentro del archivo del servidor (`server/index.js`), asegurándote de que el `host`, `user`, `password` y `database` coincidan con tu entorno local.

### 5. Ejecutar la aplicación

Inicia el servidor en modo desarrollo (con recarga automática mediante `--watch`):

```bash
npm run dev

```

Abre tu navegador y accede a:

```text
http://localhost:3000

```

---

## 👨‍💻 Autor

Desarrollado por **ferzincal**.

