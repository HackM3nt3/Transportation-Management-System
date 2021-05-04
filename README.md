Este proyecto ganó [Napier University Group Project Awards](https://www.napier.ac.uk/about-us/our-schools/school-of-computing/student-stories/computershare-awards-2020).

# Transportation Management System - Sistema de manejo para Transportadores

Este proyecto es una suite completa para una empresa de transporte de vehículos. Incluye:

 - Sitio web de los clientes: información general sobre la empresa y la opción de seguimiento de paquetes.
 - Panel de administración: permite a un usuario administrador administrar toda la base de datos en un entorno amigable para el usuario y también proporcionar aplicaciones   orientadas al negocio (descripción general de ingresos y gastos, asignación y administración de trabajos y conductores)
 - Aplicación de conductores: aplicación de Android que permite a los conductores ver los trabajos y el vehículo que se les asignó, marcar trabajos como completados, solicitar la firma del cliente, cargar recibos e imágenes de vehículos en el servidor, etc.
 - API: el elemento fundamental que conecta y hace que los tres servicios anteriores funcionen


### 0. Servidor Web

El servidor web utiliza * Python FLASK *. Por lo tanto, la API, el panel de administración y el sitio web del cliente son aplicaciones Flask.
Toda la configuración utiliza planos separados en tres áreas. Se inicia una aplicación principal y las sub-aplicaciones (api, panel de administración y sitios web de clientes) se inician dentro de la aplicación principal.
* Python * se utiliza como lenguaje del lado del servidor.


[See App.py setup and blueprints registration here](https://github.com/musevarg/Transportation-Management-System/blob/master/API-and-Admin-Panel/App/App/App.py).

### 1. API

The API is written in *Python* and *SQL*.

The API is used to fetch, update and remove content from the database. It returns JSON responses and handles GET, POST, PUT and DELETE methods.

[See API code here](https://github.com/musevarg/Transportation-Management-System/blob/master/API-and-Admin-Panel/App/App/API/RestAPI.py).

Below is a sample output for each request method:
![](https://raw.githubusercontent.com/musevarg/Transportation-Management-System/master/pic1.png)

### 2. Admin Panel

The admin panel allows an admin user to update the MySQL database. The admin can add, remove and amend records.

It is developed using *HTML*, *CSS*, *JavaScript* and *jQuery* to perform API calls. It makes extensive use of bootstrap and the above API.

It also contains a dashboard screen that allows for the admin to check the monthly revenue and the monthly fees (fuel, lunch, MOT).

[See Admin Panel code here](https://github.com/musevarg/Transportation-Management-System/tree/master/API-and-Admin-Panel/App/App/AdminPanel).

![](https://raw.githubusercontent.com/musevarg/Transportation-Management-System/master/pic2.png)

### 3. Android Application

The API allows for users authentication and also provides content to the native application.
It allows for delivery drivers to log in and see what vehicle has been assigned to them, how many jobs have been assigned to them and allows them to mark a job as completed. This updates the status of the job in the database and uploads a picture of the parcel and the customer's signature.
It also permits for uploading receipts. This content can be retrieved in the admin panel.

[See Android App code here](https://github.com/musevarg/Transportation-Management-System/tree/master/Drivers-Android-App/app/src/main).

![](https://raw.githubusercontent.com/musevarg/Transportation-Management-System/master/pic3.png)

### 4. Customers Website

This simple website gives information about the company and allows sutomers to track their parcel (the API is used for that).

[See website code here](https://github.com/musevarg/Transportation-Management-System/tree/master/API-and-Admin-Panel/App/App/Website).

Below is an example of a parcel being tracked:
![](https://raw.githubusercontent.com/musevarg/Transportation-Management-System/master/pic4.png)
