FROM openjdk:8-jre

MAINTAINER ivan.matrinez@alu.uclm.es

RUN mkdir -p /usr/local/app

WORKDIR /usr/local/app

#Copia el .jar del servicio a la imagen. No se indica el nombre porque las versiones pueden cambiar
COPY drop/*.jar usr/local/app/

#Copia el script que se ejecutará al lanzar el contenedor
COPY drop/run.sh /usr/local/app/run.sh

#Si ejecutamos la imagen en local, el servicio tendría acceso local a la ip del host de Mongo
#Como lo ejecutamos como pila de serviios Docker, le tenemos que pasar la IP en un archivo de propiedades
COPY drop/application.properties application.properties

EXPOSE 8080

ENTRYPOINT sh usr/local/app/run.sh
