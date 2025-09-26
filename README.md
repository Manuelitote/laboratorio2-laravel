<p align="center"><a href="https://laravel.com" target="_blank"><img src="https://raw.githubusercontent.com/laravel/art/master/logo-lockup/5%20SVG/2%20CMYK/1%20Full%20Color/laravel-logolockup-cmyk-red.svg" width="400" alt="Laravel Logo"></a></p>

<p align="center">
<a href="https://github.com/laravel/framework/actions"><img src="https://github.com/laravel/framework/workflows/tests/badge.svg" alt="Build Status"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/dt/laravel/framework" alt="Total Downloads"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/v/laravel/framework" alt="Latest Stable Version"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/l/laravel/framework" alt="License"></a>
</p>

---

# 📌 Laboratorio 2 – Login en Laravel

## Índice
1. Requisitos previos  
2. Introducción (MVC y estructura del proyecto)  
3. Resultado (captura) 
4. Base de datos (`.env`, migraciones, backup)  
5. Dificultades y soluciones
6. Referencias
7. Footer del laboratorio   
8. Fecha de Ejecucion

---

## 1. Requisitos previos
Para el desarrollo de este laboratorio se utilizaron los siguientes recursos:  
- **PHP** >= 8.2 (incluido en XAMPP).  
- **Composer** (última versión).  
- **XAMPP** (con Apache y MySQL).  
- **Node.js y npm** (para compilar los assets con Vite).  
- **Visual Studio Code** (como editor de código).  
- **Laravel 12.x** (framework PHP).  
- Paquete de autenticación: `laravel/ui`.  
- Git y GitHub (para el versionamiento del proyecto).  

---

## 2. Introducción — Arquitectura MVC
Laravel se basa en la arquitectura **Modelo-Vista-Controlador (MVC)**:  
- **Modelo**: representa la capa de datos. Ejemplo: `User.php` dentro de `app/Models`.  
- **Vista**: plantillas Blade que muestran la interfaz de usuario (`resources/views`).  
- **Controlador**: gestiona la lógica de negocio y conecta modelos con vistas (`app/Http/Controllers`).  
- **Rutas**: definen las URL que acceden a controladores y vistas (`routes/web.php`).  

Este laboratorio tuvo como objetivo implementar un sistema de **login y registro de usuarios en Laravel**, reforzando conceptos de MVC y la integración con una base de datos MySQL.  

---

## 3. Resultados (captura)

El laboratorio culminó con éxito, obteniendo como resultado una aplicación Laravel con sistema de autenticación.  
Se pudieron visualizar correctamente las siguientes pantallas:  

- Página de inicio.  
- Formulario de registro.  
- Formulario de inicio de sesión.  
- Vista del panel principal después de autenticarse. 
- footer agregado al final.

Para documentar visualmente los resultados, se incluyeron capturas de pantalla de cada una de estas vistas dentro de una carpeta llamada `docs/screenshots` en el repositorio.

## 4. Base de datos (.env, migraciones, backup)
En el archivo `.env` se configuró la conexión a MySQL con los siguientes valores:  

DB_CONNECTION=mysql  
DB_DATABASE=lab_login  
DB_USERNAME=root  
DB_PASSWORD=  

**Una vez configurado el archivo, se ejecutaron las migraciones con el comando:**

php artisan migrate  

**Esto creó automáticamente las tablas necesarias (`users`, `cache`, `jobs`) dentro de la base de datos. **

Para generar el respaldo de la base de datos se utilizó el comando:  

cd C:\xampp\mysql\bin  
mysqldump -u root lab_login > C:\xampp\htdocs\laboratorio2\backup_lab_login.sql  

El archivo `backup_lab_login.sql` quedó guardado en la carpeta principal del proyecto y forma parte del repositorio.  

---

## 5. Dificultades y soluciones
Durante el desarrollo se presentaron varios problemas que fueron resueltos:  

El comando `php artisan` no funcionaba porque no se estaba dentro de la carpeta del proyecto.  
La solución fue ingresar a la ruta correcta (`cd laboratorio2`).  

