Descripcion del Proyecto
Este proyecto consiste en el desarrollo y despliegue de un blog personal utilizando el framework Django. El objetivo principal ha sido implementar una arquitectura profesional mediante la contenedorizacion, separando la logica de la aplicacion del servidor de archivos estaticos.

Para lograr esto, se ha utilizado Docker para gestionar los entornos y Nginx como proxy inverso, asegurando un flujo de trabajo organizado y reproducible.

Tecnologias Utilizadas
Backend: Python 3.13-slim y Django.

Servidor de aplicaciones: Gunicorn.

Servidor web y Proxy inverso: Nginx.

Despliegue: Docker y Docker Compose.

Gestion de estilos: Tailwind CSS.

Estructura de la Arquitectura
La infraestructura se divide en dos servicios definidos en el archivo docker-compose:

Servicio Web: Ejecuta la aplicacion Django a traves de Gunicorn. Se encarga de procesar las peticiones del blog y gestionar la base de datos.

Servicio Nginx: Actúa como intermediario entre el usuario y la aplicacion. Su funcion es recibir las peticiones en el puerto 80 y servir de manera eficiente los archivos estaticos y multimedia almacenados en los volumenes.
