# Apache

![image](/img/apache-releases-update-for-leading-http-server-showcase_image-2-a-18208.jpg)

## 1.- Instalación de Apache y ficheros de configuración.

``` #apt-get update ```

``` #apt-get install apache2 ```

 - Los ficheros de configuracion se encuentran en  ``` /etc/apache2 ```
 
 - Para trabajar con el servicio de apache utilizaremos los siguientes comandos.
  
``` service apache2 start  --> para arrancar ```

``` service apache2 stop  --> para pararlo ```

``` service apache2 restart --> reinicia ( equivalente a hacer stop y luego start ) ```

``` service apache2 reload --> recargar la configuración ``` 

``` service apache2 status --> comprobamos el estado del servicio ```

![image](/img/apache1.png)


- Otra forma de comprobar qiue nuestro apache esta en funcionamiento es yendo a un navegador y poner localhost en el navegador. También se puede acceder desde fuera de la maquina visrtual poniendo en el navegador la ip de nuestro servidor apache.

  
