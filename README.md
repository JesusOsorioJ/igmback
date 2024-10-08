# Proyecto de API RESTful con Laravel y Node.js

Este proyecto consiste en una API RESTful desarrollada en Laravel que se comunica con un servidor WebSocket implementado en Node.js para notificaciones en tiempo real. La API incluye funcionalidades CRUD para gestionar cuentas y pedidos, y utiliza un servidor Node.js para manejar las notificaciones en tiempo real y almacenar los pedidos en MongoDB Atlas.

## Tabla de Contenidos

- [Requerimientos](#requerimientos)
- [Instalación](#instalación)
- [Configuración](#configuración)
- [Uso](#uso)
- [Documentación de la API](#documentación-de-la-api)
- [Pruebas de Endpoints](#pruebas-de-endpoints)
- [Pruebas de Test](#pruebas-de-Test)
## Pruebas Test

## Requerimientos

Para ejecutar este proyecto, necesitas tener instalado:

- PHP >= 8.0
- Composer
- Laravel 8.x
- Visual Studio Code con la extensión [REST Client](https://marketplace.visualstudio.com/items?itemName=humao.rest-client)

## Instalación

1. **Clona este repositorio:**

    ```bash
    git clone https://gitlab.com/usuario/proyecto.git
    cd proyecto
    ```

2. **Instalar dependencias de Laravel:**

    ```bash
    composer install
    ```

## Configuración

1. Copia el archivo `.env.example` y renómbralo a `.env`:

    ```bash
    cp .env.example .env
    ```
    
2. Genera la clave de la aplicación:

    ```bash
    php artisan key:generate
    ```

3. Configura las variables de entorno para la base de datos y otros servicios en el archivo `.env`.

    - DB_CONNECTION
    - DB_HOST
    - DB_PORT
    - #DB_DATABASE
    - DB_USERNAME
    - DB_PASSWORD

## Uso

1. **Migrar la base de datos:**

    ```bash
    php artisan migrate
    ```

2. **Iniciar el servidor de Laravel:**

    ```bash
    php artisan serve
    ```

    El servidor estará disponible en `http://localhost:8000`.


## Documentación de la API

La documentación de la API se ha generado utilizando **Swagger**. Puedes acceder a ella visitando: http://localhost:8000/api/documentation

Esta documentación incluye todos los endpoints disponibles, sus métodos, parámetros, respuestas, y ejemplos.

## Pruebas de Endpoints

Para probar los endpoints, se ha proporcionado un folder de `REST Client` en el directorio raíz del proyecto.

### Cómo usar el archivo de `REST Client`:

1. **Instalar la extensión REST Client en Visual Studio Code:**

    Si aún no la tienes instalada, puedes encontrarla [aquí](https://marketplace.visualstudio.com/items?itemName=humao.rest-client).

2. **Abrir el archivo `.rest`:**

3. **Hacer requests:**

    Haz clic en el botón `Send Request` al lado de cada bloque de solicitud para probar los diferentes endpoints de la API.

## Pruebas de Test

Para ejecutar las pruebas del proyecto, asegúrate de que tu entorno de desarrollo esté configurado correctamente y sigue los siguientes pasos:

### Configuración de la Base de Datos de Pruebas

1. Abre el archivo `.env` en la raíz del proyecto.
2. Configura la base de datos de pruebas. Para usar SQLite en memoria, agrega las siguientes líneas:

    ```env
    DB_CONNECTION=sqlite
    DB_DATABASE=:memory:
    ```

### Ejecutar Pruebas

Para ejecutar todas las pruebas, abre tu terminal y corre el siguiente comando:

```bash
php artisan test
