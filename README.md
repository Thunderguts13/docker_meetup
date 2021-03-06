# docker_meetup

## Voraussetzungen

* [docker](https://docs.docker.com/install/linux/docker-ce/ubuntu/)
* [docker-compose](https://docs.docker.com/compose/install/)
* git

## Inhalt
* Was ist Docker
* Was sind Container
* Docker Aufbau
* Dockerfile
* Übung 1
* Docker-compose
* Übung 2
* Security

## Übung 1

Docker CLI kennenlernen

[Docker-cli Dokumentation](https://docs.docker.com/engine/reference/commandline/cli/)

1. ``` $ docker run -it --name meetup thunderguts13/docker_meet_up:latest ```
1. ``` $ docker ps ```
1. ``` $ docker images ```
1. ``` $ docker exec -it meetup /bin/sh ```
1. ``` $ docker kill meetup ```
1. ``` $ docker start -a meetup ```
1. ``` $ docker kill meetup ```
1. ``` $ docker run -it --name meetup thunderguts13/docker_meet_up:latest ```
1. ``` $ docker ps -a ```
1. ``` $ docker container rm meetup ```

## Übung 2

Dockerfile für Rails Applikation schreiben. Der Source Code ist im Ordner code abgelegt.

[Dockerfile Dokumentation](https://docs.docker.com/engine/reference/builder/)

1. Basis Image finden auf [Docker Hub](https://hub.docker.com/)
1. Code ins Image laden
1. Dependecys herunterladen
1. Startbefehl

## Übung 3

Docker-Compose für entweder Cryptopus mit MySql oder Pfeedbacktool.

[Docker-Compose Dokumentation](https://docs.docker.com/compose/compose-file/)

Env-Variablen für Cryptopus:

* RAILS_DB_USERNAME=root
* RAILS_DB_PASSWORD=change-me
* SECRET_KEY_BASE=change-me
* MYSQL_ROOT_PASSWORD=change-me-too
* RAILS_DB_ADAPTER: 'mysql2'
* RAILS_DB_HOST: 'cryptopus-mysql'
* RAILS_DB_NAME: 'cryptopus_prod'
* RAILS_DB_PORT: 3306

Infos:

* Datenbank: MySql
* Image: puzzle/cryptopus:stable

#### Quellen

* https://docs.docker.com
* https://wikipedia.org
* https://www.youtube.com/watch?v=EnJ7qX9fkcU
* https://www.opencontainers.org/
* https://jonnylangefeld.github.io/learning/Docker/How%2Bto%2BDocker.html
* https://devopscube.com/what-is-docker
* https://nickjanetakis.com/blog/understanding-how-the-docker-daemon-and-docker-cli-work-together
* https://snyk.io/blog/10-docker-image-security-best-practices/
