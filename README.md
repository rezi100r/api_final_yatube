### Описание
Модуль API - Социальная сеть для публикации личных дневников. 
### Технологии
Python 3.8
Django 2.2.19
Django Rest Framework 3.12.4
### Запуск проекта в dev-режиме
- Установите и активируйте виртуальное окружение
```
python3 -m venv env
```
```
source env/bin/activate
```
```
python3 -m pip install --upgrade pip
```
- Установите зависимости из файла requirements.txt
```
pip install -r requirements.txt
``` 
- В папке с файлом manage.py выполните команду:
```
\api_final_yatube\yatube_api\manage.py
```
- Выполнить migrate
```
python manage.py migrate
```
- Создайте пользователя
```
python manage.py createsuperuser
```
- (или) Сменить пароль для пользователя admin
```
python manage.py changepassword admin
```
- Запуск сервиса
```
python manage.py runserver
```
### API Примеры
Создание токена:
```
REQUEST:
POST http://127.0.0.1:8000/api/v1/jwt/create/
Content-Type: application/json
{
    "username": "",
    "password": ""
}
______________________________________________
RESPONSE:
{
    "refresh": "DATA",
    "access": "DATA"
}
```
Просмотр постов:
```
REQUEST:
GET http://127.0.0.1:8000/api/v1/posts/
______________________________________________
RESPONSE:
[
    {
        "id": 1,
        "author": "admin",
        "group": null,
        "text": "Пост 1",
        "pub_date": "2022-04-09T16:24:28.107050Z",
        "image": null
    },
    {
        "id": 2,
        "author": "admin",
        "group": null,
        "text": "Пост 2",
        "pub_date": "2022-04-09T16:24:38.100791Z",
        "image": null
    },
    {
        "id": 3,
        "author": "admin",
        "group": null,
        "text": "Пост 3",
        "pub_date": "2022-04-09T16:24:42.160579Z",
        "image": null
    }
]
```
Просмотр групп:
```
REQUEST:
GET http://127.0.0.1:8000/api/v1/groups/
______________________________________________
RESPONSE:
[
    {
        "id": 1,
        "title": "Группа 1",
        "slug": "gruppa-1",
        "description": "Группа 1"
    }
]
```
Просмотр комментариев для поста:
```
REQUEST:
GET http://127.0.0.1:8000/api/v1/posts/<post_id>/comments/
______________________________________________
RESPONSE:
[
    {
        "id": 1,
        "author": "admin",
        "text": "Комментарий 1",
        "created": "2022-04-09T16:26:36.212570Z",
        "post": 1
    },
    {
        "id": 2,
        "author": "admin",
        "text": "Комментарий 2",
        "created": "2022-04-09T16:26:40.356078Z",
        "post": 1
    }
]
```
Просмотр подписок:
```
REQUEST:
GET http://127.0.0.1:8000/api/v1/follow/
______________________________________________
RESPONSE:

```
### Авторы
Николай Егорченков

### License
MIT
