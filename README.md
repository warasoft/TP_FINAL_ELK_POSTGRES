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
* POSTGRES latest
* PGADMIN4 WEB latest
* ELASTICSEARCH 6.6.0
* LOGSTASH 6.6.0
* KIBANA 6.6.0

Características de la computadora de prueba:
- S.O. Ubuntu 20.04.
- Intel Core I5.
- 4 Gb RAM.
- 30 Gb Hard Disk.

### PASOS PARA LA IMPLEMENTACION

1) Instalación de Docker  y Docker Compose.

Para obtener una versión estable de Docker debemos de actualizar los repositorios del Sistema Ubuntu. Aunque para obtener la última         versión debemos añadir el repositorio oficial de docker, para ello podemos seguir la guía oficial de [Docker](http://docker.com).

         sudo apt-get update

Instalación de *"docker"*, para ello debemos de instalar dos paquetes, docker y docker.io.

         sudo apt-get install docker docker.io

Continuamos con la instalación de *"docker-compose"*

         sudo apt-get install docker-compose

2) Levantar ambiente de trabajo

Para preparar el ambiente de trabajo se tomó como base un proyecto del repositorio [Docker-elk](https://github.com/caas/docker-elk.git). EL mismo fué modificado para cumplir con lo propuesto en el presente trabajo.
A continuacíon se desatallan los pasos a seguir:

  * 2.a) Descargar los archivos comprimidos *"docker-elastic-kibana.zip"* y *"docker-postgres"*, los mismos se encuentran en la raíz del repositorio.
  * 2.b) Extraer  el contenido de ambos archivos .zip, en un lugar de facil acceso (Ejemplo: /Escritorio).
  * 2.c) Para crear los contenedores de *"Elasticsearch"* y *"kibana"*, abrir el directorio "docker-elastic-kibana" en una terminal (Ejemplo: j@jlinux:~/Escritorio/docker-elastic-kibana$).
    - Ejecutar el comando docker-compose:
         
                  sudo docker-compose up -d

  * 2.d) Crear base de datos *"Postgres"* y acceso a cliente *"Pgadmin"*, abrir el directorio *"docker-postgres"* en una terminal (Ejemplo: j@jlinux:~/Escritorio/docker-postgres$).
    - Ejecutar el comando docker-compose:

                  sudo docker-compose up -d
   
  * 2.e) La herramienta *"logstash"* se descargará e instalará por separado y de forma local en la pc anfitrion.

    - "Logstash-6.6.0", link: https://www.elastic.co/es/downloads/past-releases/logstash-6-6-0, descargar el .zip.
    - Extraer el contenido del .zip en un lugar de facil acceso (Ejemplo: /Escritorio).
    - Dirigirse a la carpeta *"../logstash-6.6.0/bin/"* y pegar los siguientes archivos: *"query.sql"* y *"logstash-sample.conf"* (ambos se pueden descargar de la carpeta "*Archivos para Logstash*").
    - Descargar el archivo [postgresql-42.2.1.jar](http://www.java2s.com/ref/jar/download-postgresql4221jar-file.html), y copiarlo *"../logstash-6.6.0/bin/"*.

3) Conexión a la Base de Datos *"PostgreSql"* e importación de datos de pruebas Senasa.

<img src="Gif's/pgadmin importacion.gif" style="max-width: 50%">

4) Transacción de datos del *"PostgreSql"* al *"ElasticSearch"* mediante *"Logstash"*.

   - Abrir el directorio "*logstash-6.6.0*" en una terminal (Ejemplo: j@jlinux:~/Escritorio/logstash-6.6.0$).
   - Ejecutar los siguientes comandos:

         j@j:~/Escritorio/logstash-6.6.0$ cd bin
         j@j:~/Escritorio/logstash-6.6.0/bin$ ./logstash -f logstash-sample.conf
         
         
<img src="Gif's/logstash exec.gif" style="width: 50%">
         
5) Creación de índices en "*Kibana*" para la muestra de datos de la base *"SENASA"*.

<img src="Gif's/kibana patron.gif" style="max-width: 50%">


### EVALUACION Y PROPUESTA


### ENLACES DE INTERES

- https://github.com/caas/docker-elk.git
- https://docker.com/
- https://hub.docker.com/
- https://www.elastic.co/es/
- https://www.elastic.co/es/downloads/past-releases/logstash-6-6-0
- http://www.java2s.com/ref/jar/download-postgresql4221jar-file.html



