Task:

Развернуть kubernetes-кластер
Среда контейнеризации: K3s or GKE or EKS
Операционная система: Linux
Веб-сервер: Nginx - any
Backend: Php
Балансировщик: any

Написать скрипт, который развернет среду контейнеризации, запустит в ней веб-сервер Nginx и настроит бекенд Php для приема запросов. Скрипт после запуска веб-сервера и бекенда, должен проверить их доступность, используя порты балансировщика.


Deploy a Kubernetes cluster
Containerization environment: K3s or GKE or EKS
Linux operating system
Web server: Nginx-any
Backend: Php
Balancer: any

Write a script that will deploy the containerization environment, launch a web server with nginx in it, and configure the PHP backend to accept requests. The script after the launch web server and the backend should check their availability using the balancer ports.

NOTES:
```
kubectl create ns webapp && kubectl create -f kubernetes.yml -n webapp
```
