Django Snippets API

Этот проект на Django предоставляет простой API для управления фрагментами кода. Пользователи могут создавать, извлекать, обновлять и удалять фрагменты кода, используя предоставленные конечные точки API.
Начало работы
Предварительные требования

Убедитесь, что на вашей системе установлены следующие компоненты:

    Python (рекомендуется 3.x)
    Django
    Библиотека pygments (pip install pygments)
    Django REST Framework

Установка

    Клонируйте репозиторий:

    bash

git clone https://github.com/ваше-имя-пользователя/django-snippets-api.git

Перейдите в каталог проекта:

bash

cd django-snippets-api

Установите необходимые зависимости:

bash

pip install -r requirements.txt

Примените миграции для настройки базы данных:

bash

    python manage.py migrate

Запуск сервера

Запустите сервер разработки:

bash

python manage.py runserver

API будет доступно по адресу http://localhost:8000/.
Конечные точки API

    GET /snippets/: Извлечь список всех фрагментов кода.
    POST /snippets/: Создать новый фрагмент кода.
    GET /snippets/{id}/: Извлечь детали конкретного фрагмента кода.
    PUT /snippets/{id}/: Обновить конкретный фрагмент кода.
    DELETE /snippets/{id}/: Удалить конкретный фрагмент кода.

Использование

Вы можете использовать инструменты, такие как curl или Postman, чтобы взаимодействовать с конечными точками API. Вот пример с использованием curl:

    Создать новый фрагмент:

    bash

curl -X POST -H "Content-Type: application/json" -d '{"title": "Мой фрагмент", "code": "print(\"Привет, мир!\")", "language": "python"}' http://localhost:8000/snippets/

Извлечь все фрагменты:

bash

curl http://localhost:8000/snippets/

Извлечь конкретный фрагмент:

bash

curl http://localhost:8000/snippets/1/

Обновить фрагмент:

bash

curl -X PUT -H "Content-Type: application/json" -d '{"title": "Обновленный фрагмент", "code": "print(\"Обновлено!\")"}' http://localhost:8000/snippets/1/

Удалить фрагмент:

bash

    curl -X DELETE http://localhost:8000/snippets/1/

Не стесняйтесь изучать и настраивать проект в соответствии с вашими потребностями. Если у вас есть вопросы или возникли проблемы, обратитесь к документации Django и Django REST Framework для получения помощи.
