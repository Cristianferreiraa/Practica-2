Manual de instalación de ownCloud Server en Ubuntu 24.04

Paso 1: Descargar el archivo .zip de ownCloud Server

![imagen](0.png)

Paso 2: Instalar la versión 7.4 de PHP

![imagen](1.png)

Actualizar las listas de paquetes y actualizar todos los paquetes existentes:

![imagen](2.png)


Instalar los requisitos previos de PPA:
Seleccionar la versión de PHP que se desea utilizar:


![imagen](3.png)

![imagen](4.png)

Agregar el repositorio de PHP 7.4:

Actualizar los repositorios:


Seleccionar la versión de PHP que se desea utilizar:
Reiniciar Apache2:
![imagen](5.png)

Paso 3: Instalar Apache2, MySQL y algunas bibliotecas

Actualizar la máquina:

![imagen](6.png)


Instalar el servidor web Apache2:

Instalar el servidor de bases de datos MySQL:


![imagen](7.png)


Instalar algunas bibliotecas de PHP:

![imagen](8.png)


Reiniciar el servidor Apache2:

![imagen](9.png)


Paso 4: Configurar MySQL

Acceder a la consola de MySQL:

![image](10.png).

Crear la base de datos:

Crear un usuario:

Dar permisos al usuario:

Salir de la base de datos:
![image](11.png).
![image](12.png).




Probar la conexión a la base de datos:
![image](13.png).

Paso 5: Descargar los archivos de la aplicación web

Descargar los archivos de la aplicación web:
sudo cp ~/Baixades/app-web.zip /var/www/html
Ir al directorio /var/www/html:
cd /var/www/html
Descomprimir el archivo:
sudo unzip app-web.zip

NO PONGO CAPTURA DE ESTOS PASOS PORQUE LE HE DADO SINQUERER Y EL UNZIP ME LO A LLENADO Y NO VEO LOS COMANDOS.

Copiar los archivos a la carpeta /var/www/html:

![image](14.png).


Eliminar la carpeta creada al descomprimir:
sudo rm -rf app-web/
Eliminar el archivo index.html de Apache2:
sudo rm -rf /var/www/html/index.html
Paso 6: Aplicar permisos a las aplicaciones web

Ir al directorio /var/www/html:
cd /var/www/html
Aplicar permisos:
sudo chmod -R 775 .
sudo chown -R usuario:www-data .
Paso 7: Acceder al navegador y configurar la nube

Acceder al navegador y configurar la nube:
http://localhost
Crear un usuario admin y configurar la base de datos:
usuari: usuario
contrasenya: password
base de dades: bbdd
domini: localhost
Fin

Si todo ha ido bien, se debería ver el instalador de la aplicación web que se ha descargado y te pedira crear un usuario admin y configurar la base de datos.
