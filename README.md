# CAPTURA Y ALMACENAMIENTO DE DATOS
## Trabajo Práctico
### OBJETIVOS
El objetivo del siguiente trabajo es lograr comparar la performance entre una Base de Datos Relacional ***POSTGRESQL***, y herramientas alternativas de explotación de datos como por ejemplo ***ELASTICSEARCH***.

### CONTENIDOS

1. [INTRODUCCION Y ANTECEDENTES](#INTRODUCCION-Y-ANTECEDENTES)
2. [HERRAMIENTAS RELACIONADAS](#HERRAMIENTAS-RELACIONADAS)
3. [PASOS PARA IMPLEMENTACION](#PASOS-PARA-IMPLEMENTACION)
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

### PASOS PARA IMPLEMENTACION

1) Instalación de docker  y docker compose.

Para obtener una versión estable de Docker debemos de actualizar los repositorios del Sistema Ubuntu. Aunque para obtener la última         versión debemos añadir el repositorio oficial de docker, para ello podemos seguir la guía oficial de [Docker](http://docker.com).

- sudo apt-get update

Instalación de docker, para ello debemos de instalar dos paquetes, docker y docker.io.

- sudo apt-get install docker docker.io

Continuamos con la instalación de docker-compose

- sudo apt-get install docker-compose

3) Levantar ambiente de trabajo

Para preparar el ambiente de trabajo se tomó como base un proyecto del repositorio [Docker-elk](http://github.com/deviantony/docker-elk.git). Al mismo se le modificó y agregó ciertos parametros para cumplir con lo propuesto en el presente trabajo.

Modificaciones puntuales:
  . kibana: directorio: j@jlinux:~/Escritorio/docker-elk-main/kibana/config$
            archivo: kibana.yml 
              * elasticsearch.username: test
              * elasticsearch.password: test

  * 3.a) Descargar el archivo comprido "docker-elk-main.zip", el mismo se encuentra en la raíz del repositorio.
  * 3.b) Extraer el contenido en un lugar de facil acceso (Ejemplo: /Escritorio).
  * 3.b) Abril al directorio "docker-elk-main" en una terminal (Ejemplo: j@jlinux:~/Escritorio/docker-elk-main$ )
  * 3.c) Ejecutar el comando docker-compose (sudo docker-compose up).

### EVALUACION Y PROPUESTA


### ENLACES DE INTERES

- https://github.com/deviantony/docker-elk.git
- https://docker.com/
- https://hub.docker.com/
- https://www.elastic.co/es/
