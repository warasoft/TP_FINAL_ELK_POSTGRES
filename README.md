# CAPTURA Y ALMACENAMIENTO DE DATOS
## Trabajo Práctico
### OBJETIVOS
El objetivo del siguiente trabajo es lograr comparar la performance entre una Base de Datos Relacional ***POSTGRESQL***, y herramientas alternativas de explotación de datos como por ejemplo ***ELASTICSEARCH***.

### CONTENIDOS

1. [INTRODUCCIÓN Y ANTECEDENTES](#HERRAMEINTAS)
2. [HERRAMIENTAS RELACIONADAS](#HERRAMEINTAS)
3. [PASOS PARA IMPLEMENTACIÓN](#PASOS)
4. [EVALUACIÓN PROPUESTA](#PROPUESTA)

### HERRAMIENTAS RELACIONADAS
* S.O. UBUNTU 20.04
* DOCKER
* DOCKER COMPOSE
* POSTGRES
* PGADMIN4 WEB
* ELASTICSEARCH
* LOGSTASH
* KIBANA

### PASOS PARA IMPLEMENTACIÓN


) Para obtener una versión estable de Docker debemos de actualizar los repositorios del Sistema Ubuntu. Aunque para obtener la última versión debemos añadir el repositorio oficial de docker, para ello podemos seguir la guía oficial de docker.

- sudo apt-get update

Lo siguiente a realizar es la instalación del programa docker, para ello debemos de instalar dos paquetes, docker y docker.io.

- sudo apt-get install docker docker.io

Continuamos con la instalación de docker-compose
- sudo apt-get install docker-compose

) Descargar el archivo comprido "docker-elk-main.zip"
  - Extraer el contenido en un lugar de facil acceso (/Escritorio)

) Levantamos el docker-compose (elasticsearch, kibana, logstash, postgres, pgadmin4)
  - docker-compose up

### ENLACES DE INTERES

- https://github.com/deviantony/docker-elk.git
