# API сервис проекта YaMDB
Проект разработан командой мечты из трех разработчиков, в рамках обучения на курсе Backend-разработчик Яндекс Практикума.
___
### Описание
Это полноценный проект предоставляющий отзывы для различных произведений основанный исключительно на API. Благодаря API данные можно получать на различных ресурсах и что самое важное на различных устройствах. Любое мобильное приложение или веб сайт может пользоваться данными YaMBD, вносить изменения и быть в курсе новых отзывов и комментарий к произведениям. Блок аутентификации и авторизации выстроен просто для пользователя и в то же время защищает данные пользователей не позволяя сторонним пользователям изменять данные других пользователей. Для удобно поиска нужно произведения внедрены фильтры по жанрам и категориям. Ни одно произведение не останется без отзыва, а отзыв без комментария на всех видах устройств.
___
### Технологии
- [Python 3.7]
- [Django 3.2.15]
- [SimpleJWT 4.7.2]
- [Django REST Framework 3.12.4]
- [DRF multiple serializer 0.2.3]
- [Django-filters]
___
# Запуск проекта в dev-режиме на локальном сервере:
Клонировать репозиторий и перейти в директорию с ним:
```
git clone https://github.com/Tozix/api_yamdb.git
```
```
cd api_yamdb
```
Cоздать и активировать виртуальное окружение:
```
python3 -m venv env
```
```
source venv/bin/activate
```
Установить зависимости из файла requirements.txt:
```
python3 -m pip install --upgrade pip
```
```
pip install -r requirements.txt
```
Выполнить миграции:
```
python3 manage.py migrate
```
Запустить проект:
```
python3 manage.py runserver
```
Сервер будет доступен по адресу:
```
http://127.0.0.1:8000/
```
___
### Примеры GET запросов
Для получения списка доступных адресов отправьте запрос:
```
http://127.0.0.1:8000/api/v1/
```
Пример ответа на запрос о получении списка доступных адресов в формате json:
```
{
    "users": "http://127.0.0.1:8000/api/v1/users/",
    "titles": "http://127.0.0.1:8000/api/v1/titles/",
    "categories": "http://127.0.0.1:8000/api/v1/categories/",
    "genres": "http://127.0.0.1:8000/api/v1/genres/"
}
```
Для получения всех произведений:
```
GET http://127.0.0.1:8000/api/v1/titles/
```
Пример ответа на запрос о получении всех произведений в формате json:
```
[
    {
        "count": 1,
        "next": "Null",
        "previous": "Null",
        "results": [
            {
                "id": 1,
                "name": "The best team",
                "year": 2022,
                "rating": 10,
                "description": "Little story about dev team",
                "genre": [
                    {
                        "name": "Adventure",
                        "slug": "adventure"
                    }
                ],
                "category": {
                "name": "IT",
                "slug": "it"
                }
            }
        ]
    }
]
```
Все виды запросов и их описание доступно в документации по адресу:
```
http://127.0.0.1:8000/redoc/
```
___
### Команда
- [Никита Емельянов], студент Яндекс Практикума он же тимлид на этом проекте.
- [Полина Костина], студентка Яндекс Практикума
- [Дмитрий Ротанин], студент Яндекс Практикума

[//]: # (Ниже находятся справочные ссылки)

   [Python 3.7]: <https://www.python.org/downloads/release/python-370/>
   [Django 3.2.15]: <https://www.djangoproject.com/download/>
   [SimpleJWT 4.7.2]: <https://django-rest-framework-simplejwt.readthedocs.io/en/latest/>
   [Django REST Framework 3.12.4]: <https://www.django-rest-framework.org/community/release-notes/>
   [DRF multiple serializer 0.2.3]: <https://pypi.org/project/drf-multiple-serializer/>
   [Django-filters]: <https://django-filter.readthedocs.io/en/stable/guide/install.html>
   [Никита Емельянов]: <https://github.com/Tozix>
   [Полина Костина]: <https://github.com/Polina1Kostina>
   [Дмитрий Ротанин]: <https://github.com/Annsjaw>