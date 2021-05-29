# CAPTURA Y ALMACENAMIENTO DE DATOS
## Trabajo Práctico
### OBJETIVOS
El objetivo del siguiente trabajo es lograr comparar la capacidad de respuesta entre una Base de Datos Relacional ***POSTGRESQL***, y herramientas alternativa de explotación de datos como por ejemplo ***ELASTICSEARCH***.

### CONTENIDOS

1. [INTRODUCCION Y ANTECEDENTES](#INTRODUCCION-Y-ANTECEDENTES)
2. [HERRAMIENTAS RELACIONADAS](#HERRAMIENTAS-RELACIONADAS)
3. [PASOS PARA LA IMPLEMENTACION](#PASOS-PARA-LA-IMPLEMENTACION)
4. [EVALUACION Y PROPUESTA](#EVALUACION-Y-PROPUESTA)
5. [ENLACES DE INTERES](#ENLACES-DE-INTERES)

### INTRODUCCION Y ANTECEDENTES

### HERRAMIENTAS RELACIONADAS
* S.O. UBUNTU 20.04
* DOCKER
* DOCKER COMPOSE
* POSTGRES
* PGADMIN4 WEB
* ELASTICSEARCH
* LOGSTASH
* KIBANA

### PASOS PARA LA IMPLEMENTACION

1) Instalación de docker  y docker compose.

Para obtener una versión estable de Docker debemos de actualizar los repositorios del Sistema Ubuntu. Aunque para obtener la última         versión debemos añadir el repositorio oficial de docker, para ello podemos seguir la guía oficial de [Docker](http://docker.com).

         sudo apt-get update

Instalación de docker, para ello debemos de instalar dos paquetes, docker y docker.io.

         sudo apt-get install docker docker.io

Continuamos con la instalación de docker-compose

         sudo apt-get install docker-compose

2) Levantar ambiente de trabajo

Para preparar el ambiente de trabajo se tomó como base un proyecto del repositorio [Docker-elk](https://github.com/caas/docker-elk.git). EL mismo fué modificado para cumplir con lo propuesto en el presente trabajo.
A continuacíon se desatalla los pasos a seguir:

  * 2.a) Descargar los archivos compridos "docker-elastic-kibana.zip" y "docker-postgres", los mismos se encuentran en la raíz del repositorio.
  * 2.b) Extraer en un lugar de facil acceso (Ejemplo: /Escritorio), el contenido de ambos archivos .zip.
  * 2.c) Para crear los contenedores de "Elasticsearch" y "kibana", abrir el directorio "docker-elastic-kibana" en una terminal (Ejemplo: j@jlinux:~/Escritorio/docker-elastic-kibana$)
  * 2.c) Ejecutar el comando docker-compose:
         
         sudo docker-compose up -d

  * 2.d) Crear base de datos "Postgres" y acceso a cliente "Pgadmin", abrir el directorio "docker-postgres" en una terminal (Ejemplo: j@jlinux:~/Escritorio/docker-postgres$)
  * 2.e) Ejecutar el comando docker-compose:

         sudo docker-compose up -d

<img src="https://github.com/warasoft/tp_final/blob/main/bd%20creator.gif" style="max-width: 80%">

   
  * 2.f) La herramienta "logstash" se descargará e instalará por separado y de forma local en la pc anfitrion.

    - "Logstash-6.6.0", link: https://www.elastic.co/es/downloads/past-releases/logstash-6-6-0, descargar el .zip.
    
    

  * Modificaciones a logstash:
    - En el directorio "*j@jlinux:~/Escritorio/docker-elk-main/logstash/config$*", se modificó el archivo "*logstash.yml*" cambiandole usuario "*xpack.monitoring.elasticsearch.username: test*" y "*xpack.monitoring.elasticsearch.password: test*".
    - En el directorio "*j@jlinux:~/Escritorio/docker-elk-main/logstash/pipeline$*", se modificó el archivo "*logstash.conf*" modificando los comando para conectar con la base de datos Postgres "*xxxxxxxxxxxxxxxx*".

  * Modificaciones al archivo "*docker-compose*" del directorio "*docker-elk-main*":
    - Se agrego los comandos para la creacion de dos contenedores, uno para una base de datos Postgres y otro para la interfaz web del cliente (usuario: test@test.com y password: test).

Continuando con la creación del ambiente de trabajo, se procede a levantar todo el entorno.

  




### EVALUACION Y PROPUESTA


### ENLACES DE INTERES

- https://github.com/caas/docker-elk.git
- https://docker.com/
- https://hub.docker.com/
- https://www.elastic.co/es/
- https://www.elastic.co/es/downloads/past-releases/logstash-6-6-0
- http://www.java2s.com/ref/jar/download-postgresql4221jar-file.html



