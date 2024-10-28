Documentación del Proyecto CRUD
1. Introducción
¡Hola! Aquí te cuento cómo desarrollé mi proyecto CRUD (Crear, Leer, Actualizar, Eliminar) usando Ruby on Rails y PostgreSQL. Este sistema es súper útil para gestionar datos a través de una interfaz web.

2. Tecnologías Utilizadas
Para este proyecto, usé:

Ruby como lenguaje de programación.
Ruby on Rails como framework.
PostgreSQL como base de datos.
HTML, CSS y JavaScript para el frontend.
3. Instalación de Dependencias
3.1. Requisitos Previos
Primero, asegúrate de tener instalado lo siguiente:

Ruby
Rails
PostgreSQL
3.2. Crear un nuevo proyecto
Empecé creando un nuevo proyecto con este comando:

bash
Copiar código
rails new nombre_del_proyecto --database=postgresql
cd nombre_del_proyecto
3.3. Configuración de la Base de Datos
Luego, abrí el archivo config/database.yml para asegurarme de que la configuración estaba correcta. Después, creé la base de datos con:

bash
Copiar código
rails db:create
4. Generación de Recursos
4.1. Crear un recurso
Para generar un recurso, como por ejemplo Post, ejecuté:

bash
Copiar código
rails generate scaffold Post title:string content:text
4.2. Migrar la Base de Datos
Después, apliqué las migraciones para que se crearan las tablas en la base de datos:

bash
Copiar código
rails db:migrate
5. Configuración de Rutas
En el archivo config/routes.rb, me aseguré de que el recurso estuviera bien enrutado, así:

ruby
Copiar código
resources :posts
root "posts#index" # Defino la ruta raíz
6. Implementación del CSS
6.1. Crear archivo de estilos
Creé un archivo llamado estilos.css en app/assets/stylesheets/ y añadí algunos estilos básicos. Aquí te dejo un ejemplo de lo que incluí:

css
Copiar código
/* estilos.css */

/* Estilo general del cuerpo */
body {
    font-family: Arial, sans-serif;
    background-color: black;
    color: white;
    margin: 0;
    padding: 0;
    display: flex;
    align-items: center;
    justify-content: center;
    height: 100vh;
}

/* Contenedor principal */
.container {
    max-width: 800px;
    width: 90%;
    padding: 2rem;
    background-color: rgba(255, 255, 255, 0.1);
    border-radius: 10px;
    box-shadow: 0 4px 30px rgba(0, 0, 0, 0.8);
    text-align: center;
    border: 2px solid white;
}

/* Efecto al pasar el mouse sobre el contenedor */
.container:hover {
    background-color: rgba(255, 255, 255, 0.2);
    transform: scale(1.05);
}
6.2. Incluir CSS en la aplicación
Asegúrate de incluir el archivo estilos.css en application.css o application.scss así:

scss
Copiar código
/*
 *= require_tree .
 *= require_self
*/
@import "estilos.css";
7. Ejecución de la Aplicación
Para iniciar el servidor y ver mi proyecto en acción, simplemente ejecuté:

bash
Copiar código
rails server
Luego, abrí mi navegador y fui a http://localhost:3000.

8. Conclusión
Y así es como desarrollé mi proyecto CRUD. Desde la creación inicial hasta el CSS, todo fue un proceso bastante divertido. Si quieres, puedes añadir más detalles o ejemplos de uso a esta documentación. ¡Espero que te sirva!
