FROM mongo

MAINTAINER ivan.matrinezvillanueva@alu.uclm.es

#data/db será el volumen usado para la persistencia de sesión
COPY drop/* usr/local/data/lb


#CMD es lo mismo que ENTRYPOINT pero con otro formato
CMD ["mongod", "--smallfiles", "--rest"]