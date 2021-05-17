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

1) Para obtener una versión estable de Docker debemos de actualizar los repositorios del Sistema Ubuntu. Aunque para obtener la última versión debemos añadir el repositorio oficial de docker, para ello podemos seguir la guía oficial de docker (#enlaces-de-interes).

- sudo apt-get update

Lo siguiente a realizar es la instalación del programa docker, para ello debemos de instalar dos paquetes, docker y docker.io.

- sudo apt-get install docker docker.io

Continuamos con la instalación de docker-compose
- sudo apt-get install docker-compose

) Descargar el archivo comprido "docker-elk-main.zip"
  - Extraer el contenido en un lugar de facil acceso (/Escritorio)

) Levantamos el docker-compose (elasticsearch, kibana, logstash, postgres, pgadmin4)
  - docker-compose up


### EVALUACION Y PROPUESTA


### ENLACES DE INTERES

- https://github.com/deviantony/docker-elk.git
- https://docker.com/
- https://hub.docker.com/
- https://www.elastic.co/es/
