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


Документация с возможностями и примерами запросов проекта доступна
по адресу: http://127.0.0.1:8000/redoc/



Данный Api написал: Игорь Шкода

