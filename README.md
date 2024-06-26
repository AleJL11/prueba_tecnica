# Proyecto Laravel con PostgreSQL

Este proyecto es un ejemplo de una aplicación Laravel que utiliza PostgreSQL como base de datos.

## Requisitos

- PHP 7.4 o superior
- Composer
- PostgreSQL
- Extensión PDO_PgSQL habilitada en PHP

## Configuración Inicial

### 1. Clonar el Repositorio

Clona el repositorio en tu máquina local:

```sh
git clone https://github.com/AleJL11/prueba_tecnica.git
cd prueba_tecnica

### 2. Instalar dependencias
Instala las dependencias de PHP utilizando Composer:
composer install

### 3. Configurar el Archivo .env
Copia el archivo .env.example a .env:
cp .env.example .env

Edita el archivo .env y configura los parámetros de la base de datos PostgreSQL:

DB_CONNECTION=pgsql
DB_HOST=127.0.0.1
DB_PORT=5432
DB_DATABASE=nombre_de_tu_base_de_datos
DB_USERNAME=tu_usuario
DB_PASSWORD=tu_contraseña

### 4. Generar la Clave de Aplicación
Genera una clave de aplicación:
php artisan key:generate

### 5. Ejecutar Migraciones
Ejecuta las migraciones para crear las tablas en la base de datos:
php artisan migrate

### Operaciones CRUD de Productos

- Crear un Producto
Envía una solicitud POST a /productos con los siguientes campos:

nombre: Nombre del producto
descripcion: Descripción del producto
precio: Precio del producto
Leer Productos
Envía una solicitud GET a /productos para obtener la lista de productos.

- Actualizar un Producto
Envía una solicitud PUT a /productos/{id} con los campos que deseas actualizar:

nombre: Nombre del producto
descripcion: Descripción del producto
precio: Precio del producto
Eliminar un Producto
Envía una solicitud DELETE a /productos/{id} para eliminar un producto.

- Vistas y Plantillas Blade
Listar Productos
La vista resources/views/productos/index.blade.php muestra la lista de productos.

- Agregar un Nuevo Producto
La vista resources/views/productos/create.blade.php contiene un formulario para agregar un nuevo producto.

- Ver Detalles de un Producto
La vista resources/views/productos/show.blade.php muestra los detalles de un producto específico.

### Pasos para Verificar y Ejecutar

- Clonar y Configurar el Proyecto:

Clona el repositorio en el directorio htdocs de XAMPP.
Configura el archivo .env con los detalles de PostgreSQL y ejecuta composer install.

- Ejecutar las Migraciones:

Ejecuta php artisan migrate para crear las tablas en PostgreSQL.

- Iniciar el Servidor de Desarrollo:

Desde la terminal, ejecuta php artisan serve y accede a http://localhost:8000/productos en tu navegador.

- Probar la Aplicación:

Navega a las rutas de tu aplicación (http://localhost:8000/productos) para asegurarte de que todo funciona correctamente.