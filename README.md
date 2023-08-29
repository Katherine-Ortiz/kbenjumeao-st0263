# ST02363 Tópicos Especiales en Telemática

# Estudiante: Katherine Benjumea Ortiz, kbenjumeao@eafit.edu.co

# Profesor: Edwin Nelson Montoya Munera, emontoya@eafit.edu.co

# Reto 2


# 1. breve descripción de la actividad
Para este reto, se implementó lo siguiente:

- **Microservicio 1:** Este es encargado de listar archivos a través de gRPC. Tiene comunicación con el API Gateway.

- **Microservicio API Gateway:** Este es encargado de funcionar como gateway y también como un balanceador de cargas y proxy.

## 1.1. Qué aspectos cumplió o desarrolló de la actividad propuesta por el profesor (requerimientos funcionales y no funcionales)

- Implementación microservicio 1.
- Comunicación vía gRPC para el microservicio 1.
- Implementación microservicio API Gateway.
- Comunicación API Rest entre cliente y API Gateway.
- Archivos de configuración .env.
- Implementación de endpoints para listar archivos.

## 1.2. Que aspectos NO cumplió o desarrolló de la actividad propuesta por el profesor (requerimientos funcionales y no funcionales)

Se hizo el intento de implementar el microservicio 2 que es el encargado de buscar los archivos a traves de RabbitMQ, pero no se logra establecer conexión para su adecuado funcionamiento. 
No se logró dockerizar por diversos problemas presentados en el ambiente de desarrollo.

# 2. información general de diseño de alto nivel, arquitectura, patrones, mejores prácticas utilizadas.

En la arquitectura del proyecto se observan 2 componentes en el desarrollo de este mismo, se describen a continuación:

1. API Gateway.
2. Microservicio 1 con Grpc

- Se utiliza Python como lenguaje de programación.

En el proyecto un cliente puede hacer una petición mediante su navegador web, o mediante desde Postman. Éste se comunica mediante el API Rest. El API Gateway a su vez se comunica mediante gRPC con el primer microservicio, el cual tiene la función de listar los archivos disponibles. El microservicio de buscar un archivo se buscó ser implementado con MOM a través de RabbitMQ. Luego de varias pruebas no se logra establecer comunicación. Se crea la cola en la interfaz al ejecutar y correr el consumidor, pero no logra entrar el query enviado. 

![](./imagenes/rabbit.jpg)


# 3. Descripción del ambiente de desarrollo y técnico: lenguaje de programación, librerias, paquetes, etc, con sus numeros de versiones.

Todos los servicios fueron implementados con Python 3.11.4.

    Flask==2.3.3



