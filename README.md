# Apache

![image](/img/apache-releases-update-for-leading-http-server-showcase_image-2-a-18208.jpg)

## 1.- Instalación de Apache y ficheros de configuración.

```sh
# apt-get update
# apt-get install apache2
```
 
 - Para trabajar con el servicio de apache utilizaremos los siguientes comandos.
  
```sh
$ service apache2 start  --> para arrancar

$ service apache2 stop  --> para pararlo

$ service apache2 restart --> reinicia ( equivalente a hacer stop y luego start )

$ service apache2 reload --> recargar la configuración

$ service apache2 status --> comprobamos el estado del servicio
```

![image](/img/apache1.png)

- Otra forma de comprobar que nuestro servidor apache esta en funcionamiento es yendo a un navegador y poner localhost en el buscador. También se puede acceder desde fuera de la maquina visrtual poniendo en el navegador la ip de nuestro servidor apache.

- Esta página web que nos muestra en el navegador se encuentra en la ruta  `# cd /var/www/html` , dentro encontraremos un fichero index.html, que es la configuración html de la página web que nos muestra por defecto. Si queremos lo podemos modificar a través del editor de textos nano.

- Los ficheros de configuración se encuentran en  ``` /etc/apache2 ```
- También existe otro comando para comprobar que no existen errores de sintaxis en los ficheros de configuración:
  
  ``` # apache2ctl -t ```

## 2.- Creación de un sitio virtual

Los sitios virtuales permiten que un único servidor Apache pueda servir a las páginas de varios dominios. Esto es posible gracias a que los navegadores envían siempre una cabecera Host que permite saber al servidor cuál es el dominio que se está solicitando.

- Primer paso para crear sitios virtuales
  Como no disponemos de dominios registrados en internet lo que vamos a hacer es simularlos, para ello lo que podemos hacer es editar el siguiente fichero ``` # nano /etc/hosts ``` y vamos a poner que con la ip 127.0.0.1 somos www.larry1.com y www.larry2.com. Para comprobarlo solo tenemos que hacen un ``` ping www.larry1.com y ping wwww.larry2.com ``` y veremos que nos responderá.

![image](/img/apache2.png)

![image](/img/apache3.png)

- Segundo paso crear dos carpetas con e comando `# mkdir larry1 larry2` en la ruta `# cd /var/www`. Dentro de estas carpetas creamos un archivo index.html y lo editamos.

![image](/img/apache4.png)

![image](/img/apache5.png)

- Tercer paso nos dirigiremos a `/etc/apache2/sites-available` ahí encontraremos dos ficheros de configuración y copiamos uno de ellos en otros ficheros de configuracion que llevan el nombre de nuestro sitio virtual, y accederemos con nano a los archivos de configurción.

```sh
# cp 000-default.cont larry1.conf
# cp 000-default.cont larry2.conf
```

![image](/img/apache6.png)
![image](/img/apache7.png)

- Cuarto: Accedemos a los archivos con nano y modidificamos dos apartados, ServerName y DocumentRoot

![image](/img/apache8.png)




