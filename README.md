
### Open psql shell
docker exec -it containerID psql -U postgres

### Create a new Django project
docker-compose run --rm --user uid:gid django sh -c 'cd /prj && django-admin startproject projectName'

### Open Django shell / run createsuperuser
docker exec -it containerID sh -c 'cd /prj/projectName && python manage.py shell'

### Create migration file
docker exec containerID sh -c 'cd /prj/projectName && python manage.py makemigrations appName'

### Apply the migrations
docker exec containerID sh -c 'cd /prj/projectName && python manage.py migrate appName'

