## HW12 - Docker контейнеры. Docker под капотом

Использование директории docker-monolith внутри проекта microservices.

- репозитории настроить интеграцию с travis-ci по аналогии с репозиторием infra

- установить Docker

- cоздать docker host

- создать свой образ: docker commit <u_container_id> yourname/ubuntu-tmp-file

- изучить как безусловно завершить процесс: docker kill $(docker ps -q)

- изучить как увидеть сколько дискового пространства занято образами, контейнерами и volume’ами и сколько из них не используется и   возможно удалить: docker system df

- изучить как удалить контейнер и image: docker rm $(docker ps -a -q) # удалит все незапущенные контейнеры, docker rmi $(docker images -q)

- собрать свой образ: docker build -t reddit:latest .

- работа с Docker Hub: выгрузить и загрузить из/в него докер образ
