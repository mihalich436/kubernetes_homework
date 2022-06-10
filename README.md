# kubernetes_homework

Были выполнены следующие шаги:
1. Создан файл hello.html, в котором содержится одна строка "hello world!";
2. Создан Dockerfile на основе python:3-alpine, который копирует в каталог "/app" файлы, содержащиеся в папке с докерфайлом (в данном случае копируется только hello.html, а dockerfile игнорируется);
3. Собран Docker image "web:1.0.0" и выложен в Docker Hub;
4. Создан Kubernetes Pod manifest "webpod.yaml", в котором запускается ReplicaSet с двумя репликами пода, запускающими контейнер из созданного image;
5. Обеспечен доступ к приложению внутри кластера.

Результат команды “kubectl describe pod web” приведен в файле "result.txt".
