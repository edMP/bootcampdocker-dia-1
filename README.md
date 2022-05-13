# bootcampdocker-dia-1
con docker pull httpd:latest descargamos la ultima imagen de httpd que exista en docker hub

docker hub repositorio de imagenes docker

medainte docker build podemos crear nuestras propias imagenes con -t o --tag le daremos el nombre que queramos 

para ver las imagenes que temnemos creadas usaremos docker image ls
si queremos borrar alguna usaremos rmi nombre de la imagen -f o --force si no no permite borarla, setiene que tener encuenta que si existe un contedor actibo que la user no podremos borrar la imagen 

para crear un contendor que use una imagen empelaremos doceker run  con --name le pondremos un nombre a el contenedor de lo contrario docker le podnra el que quiera, -d nos permite levantarlo en segundo pano y por ultimo le tendremos que decir la imagen a utilizar quedaria algo como 
docker run -d --name test httpd:latest tambien le podremos indicar en que peurto queremos que se elvante com 80:80 
docker ps meutras los conendores actibos con -a dara una vista mas detallada

docker stop y el nombre o el identificador detendra el contendor  

medainte un docker file poremos crear  una imagen personal con las opciones de arranque que queramos en estes caso
es una imagen de httpd
from httpd:latest
que genera un index.html en la carpeta index.hmtl del conenedor(sino esta la crea) con un hola mundo 
COPY ./index.html /home/devops/html/index.html

