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

## HW13 - Docker образы. Микросервисы

Использование директории src внутри проекта microservices.

- научиться описывать и собирать Docker-образы для сервисного приложения

- научиться оптимизировать работу с Docker-образами

- запуск и работа приложения на основе Docker-образов
`
- оценить удобства запуска контейнеров при помощи docker run

- разбить наше приложение на несколько компонентов

- запустить наше микросервисное приложение

## HW14 - Сетевое взаимодействие Docker контейнеров. Docker Compose. Тестирование образов

Использование директории src внутри проекта microservices.

- работа с сетями в Docker(none, host, bridge)

- использование docker-compose

## HW15 - Gitlab CI. Построение процесса непрерывной интеграции

Использование .gitlab-ci.yml внутри проекта microservices.

- подготовить инсталляцию Gitlab CI

- подготовить репозиторий с кодом приложения

- описать для приложения этапы пайплайна

- определить окружения

## HW16 - Введение в мониторинг. Модели и принципы работы систем мониторинга

Ссылки на образы на докер хаб:

https://hub.docker.com/repository/docker/natali1701/prometheus

https://hub.docker.com/repository/docker/natali1701/post

https://hub.docker.com/repository/docker/natali1701/comment

https://hub.docker.com/repository/docker/natali1701/ui

Использование директории docker внутри проекта microservices.

- Prometheus: запуск, конфигурация, знакомство с Web UI

- мониторинг состояния микросервисов

- сбор метрик хоста с использованием экспортера

## HW17 - Мониторинг приложения и инфраструктуры

Использование директорий docker, monitoring внутри проекта microservices.

- Мониторинг Docker контейнеров

- Визуализация метрик

- Сбор метрик работы приложения и бизнес метрик

- Настройка и проверка алертинга

Ссылки на образы на докер хаб:

https://hub.docker.com/repository/docker/natali1701/prometheus

https://hub.docker.com/repository/docker/natali1701/post

https://hub.docker.com/repository/docker/natali1701/comment

https://hub.docker.com/repository/docker/natali1701/ui

https://hub.docker.com/repository/docker/natali1701/alertmanager

## HW18 - Применение системы логирования в инфраструктуре на основе Docker

Использование директорий docker, logging внутри проекта microservices.

- Сбор неструктурированных логов

- Визуализация логов

- Сбор структурированных логов

- Распределенная трасировка


## HW19 - Введение в Kubernetes

Использование директорий kubernetes внутри проекта microservices.

- пройти Kubernetes The Hard Way

- проверить, что kubectl apply -f <filename> проходит по созданным до этого deployment-ам (ui, post, mongo, comment) и поды запускаются

- удалить кластер после прохождения THW

- все созданные в ходе прохождения THW файлы (кроме бинарных) поместить в папку kubernetes/the_hard_way репозитория (сертификаты и ключи тоже можно коммитить, но только после удаления кластера)

## HW20 - Основные модели безопасности и контроллеры в Kubernetes

Использование директорий kubernetes внутри проекта microservices.

- Ingress Controller

- Ingress

- Secret

- TLS

- LoadBalancer Service

- Network Policies

- PersistentVolumes

- PersistentVolumeClaims

## HW21 - Основные модели безопасности и контроллеры в Kubernetes 

Использование директории kubernetes внутри проекта microservices.

- Развернуть локальное окружение для работы с Kubernetes 

- Развернуть Kubernetes в GKE 

- Запустить reddit в Kubernetes

- Подготовить локальноеокружение, которое будет состоять из: 

  1)kubectl  - фактически, главной утилиты для работы c Kubernetes API (все, что делает kubectl, можно сделать с помощью HTTP-запросов к API k8s)

  2)Директории ~/.kube - содержит служебную инфу для kubectl (конфиги, кеши, схемыAPI)

  3)minikube - утилиты для разворачивания локальной инсталляции Kubernetes
