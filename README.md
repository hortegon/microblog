Proyecto Microblog - Flask
Este proyecto es un sistema de microblogging desarrollado en Flask, realizado por el profesor Henry Ortegon como parte del curso de programación web.

Requisitos previos
Python 3.8 o superior

Git (opcional)

Terminal (Bash, CMD o PowerShell)

Instalación paso a paso
1. Clonar el repositorio
bash
git clone https://github.com/henryortegon/microblog.git
cd microblog
2. Crear entorno virtual
bash
python -m venv venv
3. Activar entorno virtual
bash
# Windows (CMD):
venv\Scripts\activate

# Windows (PowerShell):
.\venv\Scripts\Activate.ps1

# Linux/Mac:
source venv/bin/activate
4. Instalar dependencias
bash
pip install -r requirements.txt
5. Configurar variables de entorno
bash
# Copiar plantilla de variables:
copy .env.example .env  # Windows
cp .env.example .env    # Linux/Mac

# Editar archivo .env con tus credenciales
notepad .env  # Windows
nano .env     # Linux/Mac
Importante: Configurar al menos:

SECRET_KEY (cadena aleatoria)

MAIL_USERNAME y MAIL_PASSWORD para funcionalidad de correo

DATABASE_URL (ej: sqlite:///app.db)

6. Inicializar base de datos
bash
flask db upgrade
7. Ejecutar la aplicación
bash
flask run
Visita la aplicación en: http://localhost:5000

Comandos útiles
Acción	Comando
Crear nuevas migraciones	flask db migrate -m "Descripción"
Aplicar migraciones	flask db upgrade
Desactivar entorno virtual	deactivate
Instalar nueva dependencia	pip install <paquete>
Actualizar requirements	pip freeze > requirements.txt
Estructura del proyecto
text
microblog/
├── app/
│   ├── templates/      # Plantillas HTML
│   ├── __init__.py     # Configuración de la app
│   ├── routes.py       # Rutas y controladores
│   ├── models.py       # Modelos de base de datos
│   ├── forms.py        # Formularios
│   └── emails.py       # Funciones de correo
├── migrations/         # Migraciones de base de datos
├── venv/               # Entorno virtual (no se incluye en Git)
├── .env                # Variables de entorno (no se incluye en Git)
├── .env.example        # Plantilla de variables
├── config.py           # Configuración principal
├── microblog.py        # Punto de entrada
└── requirements.txt    # Dependencias
Solución de problemas comunes
Error: Módulo no encontrado

bash
pip install nombre_modulo
pip freeze > requirements.txt
Error: Importación relativa

Asegúrate que los imports en app/__init__.py usen:

python
from config import Config
Error: Validación de email

bash
pip install email_validator
Características implementadas
✅ Sistema de usuarios (registro, login, perfil)

✅ Publicación de mensajes (posts)

✅ Seguimiento entre usuarios

✅ Recuperación de contraseña por email

✅ Paginación de resultados

✅ Internacionalización (i18n)

✅ API REST básica

Soporte técnico
Para problemas técnicos, contactar al profesor:
Henry Ortegon
📧 hortegong@inemkennedy.edu.co
via-tecno.com

Nota: Este proyecto es con fines educativos. No usar en producción sin las debidas medidas de seguridad.

a trabajar chicos
