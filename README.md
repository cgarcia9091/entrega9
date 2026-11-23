# Blog Django

Proyecto web de un blog desarrollado con Django. Permite gestionar publicaciones mediante el panel administrativo y mostrarlas dinámicamente utilizando el ORM de Django y una base de datos SQLite.

## Descripción

Este proyecto contiene:

- Proyecto principal `blog_project`.
- Aplicación `posts`.
- Templates HTML con herencia.
- Estilos CSS.
- Modelo `Post` para gestionar publicaciones.
- Panel administrativo de Django.
- Listado dinámico de publicaciones.

## Requisitos

- Python 3.12 o superior.
- Django 6.1.3.

## Instalación

Clonar el repositorio:

```bash
git clone https://github.com/cgarcia9091/entrega9.git
```

Ingresar a la carpeta:

```bash
cd entrega9
```

Crear el entorno virtual:

```bash
python -m venv venv
```

Activar el entorno virtual en Windows PowerShell:

```powershell
.\venv\Scripts\Activate.ps1
```

Instalar las dependencias:

```bash
pip install -r requirements.txt
```

Aplicar las migraciones:

```bash
python manage.py migrate
```

## Crear un superusuario

Para acceder al panel administrativo, ejecutar:

```bash
python manage.py createsuperuser
```

Seguir las instrucciones para crear el nombre de usuario, correo electrónico y contraseña.

## Ejecutar el servidor

```bash
python manage.py runserver
```

Abrir en el navegador:

- Inicio: http://127.0.0.1:8000/
- Publicaciones: http://127.0.0.1:8000/posts/
- Acerca de: http://127.0.0.1:8000/acerca/
- Panel administrativo: http://127.0.0.1:8000/admin/

## Modelo Post

El modelo `Post` contiene los siguientes campos:

- `titulo`: título de la publicación.
- `contenido`: contenido del post.
- `autor`: autor de la publicación.
- `fecha_creacion`: fecha generada automáticamente.
- `estado`: permite seleccionar entre borrador, publicado y archivado.

Las publicaciones se administran desde el panel administrativo de Django.

## ORM y publicaciones dinámicas

El listado de publicaciones utiliza el ORM de Django para consultar los posts cuyo estado sea publicado, ordenados por fecha de creación descendente.

Las publicaciones se muestran dinámicamente en los templates `inicio.html` y `lista_posts.html`.

## Aplicaciones

- `posts`: aplicación encargada de gestionar las publicaciones del blog.

## Configuración

- Idioma: español de Argentina (`es-ar`).
- Zona horaria: `America/Argentina/Buenos_Aires`.
- Base de datos: SQLite.