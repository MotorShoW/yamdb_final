# yamdb_final
![YAMDB](https://github.com/MotorShoW/yamdb_final/actions/workflows/yamdb_workflows.yml/badge.svg?event=push)

Учебный проект, REST API для сервиса YAMDB,
который позволяет собирать отзывы юзеров по выбранным категориям.
Подробная документация по эндпойнту 'http://51.250.28.135/redoc/'
Или локально `http://localhost/redoc/` после  запуска проекта


## Инструкция для запуска приложения в контейнерах
Клонируем репозиторий через командную строку, заходим в директорию с `docker-compose.yaml`
```
*заходим в нужную директорию*

git clone https://github.com/MotorShoW/infra_sp2

cd infra_sp2/infra/
```
Запускаем контейнеры, выполняем миграции, проводим сбор статики
```
docker-compose up -d --build

docker-compose exec web python manage.py migrate

docker-compose exec web python manage.py collectstatic --no-input

```
Для остановки контейнеров :
```

docker-compose down -v

```
## Шаблон наполнения ENV-файла
```
DB_ENGINE=django.db.backends.postgresql

DB_NAME=postgres

POSTGRES_USER=postgres

POSTGRES_PASSWORD=postgres

DB_HOST=db

DB_PORT=5432

SECRET_KEY = 'YourSecretKey'

```
# Python, Django, DRF, PostgreSQL, Docker-compose.

### Код написан [MotorShoW](https://github.com/MotorShoW).