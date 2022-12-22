# DockerCompose-Django-PostgreSQL-Redis-Celery

run:

    docker-compose build

    docker-compose run --rm app django-admin startproject core .

    docker-compose up

then enter container and start app:

    docker exec -it django_app sh

    python manage.py startapp newapp


run celery tasks in a new terminal:

    docker exec -it django_app sh

    python manage.py shell

    from newapp.tasks import add

    add.delay(2, 2)