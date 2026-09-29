# KiriClaw

Este repositorio contiene el código fuente del backend para el proyecto KiriClaw. Está desarrollado en Python y organizado mediante una arquitectura modular para separar responsabilidades.

## Estructura del proyecto

* **alembic/**: Archivos y configuraciones para manejar las migraciones de la base de datos.
* **api/**: Definición de los endpoints y rutas de la aplicación.
* **core/**: Configuraciones globales del sistema, seguridad y manejo de variables de entorno.
* **db/**: Lógica de conexión a la base de datos y gestión de sesiones.
* **models/**: Modelos ORM que representan las tablas en la base de datos.
* **schemas/**: Esquemas de validación para los datos de entrada y salida de las peticiones.
* **script/**: Scripts de utilidad para tareas específicas o mantenimiento.

### Archivos principales en la raíz

* **main.py**: Punto de entrada de la aplicación. Es el archivo que se ejecuta para levantar el servidor.
* **alembic.ini**: Configuración de Alembic para las migraciones.
* **docker-compose.yml**: Configuración para levantar el entorno usando Docker.
* **requerimientos.txt**: Lista de dependencias y librerías de Python necesarias.

## Instalación local

Para correr este proyecto en tu computadora, sigue estos pasos:

1. **Clonar el repositorio**
   ```bash
   git clone https://github.com/AnaAlgandar89/KiriClaw.git
   cd KiriClaw
   ```

2. **Crear y activar el entorno virtual**
   ```bash
   python -m venv .venv
   ```
   * En Windows: `.venv\Scripts\activate`
   * En Linux/Mac: `source .venv/bin/activate`

3. **Instalar dependencias**
   ```bash
   pip install -r requerimientos.txt
   ```

4. **Configurar el entorno**
   Crea un archivo `.env` en la raíz del proyecto basándote en las variables que requiere el sistema (conexión a DB, claves secretas, etc.). Este archivo no se sube al repositorio por seguridad.

5. **Ejecutar el servidor**
   ```bash
   uvicorn main:app --reload
   ```
   La API estará corriendo en `http://localhost:8000`.