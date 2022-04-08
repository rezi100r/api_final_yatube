### Описание
Модуль API - Социальная сеть для публикации личных дневников. 
### Технологии
Python 3.8
Django 2.2.19
### Запуск проекта в dev-режиме
- Установите и активируйте виртуальное окружение
- Установите зависимости из файла requirements.txt
```
pip install -r requirements.txt
``` 
- В папке с файлом manage.py выполните команду:
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
POST .../api/v1/jwt/create/
Content-Type: application/json
{
    "username": "",
    "password": ""
}
```
Просмотр постов:
```
GET .../api/v1/posts/
```
Просмотр групп:
```
GET .../api/v1/groups/
```
Просмотр комментариев для поста:
```
GET .../api/v1/posts/<post_id>/comments/
```
Просмотр подписок:
```
GET .../api/v1/follow/
```
### Авторы
Николай Егорченков

### License
MIT
