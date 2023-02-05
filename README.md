# Проект API Yamdb - api для сайта с отзывами на кино, книги и музыку

## Запуск проекта:

Клонировать репозиторий и перейти в него в командной строке:

```
git clone git@github.com:golenkovyura/api_yamdb.git
```

```
cd api_yamdb
```

Cоздать и активировать виртуальное окружение:

```
python -m venv env
```

```
source venv/Scripts/activate
```

```
python -m pip install --upgrade pip
```

Установить зависимости из файла requirements.txt:

```
pip install -r requirements.txt
```

Выполнить миграции:

```
python manage.py migrate
```
Выполнить загрузку информации в базу данных:

```
python manage.py csv_to_db
```

Запустить проект:

```
python manage.py runserver
```

## Примеры запросов

* Основные эндпоинты для аутентификации нового пользователя
> Для аутентификации применены JWT-токены.

  Создание JWT-токена:
```
http://127.0.0.1:8000/api/v1/jwt/create/
```
> Токен необходимо передавать в заголовке каждого запроса, в поле Authorization. Перед самим токеном должно стоять ключевое слово Bearer и пробел.

* Основные эндпоинты API
```
http://127.0.0.1:8000/api/v1/categories/
```
```
http://127.0.0.1:8000/api/v1/genres/
```
```
http://127.0.0.1:8000/api/v1/titles/
```
> пример POST запроса на (http://127.0.0.1:8000/api/v1/categories/):
```
{
  "name": "Василий",
  "slug": "Текст"
}
```
Полный список эндпойнтов, методы и параметры запросов описаны в докуметации:
```
http://127.0.0.1:8000/redoc/
```

## Авторы:
[Юрий Голенков](https://github.com/golenkovyura)

[Дмитрий Соколов](https://github.com/SokoDi)

[Александр Джуманов](https://github.com/AlexDjum)
