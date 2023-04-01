# Домашнее задание к лекции «Docker»

Клонировать проект:
```
git clone git@github.com:SergeyMMedvedev/1.3-docker.git
```

## Задание 1

Перейти в папку task_1 с файлом для образа:
```
cd 1.3-docker/task_1
```
Собрать образ:
```
docker build -t my-nginx .
```
Запустить контейнер на основе образа:
```
docker run --name my-nginx-server -d -p 8081:80 my-nginx
```
Проверить, что стартовая страница index.html была заменена в ходе сборки образа:
```
curl localhost:8081/
```

## Задание 2

Перейти в папку task_2/stocks_products с файлом для образа:
```
cd 1.3-docker/task_2/stocks_products
```

Собрать образ с джанго приложением:
```
docker build -t my-django .
```
Запустить контейнер на основе образа:
```
docker run --name my-django-app -d -p 8000:8000 my-django
```
Проверить работу API:
```
curl localhost:8000/api/v1/check/
curl localhost:8000/api/v1/test/
curl localhost:8000/api/v1/
```