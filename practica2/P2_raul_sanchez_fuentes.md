# Práctica 2   

## Probar el funcionamiento de la copia de archivos por ssh.  

Mediante el comando: tar czf - directorio | ssh equipodestino 'cat > ~/tar.tgz’, creamos una copia de la carpeta “pruebassh” del equipo raul, comprimida y almacenada como ~/tar.tgz en el equipo raul2.   

Nota: Las máquinas se llamaban ubuntu las dos, pero después de tomar las capturas ya las llamé: raul y raul2.   

![](https://github.com/RaulSFuentes/SWAP2015/blob/master/practica2/imagenes/1.png)   

![](https://github.com/RaulSFuentes/SWAP2015/blob/master/practica2/imagenes/2.png)



Para clocar una carpeta utilizamos el comando rsync, en las capturas se ven las vertientes de sin opciones o con opciones.   


![](https://github.com/RaulSFuentes/SWAP2015/blob/master/practica2/imagenes/3.png)  


![](https://github.com/RaulSFuentes/SWAP2015/blob/master/practica2/imagenes/4.png)   


Primeramente generaremos la clave con ssh-keygen como se ve en la captura:   

![](https://github.com/RaulSFuentes/SWAP2015/blob/master/practica2/imagenes/5.png)   

Después copiaremos la clave en el equipo raul (192.168.121.252), y hacemos una prueba para comprobar que no nos pide ssh.   

![](https://github.com/RaulSFuentes/SWAP2015/blob/master/practica2/imagenes/6.png)   


Para establecer la tarea escribimos en el fichero /etc/crontab una nueva línea como la última que aparece en la captura, en la que indicamos que cada minuto 0 de cada hora se realice una clonación de la carpeta /var/www.   

![](https://github.com/RaulSFuentes/SWAP2015/blob/master/practica2/imagenes/7.png)   