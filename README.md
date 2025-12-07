# Домашнее задание к занятию «Базовые объекты K8S» Стасенко Григорий Михайлович

### Цель задания

В тестовой среде для работы с Kubernetes, установленной в предыдущем ДЗ, необходимо развернуть Pod с приложением и подключиться к нему со своего локального компьютера. 

------

### Чеклист готовности к домашнему заданию

1. Установленное k8s-решение (например, MicroK8S).
2. Установленный локальный kubectl.
3. Редактор YAML-файлов с подключенным Git-репозиторием.

------

### Инструменты и дополнительные материалы, которые пригодятся для выполнения задания

1. Описание [Pod](https://kubernetes.io/docs/concepts/workloads/pods/) и примеры манифестов.
2. Описание [Service](https://kubernetes.io/docs/concepts/services-networking/service/).

------

### Задание 1. Создать Pod с именем hello-world

1. Создать манифест (yaml-конфигурацию) Pod.

<img width="567" height="275" alt="image" src="https://github.com/user-attachments/assets/f44a07f6-23fb-4632-98fc-0a32904d8654" />

2. Использовать image - gcr.io/kubernetes-e2e-test-images/echoserver:2.2.

<img width="694" height="211" alt="image" src="https://github.com/user-attachments/assets/0380e0c4-aab2-4395-80f7-949efa458ab3" />


3. Подключиться локально к Pod с помощью `kubectl port-forward` и вывести значение (curl или в браузере).

<img width="657" height="95" alt="image" src="https://github.com/user-attachments/assets/28984f18-17ee-4f2d-93ec-01d1e0f852a4" />
<img width="416" height="473" alt="image" src="https://github.com/user-attachments/assets/6b07afaa-09b7-4e42-9118-123ec565d505" />


------

### Задание 2. Создать Service и подключить его к Pod

1. Создать Pod с именем netology-web.
2. Использовать image — gcr.io/kubernetes-e2e-test-images/echoserver:2.2.

<img width="602" height="306" alt="image" src="https://github.com/user-attachments/assets/9e328186-92fc-4319-afd7-8bf942cd964b" />

3. Создать Service с именем netology-svc и подключить к netology-web.

<img width="539" height="317" alt="image" src="https://github.com/user-attachments/assets/2d5d6731-e1a4-40d2-a103-e7060a1e617a" />
<img width="540" height="194" alt="image" src="https://github.com/user-attachments/assets/99a86836-de7f-4ab3-a524-714442e60239" />

4. Подключиться локально к Service с помощью `kubectl port-forward` и вывести значение (curl или в браузере).

<img width="654" height="81" alt="image" src="https://github.com/user-attachments/assets/88968998-b241-4213-a582-f46d19d452f8" />
<img width="461" height="471" alt="image" src="https://github.com/user-attachments/assets/f84448fb-a5fa-4ae1-bf4f-32f2c8e51171" />


------

### Правила приёма работы

1. Домашняя работа оформляется в своем Git-репозитории в файле README.md. Выполненное домашнее задание пришлите ссылкой на .md-файл в вашем репозитории.
2. Файл README.md должен содержать скриншоты вывода команд `kubectl get pods`, а также скриншот результата подключения.
3. Репозиторий должен содержать файлы манифестов и ссылки на них в файле README.md.
