# Dockerize Django with Postgres, Gunicorn and Nginx

### Development

```sh
$ docker compose up -d --build
$ docker compose -f docker-compose.yml up -d --build
```

Test app at: [http://localhost:8000](http://localhost:8000). The "app" folder is mounted into the container and your code changes apply automatically.

run django terminal command example:
```sh
docker compose exec web python manage.py migrate
```

### Production

```sh
$ docker compose -f docker-compose.prod.yml up -d --build
docker compose -f docker-compose.prod.yml exec web python manage.py migrate --noinput
docker compose -f docker-compose.prod.yml exec web python manage.py collectstatic --no-input --clear
```

Test app at: [http://localhost:1337](http://localhost:1337). Folders are not mounted, image needs to be rebuilt.
