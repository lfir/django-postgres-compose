## Development environment for Django projects that uses docker-compose and PostgreSQL.

### Open psql shell (interactive shell)
docker exec -it containerID psql -U postgres

### Create a new Django project
docker-compose run --rm --user uid:gid django sh -c 'cd /prj && django-admin startproject projectName'

### Open Django shell / run createsuperuser (interactive shell)
docker exec -it containerID sh -c 'cd /prj/projectName && python manage.py shell'

### Create migration file / run migrate or startapp (non-interactive)
docker exec containerID sh -c 'cd /prj/projectName && python manage.py makemigrations appName'

