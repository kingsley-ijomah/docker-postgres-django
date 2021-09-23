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