<img width="1897" height="902" alt="image" src="https://github.com/user-attachments/assets/ab0ed94d-eee4-4c42-980a-877723a789da" />Descripcion del Proyecto
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
<img width="1897" height="902" alt="Captura de pantalla 2026-02-05 203110" src="https://github.com/user-attachments/assets/d6979f86-130b-403e-81b7-95825c9a4a6d" />
<img width="1000" height="768" alt="aaaaaaaa" src="https://github.com/user-attachments/assets/1ef63960-1225-4446-893b-5df0d0259aeb" />
<img width="1000" height="768" alt="aaaaaaaa" src="https://github.com/user-attachments/assets/d5978043-17e7-4a18-921d-336c2540eea6" />
