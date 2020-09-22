# Glen's Boutique

E-commerce de ropa interior femenina.

https://glenboutique.vercel.app/

En construcción actualmente, trabajando sobre la maquetacion utilizando el framework de bootstrap para ciertas secciones de la página y esquematizando sección por sección para definir la distribución correcta de la información, teniendo en cuenta el formato de un e-commerce.

Para poder trabajar con SASS, es necesario primero instalar NodeJS desde la pagina oficial:
1- https://nodejs.org/es/
2- instalar npm
    Corroborar en consola si esta instalado y la version seleccionada de instalación.
3- Una vez instalado NodeJS, corroborar en consola la versión de npm que trae el paquete de Node. ej: 6.14.4
4- Para poder utilizar NodeJS e iniciar el npm, es necesario ir a la carpeta del proyecto desde la terminal.
5- Una vez en el directorio correcto, ejecuta el comando npm init. Se te pedirá responder varias preguntas sobre el proyecto, después de las cuales NPM generará un archivo package.json en tu directorio. (En este caso no es necesario ingresar los datos que va pidiendo, ya que estan ingresados previamente.)
6- Instalar Nodemon:
    EL nodemon es el que va a monitorear los cambios en el código fuente, nuestro SASS,  que se está desarrollando y automáticamente reinicia el servidor para generar el CSS.  

Node-sass se usará para compilar tus archivos scss en archivos css. 
Nodemon es algo que usaremos para ver los cambios en nuestros archivos scss. 

Normalmente, se usa para detectar cambios en el código Node.js del lado del servidor.

Para instalar nuestras dependencias (node-sass y nodemon) ejecutaremos el siguiente comando en la terminal:  npm install -D node-sass nodemon

	Al final se observa que se creó la carpeta de node_modules y el archivo package-lock.json
  
10- para compilar el codigo es necesario hacerlo desde la consola siguiendo el siguiente comando:  
      run watch-css
      
Cabe destacar que no es necesario modificar el package.json, ya que viene premodificado por mi cuenta.
De todas formas, no van a estar incluidos por una cuestion de privacidad y de accesos a datos sensibles.

De querer poder trabajar sobre el codigo va a ser necesario modificar el archivo .json que se genere al instalar el npm y nodemon.
La forma es la siguiente:
  Editar el package.json e insertar los lineas
    "build-css": "node-sass --include-path scss scss/miarchivoSCSS.scss css/miarchivoCSS.css",
    "watch-css": "nodemon -e scss -x \"npm run build-css\""
Tomar en cuenta que "miarchivoCSS.css" es en modo de ejemplo, modificarlo por el archivo que va a compilar nuestro SCSS. Ej: css/style.css.

Cualquier comentario o ayuda que se quiera brindar para poder terminar con este e-commerce, es totalmente bienvenida.


Los avances van a poder apreciarse a medida que se vaya actualizando el repositorio, entrando al link del hosteo provisorio en Vercel.
