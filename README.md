# Gogs and Postgres running with Docker Compose

## How to start
---

1. Run gogs and postgresql:
```
docker-compose up -d
```
2. To check that your gogs application is running go to link:
[http://localhost:8080](http://localhost:8080)

3. Find postgresql IP address in docker container with:
```
docker inspect --format="{{range .NetworkSettings.Networks}}{{.IPAddress}}{{end}}" gogs-postgresql
```

4. Set up and Initial your gogs application at [http://localhost:8080](http://localhost:8080), on DataBase section choose PostgreSQL, Host: `(IP from step #):5432`, User:`gogs`, Password:`changeme`, Database Name:`gogs`. you can define these on `docker-compose.yaml`.

## How to close 
---

1. Run `docker-compose stop` to stop gogs and postgresql containers.
2. Run `docker-compose rm -f` to remove gogs and postgresql containers.
3. Run `./clean.sh` if you want remove gogs and postgresql all datas.
>>>>>>> [chaohui] N/A add all files

## Сборка tar-архивов образов

### Тянем образ PostgreSQL
```
docker pull postgres
```

### Архивируем образ PostgreSQL
```
docker save postgres > postgres.tar
```



