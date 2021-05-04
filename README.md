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

La API está escrita en Python y SQL.

La API se utiliza para buscar, actualizar y eliminar contenido de la base de datos. Devuelve respuestas JSON y maneja los métodos GET, POST, PUT y DELETE.


[See API code here](https://github.com/musevarg/Transportation-Management-System/blob/master/API-and-Admin-Panel/App/App/API/RestAPI.py).

A continuación se muestra una salida de muestra para cada método de solicitud:
![](https://raw.githubusercontent.com/musevarg/Transportation-Management-System/master/pic1.png)

### 2. Panel de Administrador

El panel de administración permite que un usuario administrador actualice la base de datos MySQL. El administrador puede agregar, eliminar y modificar registros.

Se desarrolla usando * HTML *, * CSS *, * JavaScript * y * jQuery * para realizar llamadas a la API. Hace un uso extensivo de bootstrap y la API anterior.

También contiene una pantalla de tablero que le permite al administrador verificar los ingresos mensuales y las tarifas mensuales (combustible, almuerzo, MOT).


[See Admin Panel code here](https://github.com/musevarg/Transportation-Management-System/tree/master/API-and-Admin-Panel/App/App/AdminPanel).

![](https://raw.githubusercontent.com/musevarg/Transportation-Management-System/master/pic2.png)

### 3. Aplicación Android

La API permite la autenticación de usuarios y también proporciona contenido a la aplicación nativa. Permite a los conductores de reparto iniciar sesión y ver qué vehículo se les ha asignado, cuántos trabajos se les han asignado y les permite marcar un trabajo como completado. Esto actualiza el estado del trabajo en la base de datos y carga una imagen del paquete y la firma del cliente. También permite cargar recibos. Este contenido se puede recuperar en el panel de administración.

[See Android App code here](https://github.com/musevarg/Transportation-Management-System/tree/master/Drivers-Android-App/app/src/main).

![](https://raw.githubusercontent.com/musevarg/Transportation-Management-System/master/pic3.png)

### 4. Sitio web de clientes

Este sencillo sitio web proporciona información sobre la empresa y permite a los usuarios realizar un seguimiento de su paquete (la API se utiliza para eso).

[See website code here](https://github.com/musevarg/Transportation-Management-System/tree/master/API-and-Admin-Panel/App/App/Website).

Below is an example of a parcel being tracked:
![](https://raw.githubusercontent.com/musevarg/Transportation-Management-System/master/pic4.png)
