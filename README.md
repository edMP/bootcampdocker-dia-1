# bootcampdocker-dia-1
con docker pull httpd:latest descargamos la ultima imagen de httpd que exista en docker hub 

docker hub repositorio de imágenes docker 

mediante docker build podemos crear nuestras propias imágenes con -t o --tag le daremos el nombre que queramos 

para ver las imágenes que tenemos creadas usaremos docker image ls
si queremos borrar alguna usaremos rmi nombre de la imagen -f o --force si no permite borrarla, se tiene que tener en cuenta que si existe un contenedor activo que la use no podremos borrar la imagen 

para crear un contendor que use una imagen empelaremos doceker run con --name le pondremos un nombre a el contenedor de lo contrario docker le podrá el que quiera,
-d nos permite levantarlo en segundo plano y por último le tendremos que decir la imagen a utilizar.
Quedaría algo como docker run -d --name test httpd:latest

Tambien le podremos indicar en que puerto queremos que se levante com 80:80 docker ps muestras los contendores activos con -a dara una vista más detallada 

docker stop y el nombre o el identificador detendrá el contendor 

mediante un docker file podemos crear una imagen personal con las opciones de arranque que queramos en estes caso es una imagen de httpd from httpd:latest que genera un index.html en la carpeta index.hmtl del contenedor(sino esta la crea) con un hola mundo COPY ./index.html /home/devops/html/index.html 

 

 
