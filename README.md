# Biblioteca-en-equipo
# Sistema de Gestión de Biblioteca (INF-512)

## Integrantes
Keyther Davis Tavera Peralta 100765924 
Cesar Alonso Sierra Cuevas 100708687 
Randy José Sánchez Mota 100552665 
Diana Lia Víctor Ventura 100630377

Un sistema de consola desarrollado en C# (.NET) para gestionar el inventario, registro de usuarios, préstamos y devoluciones de libros de una biblioteca universitaria.

---

## 📝 Descripción del Proyecto

Este proyecto es una aplicación de consola orientada a objetos (POO) que permite administrar las operaciones esenciales de una biblioteca:
* Registro y control de inventario de libros categorizados.
* Registro de estudiantes/usuarios de la universidad.
* Gestión del ciclo de vida de los préstamos (salida y devolución).
* Consultas en tiempo real sobre disponibilidad y estado de préstamos activos por usuario.

---

## 🧩 Clases Principales

El proyecto sigue una arquitectura en capas sencilla separando las entidades del dominio, la lógica de negocio y la interfaz de usuario:

| Clase | Tipo | Descripción |
| :--- | :--- | :--- |
| `Categoria` | Entidad | Representa las áreas de conocimiento (ej. *Ingeniería de Software*, *Matemáticas*). |
| `Libro` | Entidad | Almacena el código, título, autor, categoría asignada y estado de disponibilidad (`EstaDisponible`). |
| `Usuario` | Entidad | Modela a los estudiantes o lectores del sistema mediante su matrícula/ID universitario, nombre y carrera. |
| `Prestamo` | Entidad | Asocia un `Libro` a un `Usuario`, registrando la fecha de salida y de devolución. |
| `Biblioteca` | Lógica | Contiene la lógica de negocio central (registros, validaciones de disponibilidad, búsquedas y relaciones). |
| `Program` | Interfaz (Consola) | Administra el menú interactivo, la entrada/salida de datos por consola y los mensajes de error/éxito. |

---

## 🐳 Contenedor Utilizado

Para simplificar el despliegue y garantizar que la aplicación funcione en cualquier entorno sin necesidad de instalar .NET localmente, el proyecto se encuentra dockerizado utilizando **Docker**:

## las instrucciones para utilizarlo son ir a la consola entrar en la terminal y buscar la carpeta usando cd (nombre de la carpeta) luego escribiras dotnet run y listo

este es el contenedor de forma interactiva
docker run -it --rm sistema-biblioteca

## distribucion 
Integrante / Rol       Responsabilidades y Aportes

Modelado de Datos / POO      Diseños de las clases Categoria, Libro, Usuario y Prestamo con encapsulamiento.

Lógica de Negocio (Biblioteca)     Implementación de las búsquedas con LINQ, control de duplicados y flujo de préstamos/devoluciones.

Interfaz de Usuario (Program)      Diseño del menú en consola, formateo de texto, colores de alerta y validación de entradas.

Despliegue y Dockerization          Creación del Dockerfile, pruebas de contenedorización y documentación en el README.md.
