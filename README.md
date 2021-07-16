:spring_version: current
:toc:
:project_id: dynfi docker
:icons: font
:source-highlighter: prettify

This guide walks you through the process of building a https://docker.com[Docker] image for running a Spring Boot application with mongo database.

== Instalar Docker

Instalar Docker en Centos
include::https://docs.docker.com/engine/install/centos/
Instalar docker en Ubuntu
include::https://docs.docker.com/engine/install/ubuntu/

[[Clonar]]
== Instalacion de App Dynfi

Clonar el directorio de la siguiente forma:
----
git clone git@github.com:themendas/DynFi.git
----
[[initial]]
== Instalacion de App Dynfi

Ejecutar el siguiente comando:
----
docker up -d
----

[subs="attributes"]
----
./mvn package && java -jar target/spring-boot-mongo-docker-1.0.0.jar
----

and go to http://localhost:8080/customer/ to see your persisted customers.

== Containerize It

If you want to run with Docker, execute:

[subs="attributes"]
----
./docker-compose up
----


== Summary

Congratulations! You've just created a Docker container for a Spring Boot app! Spring Boot apps run on port 8080 inside the container by default and we mapped that to the same port on the host using "-p" on the command line.

== Ver Tambien:

Para mas ayuda puedes consultar los siguientes apartados del fabricante

* https://dynfi.com/

Para la documentacion sobre la aplicacion

* https://dynfi.com/documentation/index.html

