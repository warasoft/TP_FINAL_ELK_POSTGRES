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

3) Levantar ambiente de trabajo

Para preparar el ambiente de trabajo se tomó como base un proyecto del repositorio [Docker-elk](https://github.com/caas/docker-elk.git). Al mismo se le modificó y agregó ciertos parametros para cumplir con lo propuesto en el presente trabajo.

  * Eliminación del directorio "logstash":
    - La herramienta "logstash" se descargará e instalará por separado y de forma local en la pc anfitrion.
    - Descargar el archivo .zip del siguiente link: https://www.elastic.co/es/downloads/past-releases/logstash-6-6-0
    - 

  * Modificaciones a logstash:
    - En el directorio "*j@jlinux:~/Escritorio/docker-elk-main/logstash/config$*", se modificó el archivo "*logstash.yml*" cambiandole usuario "*xpack.monitoring.elasticsearch.username: test*" y "*xpack.monitoring.elasticsearch.password: test*".
    - En el directorio "*j@jlinux:~/Escritorio/docker-elk-main/logstash/pipeline$*", se modificó el archivo "*logstash.conf*" modificando los comando para conectar con la base de datos Postgres "*xxxxxxxxxxxxxxxx*".

  * Modificaciones al archivo "*docker-compose*" del directorio "*docker-elk-main*":
    - Se agrego los comandos para la creacion de dos contenedores, uno para una base de datos Postgres y otro para la interfaz web del cliente (usuario: test@test.com y password: test).

Continuando con la creación del ambiente de trabajo, se procede a levantar todo el entorno.

  * 3.a) Descargar los archivos compridos "docker-postgres" y "docker-elastic-kibana.zip", los mismos se encuentran en la raíz del repositorio.
  * 3.b) Extraer el contenido de ambos archivos .zip, en un lugar de facil acceso (Ejemplo: /Escritorio).
  * 3.b) Abrir el directorio "docker-elastic-kibana" en una terminal (Ejemplo: j@jlinux:~/Escritorio/docker-elastic-kibana$)
  * 3.c) Ejecutar el comando docker-compose:

         sudo docker-compose up -d

4) Creación e importacion de la Base de datos Postgres

<img src="https://github.com/warasoft/tp_final/blob/main/bd%20creator.gif" style="max-width: 80%">

### EVALUACION Y PROPUESTA


### ENLACES DE INTERES

- https://github.com/deviantony/docker-elk.git
- https://docker.com/
- https://hub.docker.com/
- https://www.elastic.co/es/



