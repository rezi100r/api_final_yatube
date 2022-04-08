### Описание
Социальная сеть для публикации личных дневников, модуль API
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
Создание токена
/api/v1/jwt/create/
{
    "username": "",
    "password": ""
}
### Авторы
Николай Егорченков

### License
MIT