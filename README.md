### Deploying:
Components:
- Orchestration: K3S Lightweight Kubernetes
- LB: Traefik Ingress Controller
- Frontend: Nginx Helm chart
- Backend: PHP application Guestbook
- Database: Redis cluster

Before deploying the project, you should clone repository and edit Ansible inventory file `hosts`, specify the desired IP addresses in it.
Specify the expected domain name in `chart.nginx/values.yaml` in `serverBlock:` and `ingress:` for proxing and ingress balancing.
Also appropriate A-record must be present in DNS or `/etc/hosts`. For example: `192.168.0.102	exness.local`.
Then execute playbook:
```
ansible-playbook -i hosts playbook.yml
```
![](png/playbook_output.png)
Getting status of components on target host:
![](png/kubectl_get.png)
Check web access through domain name:
![](png/web.png)

### Задача (rus):
Развернуть kubernetes-кластер:
Среда контейнеризации: K3s or GKE or EKS;
Операционная система: Linux;
Веб-сервер: Nginx - any;
Backend: Php;
Балансировщик: any.

Написать скрипт, который развернет среду контейнеризации, запустит в ней веб-сервер Nginx и настроит бекенд Php для приема запросов. Скрипт после запуска веб-сервера и бекенда, должен проверить их доступность, используя порты балансировщика.
