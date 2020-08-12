## Development environment for Django projects that uses docker-compose and PostgreSQL.

### Interactive shell commands
- Open psql

```
docker exec -it containerID psql -U postgres
```

- Access Django's shell

```
docker exec -w /prj/projectName -it containerID python manage.py shell
```

- Create admin user

```
docker exec -w /prj/projectName -it containerID python manage.py createsuperuser
```

### Non-interactive shell commands
- Create a new Django project

```
docker-compose run -w /prj/projectName --rm --u uid:gid django django-admin startproject projectName
```

- Create migration file

```
docker-compose run -w /prj/projectName --rm django python manage.py makemigrations appName
```

- Run migrate

```
docker-compose run -w /prj/projectName --rm django python manage.py migrate appName
```

- Run startapp

```
docker-compose run -w /prj/projectName --rm django python manage.py startapp appName
```
