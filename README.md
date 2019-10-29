<p align="center"><img src="https://res.cloudinary.com/dtfbvvkyp/image/upload/v1566331377/laravel-logolockup-cmyk-red.svg" width="400"></p>

paso 1: instalar composer, xampp y git

paso 2: borrar el contenido de la carpeta C:\xampp\htdocs

paso 3: inicializar git bash en la carpeta antes mencionada y ejecutar en la CLI el siguiente comando:

$git clone  https://github.com/Juanjomorad/Prueba  

paso 4: en xampp arrancar los modulos de Apache y MySQL

paso 5: en http://localhost/phpmyadmin/ crear una base de datos con el nombre "prueba"

paso 6: en nuestra carpeta clonada de git hub (C:\xampp\htdocs\prueba) abriremos el cmd  y ejecutamos el comando

>composer install
para instalar todas dependencias, esto puede tardar un poco (depende de la conexion )

paso 7: en el mismo cmd ejecutamos el comando

>copy .env.example .env
Abrimos el archivo .env que se genero con el comando anterior y cambiamos

DB_DATABASE=laravel por DB_DATABASE=prueba <--- que es el mismo nombre de la base que creamos en el paso 5

paso 8: en el mismo cmd ejecutamos el comando

>php artisan migrate
para que se generen las tablas de companies, employees y las tablas necesarias para la autenticacion de laravel

paso 9: en el mismo cmd ejecutamos el comando

>php artisan key:generate
para que se genere y configure una nueva key de la aplicacion

paso 10: en nuestro navegador de preferencia iremos a la siguiente direccion

http://localhost/prueba/public/register
y crearemos el usuario de la aplicacion admin con email admin@admin.com y contraseña password, ya que creamos las tablas y columnas desde migraciones en el paso 8 estaremos sin datos en esta.

y listo ya con esto estara configurado el proyecto laravel para la creacion de compañias y empleados
