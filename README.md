Api yatube final
Финальный проект по API для работы с постами, имеется возможность
объединять их в сообщества, добавлять к ним комментарии, возможность подписки
на понравившегося автора.

Как запустить проект:

Cоздать и активировать виртуальное окружение:
python3 -m venv env
source env/bin/activate

Установить зависимости из файла requirements.txt:
python3 -m pip install --upgrade pip
pip install -r requirements.txt

Выполнить миграции:
python3 manage.py migrate

Запустить проект:
python3 manage.py runserver


Пример запроса POST на создание поста по эндпоинту:
http://127.0.0.1:8000/api/v1/posts/

{
    "text": "Это отличное Api"
}

При удачном создании (статусе 201) вернется ответ:

{
    "id": 1,
    "author": "delta",
    "text": "Это отличное Api",
    "pub_date": "2022-07-20T02:18:28.507681+03:00",
    "image": null,
    "group": null
}

Пример запроса GET на получение поста по эндпоинту:
http://127.0.0.1:8000/api/v1/posts/2/
вернется ответ: 
{
    "id": 2,
    "author": "delta",
    "text": "Есть возможность оставить комментарий к этой записи",
    "pub_date": "2022-07-20T02:26:46.222376+03:00",
    "image": null,
    "group": null
}