La base de datos no podía crearse directamente en el CMD con el comando CREATE DATABASE.  
La solución fue dejar que Laravel la generara automáticamente al ejecutar las migraciones.  

El servicio de MySQL en XAMPP no iniciaba debido a conflictos en la carpeta `mysql/data`.  
La solución fue respaldar la carpeta, limpiarla y permitir que XAMPP regenerara los archivos necesarios.  

Hubo dudas al momento de ejecutar el servidor de Laravel y el compilador de Vite.  
La solución fue abrir dos ventanas de las terminal del cmd de windows y en cada uno correr cada cosa: una para `npm run dev` y otra para `php artisan serve`.  

---

## 6. Referencias
La elaboración de este laboratorio se apoyó en la siguiente documentación y recursos:  

https://laravel.com/docs  
https://www.apachefriends.org/es/index.html  
https://getcomposer.org/  


---

## 7. Footer del laboratorio
Este laboratorio ha sido desarrollado por el estudiante de la Universidad Tecnológica de Panamá:  

Nombre: Manuel Campos  
Correo: manuel.campos1@utp.ac.pa
Curso: Ingeniería Web  
Instructor del Laboratorio: Irina Fong  
Fecha de Ejecución:  26 de septiembre de 2025  

## 8. Fecha de Ejecucion 
La elaboración de este laboratorio se realizo la siguiente fecha:

Fecha de Ejecución:  26 de septiembre de 2025  


## About Laravel

Laravel is a web application framework with expressive, elegant syntax. We believe development must be an enjoyable and creative experience to be truly fulfilling. Laravel takes the pain out of development by easing common tasks used in many web projects, such as:

- [Simple, fast routing engine](https://laravel.com/docs/routing).
- [Powerful dependency injection container](https://laravel.com/docs/container).
- Multiple back-ends for [session](https://laravel.com/docs/session) and [cache](https://laravel.com/docs/cache) storage.
- Expressive, intuitive [database ORM](https://laravel.com/docs/eloquent).
- Database agnostic [schema migrations](https://laravel.com/docs/migrations).
- [Robust background job processing](https://laravel.com/docs/queues).
- [Real-time event broadcasting](https://laravel.com/docs/broadcasting).

Laravel is accessible, powerful, and provides tools required for large, robust applications.

## Learning Laravel

Laravel has the most extensive and thorough [documentation](https://laravel.com/docs) and video tutorial library of all modern web application frameworks, making it a breeze to get started with the framework.

You may also try the [Laravel Bootcamp](https://bootcamp.laravel.com), where you will be guided through building a modern Laravel application from scratch.

If you don't feel like reading, [Laracasts](https://laracasts.com) can help. Laracasts contains thousands of video tutorials on a range of topics including Laravel, modern PHP, unit testing, and JavaScript. Boost your skills by digging into our comprehensive video library.

## Laravel Sponsors

We would like to extend our thanks to the following sponsors for funding Laravel development. If you are interested in becoming a sponsor, please visit the [Laravel Partners program](https://partners.laravel.com).

### Premium Partners

- **[Vehikl](https://vehikl.com)**
- **[Tighten Co.](https://tighten.co)**
- **[Kirschbaum Development Group](https://kirschbaumdevelopment.com)**
- **[64 Robots](https://64robots.com)**
- **[Curotec](https://www.curotec.com/services/technologies/laravel)**
- **[DevSquad](https://devsquad.com/hire-laravel-developers)**
- **[Redberry](https://redberry.international/laravel-development)**
- **[Active Logic](https://activelogic.com)**

## Contributing

Thank you for considering contributing to the Laravel framework! The contribution guide can be found in the [Laravel documentation](https://laravel.com/docs/contributions).

## Code of Conduct

In order to ensure that the Laravel community is welcoming to all, please review and abide by the [Code of Conduct](https://laravel.com/docs/contributions#code-of-conduct).

## Security Vulnerabilities

If you discover a security vulnerability within Laravel, please send an e-mail to Taylor Otwell via [taylor@laravel.com](mailto:taylor@laravel.com). All security vulnerabilities will be promptly addressed.

## License

The Laravel framework is open-sourced software licensed under the [MIT license](https://opensource.org/licenses/MIT).
