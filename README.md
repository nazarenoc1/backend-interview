# Prueba técnica Laravel
 
## Requisitos previos

Este repositorio está construido utilizando Laravel versión 10. Si nunca trabajaste  con esta versión de Laravel, asegúrate de contar con los siguientes requisitos previos:

 - PHP 8.1 o superior
 - Extensión SQLite habilitada para tu versión de PHP

## Instalación

Para comenzar, clona el repositorio en tu entorno local utilizando el siguiente comando:
`git clone https://github.com/animus-coop/prueba-tecnica-laravel.git`

Luego, para configurar la base de datos, debes seguir estos pasos:

 1. Crea un archivo llamado `database.sqlite` dentro de la carpeta `database` del repositorio.
 2. Copia el archivo `.env.example` y renómbralo a `.env`. Podes hacerlo fácilmente desde Visual Studio Code o ejecutando `cp .env.example .env` en la terminal.
 3. Abri el archivo `.env` en el editor de código y busca la variable de entorno `DB_DATABASE`. Edítala para que apunte al path absoluto del archivo `database.sqlite` que creaste anteriormente.

> Asegúrate de reemplazar `/absolute/path/to/` con la ubicación real del
> archivo SQLite en tu sistema. 


Posteriormente deberías poder ejecutar sin inconvenientes  `php artisan migrate:fresh --seed` para crear la estructura de las tablas en la base de datos e insertar algunos registros a modo de ejemplo.

## Objetivos
### Endpoint para agregar nuevos items
El repositorio ya incluye el `TaskController` donde podrás visualizar la función `index`, `show`, `store`, `update` y `delete`. En dicho controlador deberás hacer la lógica para que mediante la función `store` se puedan agregar nuevos items a la base de datos.

> No te olvides, además de la lógica del controlador, vas a tener que armar la ruta API que utilice la función que acabás de tocar.

### Endpoint para eliminar items
En este caso, tendrás que crear un endpoint que **borre** el item específico que le indiques de la base de datos.

> Además de meterle mano al controlador, acordate de armar la ruta API que se conecte con la función que acabás de modificar. 

¡Éxitos! 😎
