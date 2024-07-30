# Домашнее задание к занятию «Конфигурация приложений в k8s» - Сергей Ситкарёв

## Задание 1. Создать Deployment приложения и решить возникшую проблему с помощью ConfigMap. Добавить веб-страницу

Создать Deployment приложения, состоящего из контейнеров nginx и multitool.

[deployment](https://github.com/SSitkarev/2.3-k8s-app-config/blob/main/src/deployment.yaml)

Решить возникшую проблему с помощью ConfigMap.

![Задание1](https://github.com/SSitkarev/2.3-k8s-app-config/blob/main/img/1.jpg)

Оба приложения по умолчанию используют порт 80. Необходимо переопределить порт одному из приложений.

[configmap](https://github.com/SSitkarev/2.3-k8s-app-config/blob/main/src/configmap.yaml)

Продемонстрировать, что pod стартовал и оба конейнера работают.

![Задание1](https://github.com/SSitkarev/2.3-k8s-app-config/blob/main/img/2.jpg)

Сделать простую веб-страницу и подключить её к Nginx с помощью ConfigMap. Подключить Service и показать вывод curl или в браузере.

[service](https://github.com/SSitkarev/2.3-k8s-app-config/blob/main/src/service.yaml)

![Задание1](https://github.com/SSitkarev/2.3-k8s-app-config/blob/main/img/3.jpg)

## Задание 2. Создать приложение с вашей веб-страницей, доступной по HTTPS

Создать Deployment приложения, состоящего из Nginx.

[nginx-deployment](https://github.com/SSitkarev/2.3-k8s-app-config/blob/main/src/nginx-deployment.yaml)

Создать собственную веб-страницу и подключить её как ConfigMap к приложению.

[nginx-configmap](https://github.com/SSitkarev/2.3-k8s-app-config/blob/main/src/nginx-configmap.yaml)

Выпустить самоподписной сертификат SSL. 

![Задание2](https://github.com/SSitkarev/2.3-k8s-app-config/blob/main/img/4.jpg)

Создать Secret для использования сертификата.

[nginx-secret](https://github.com/SSitkarev/2.3-k8s-app-config/blob/main/src/nginx-secret.yaml)

![Задание2](https://github.com/SSitkarev/2.3-k8s-app-config/blob/main/img/5.jpg)

Создать Ingress и необходимый Service, 

[nginx-service](https://github.com/SSitkarev/2.3-k8s-app-config/blob/main/src/nginx-service.yaml)

[nginx-ingress](https://github.com/SSitkarev/2.3-k8s-app-config/blob/main/src/nginx-ingress.yaml)

подключить к нему SSL в вид. Продемонстировать доступ к приложению по HTTPS.

![Задание2](https://github.com/SSitkarev/2.3-k8s-app-config/blob/main/img/6.jpg)