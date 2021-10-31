<div align="justify">

# Git
<div align="center">
   <img src="Img/Git.png"  width="300px">
 </div>
  
## Instalar Git en Ubuntu  
  
  1.	Primero verificamos si hay alguna versión de Git instalada en la maquina virtual para ello abrimos una terminal y escribimos el siguiente comando:
  
```
git --version
```
  
<div align="center">
  <img src="Img/1.png">
</div>  
  
 2.	Ahora procedemos a actualizar las herramientas de actualización de paquetes para ello utilizamos el comando:
  
```
sudo apt update
``` 
  
<div align="center">
  <img src="Img/2.png">
</div> 
  
 3.	Una vez actualizada la herramienta de paquetes. Procedemos a instalar Git para ello introducimos el siguiente comando en la terminal: 
  
```
sudo apt install git
``` 
  
<div align="center">
  <img src="Img/3.png">
</div> 
  
 4.	Una vez terminado el proceso de instalación, pasamos a confirmar que Git se instaló correctamente, para ello ejecutamos el siguiente comando:  
  
```
git --version
``` 
  
<div align="center">
  <img src="Img/4.png">
</div> 
  
## Instalación de Git desde la fuente: 
  
 1.	Primero comprobamos la versión de Git que tenemos instalada, para ello empleamos el siguiente comando:
  
```
git --version
```   

<div align="center">
  <img src="Img/4.png">
</div> 
  
 2.	Antes de comenzar, debemos instalar el software necesario para Git. Todo se encuentra disponible en los repositorios predeterminados, de modo que podemos actualizar nuestro índice local de paquetes y luego instalar los paquetes pertinentes. Para ello utilizamos los siguientes comandos.  
  
```
sudo apt update
sudo apt install libz-dev libssl-dev libcurl4-gnutls-dev libexpat1-dev gettext cmake gcc
```   
  
<div align="center">
  <img src="Img/5.png">
</div>  
<div align="center">
  <img src="Img/6.png">
</div> 
  
 3.	Tras haber instalado las dependencias necesarias, creamos un directorio temporal y nos desplazamos a dicho directorio. Aquí es donde descargaremos nuestro tarball de Git.  

```
mkdir tmp
cd /tmp
```   

<div align="center">
  <img src="Img/7.png">
</div> 
  
 4.	Ahora descargados la versión especifica de Git que queramos instalar en nuestro caso trabajaremos con la versión 2.29.3 para descargarlo utilizaremos curl y enviaremos a la carpeta el archivo que descarguemos a git.tar.gz, para ello utilizamos el siguiente comando.  
  
```
curl -o git.tar.gz https://mirrors.edge.kernel.org/pub/software/scm/git/git-2.29.3.tar.gz
```   
  
<div align="center">
  <img src="Img/8.png">
</div> 
  
 5.	Nos da un error porque no tenemos instalado el curl, asi que antes de seguir con la instalación procedemos a instalar curl, para ello usamos el siguiente comando.  
  
 ```
sudo snap install curl
```   
  
 6.	Una vez instalado Curl, volvemos a introducir el comando:  
  
<div align="center">
  <img src="Img/9.png">
</div> 
  
7.	Ahora descomprimimos el archivo tarball, una vez terminados nos desplazamos a la carpeta del nuevo directorio de Git.  
  
<div align="center">
  <img src="Img/10.png">
</div> 
  
 8.	Ahora podemos crear el paquete e instalarlo escribiendo estos dos comandos:  
  
```
make prefix=/usr/local all
sudo make prefix=/usr/local install
``` 
<div align="center">
  <img src="Img/11.png">
</div> 
<div align="center">
  <img src="Img/12.png">
</div>    
<div align="center">
  <img src="Img/13.png">
</div>    
<div align="center">
  <img src="Img/14.png">
</div>    
  
 9.	Una vez terminado el proceso, modificamos el proceso de Shell para que se utilice la versión de Git que acabamos de instalar, para ello usamos el siguiente comando:
  
 ```
 exec bash
```
  
<div align="center">
  <img src="Img/15.png">
</div> 
  
 10.	Una vez completado esto volvemos a verificar la versión instalada para verificar que se ha realizado el proceso correctamente para ello usaremos el siguiente comando:  
  
```
git --version
```   
  
<div align="center">
  <img src="Img/16.png">
</div>  
  
## Configuración de Git;  
  
 1.	Procedemos a configurar el nombre de usuario y el correo electrónico. Para ello emplearemos los siguientes comandos:  
  
```
git config --global user.name "Your Name"
git config --global user.email "youremail@domain.com"
```
  
<div align="center">
  <img src="Img/17.png">
</div> 
  
 2.	Podemos ver todos los elementos de configuración creados escribiendo lo siguiente:  
  
```
git config --list
```  
  
<div align="center">
  <img src="Img/18.png">
</div> 

 3.	También podemos editar esta información manualmente con un editor de texto para ello vamos a utilizar por ejemplo el nano y el siguiente comando:
  
```
nano ~/.gitconfig
```  
  
<div align="center">
  <img src="Img/19.png">
</div> 
</div>
