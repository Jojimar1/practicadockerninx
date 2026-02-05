Django Personal Blog - Arquitectura Profesional Contenedorizada
📋 Descripción del Proyecto
Este repositorio contiene un sistema de blog personal desarrollado en Django 5.1, diseñado específicamente para ejecutarse en entornos de producción mediante Docker. La arquitectura no utiliza el servidor de desarrollo simple de Django; en su lugar, implementa un stack profesional compuesto por un servidor de aplicaciones (Gunicorn) y un servidor web de alto rendimiento (Nginx) actuando como proxy inverso.

🏗️ Stack Tecnológico
Lenguaje: Python 3.13-slim (Optimizado para contenedores).

Framework: Django 5.1.

Servidor de Aplicaciones: Gunicorn (Green Unicorn).

Servidor Web / Proxy: Nginx (Alpine Linux).

Orquestación: Docker & Docker Compose.

Frontend: Tailwind CSS (vía django-tailwind).

⚙️ Arquitectura de Servicios
El despliegue se gestiona a través de dos servicios principales interconectados:

Servicio web:

Construido a partir de una imagen de Python ligera.

Gestiona la lógica de negocio, procesamiento de formularios y base de datos.

No expone puertos directamente al exterior para mayor seguridad.

Servicio nginx:

Actúa como puerta de enlace única (Puerto 80).

Balanceo y Proxy: Redirige el tráfico dinámico al contenedor de Django.

Eficiencia: Sirve directamente los archivos estáticos (CSS, JS) y multimedia (imágenes) desde volúmenes compartidos, liberando de carga a Python.
