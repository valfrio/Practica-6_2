# Práctica 6.2 - Despliegue de una aplicación PHP con Nginx y MySQL usando Docker y Docker-Compose
Para comenzar, la ip usada fue 192.168.91.192.

## Estructura de directorios

Para comenzar, se ha creado una estructura de directorios como la siguiente:

![1](assets/images/1.png)

que queda de la siguiente forma:

![2](assets/images/2.png)

## Creación del contenedor de Nginx

Para comenzar, modificamos el docker-compose.yml:

![3](assets/images/3.png)

Correremos el contenedor y comprobaremos que funciona correctamente:

![4](assets/images/4.png)

Si funciona correctamente, veremos la siguiente página:

![5](assets/images/6.png)

## Creación del contenedor de PHP

Creamos el index.php:

![6](assets/images/7.png)

Ahora debemos de modificar la configuración de Nginx para que pueda ejecutar PHP:

![7](assets/images/8.png)

y por último modificamos el Dockerfile de Nginx:

![8](assets/images/9.png)

Modificamos el docker-compose.yml:

![9](assets/images/10.png)

Ahora levantamos los contenedores y comprobamos que funciona correctamente:

![10](assets/images/11.png)

Comprobamos que funciona correctamente:

![11](assets/images/12.png)

## Creación del contenedor MySQL

Modificamos el Dockerfile de php:

![12](assets/images/13.png)

Modificamos el docker-compose.yml:

![13](assets/images/14.png)

Modificamos el index.php:

![14](assets/images/15.png)

Se levantan los contenedores y comprobamos que funciona correctamente:

![15](assets/images/17.png)

y comprobamos los contenedores:

![16](assets/images/18.png)

## Conexión a la base de datos

Accedemos a la página y comprobamos que funciona correctamente:

![16](assets/images/19.png)

Ahora para comprobar que se ha conectado correctamente a la base de datos, modificamos el index.php con un nuevo usuario, dejando el index así:

![17](assets/images/20.png)

y comprobamos que funciona correctamente:

![18](assets/images/21.png)

## Esquema de la aplicación

![19](assets/images/22.png)
