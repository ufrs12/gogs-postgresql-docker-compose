# Gogs and Postgres running with Docker Compose

## How to start
---

1. Run gogs and postgresql:
```
docker-compose up -d
```

2. To check that your gogs application is running go to link:
[http://localhost:3000](http://localhost:3000)

3. Set up and Initial your gogs application. On DataBase section choose PostgreSQL, Host: `db:5432`, User:`gogs`, Password:`changeme`, Database Name:`gogs`. You can define these on `docker-compose.yaml`.

## How to close 
---

1. Run `docker-compose stop` to stop gogs and postgresql containers.
2. Run `docker-compose rm -f` to remove gogs and postgresql containers.


# Сборка на хостах без интернета

## Сборка tar-архивов образов

### Тянем образ PostgreSQL
```
docker pull postgres
```

### Архивируем образ PostgreSQL
```
docker save postgres > postgres.tar
```

### Тянем образ Gogs
```
docker pull gogs/gogs
```

### Архивируем образ Gogs
```
docker save gogs/gogs > gogs.tar
```

## По FTP переносим архивы на хост

## Загружаем образы в Docker

### Загружаем образ PostgreSQL
```
docker load --input postgres.tar
```
images_name:image_p

### Загружаем образ Gogs
```
docker load --input gogs.tar
```
images_name:image_g



# Git-client

https://tortoisegit.org/

В процессе установки, на этапе выбора языка, можно скачать языковой пакет и русифицировать прям на ходу.

### Авторизация без пароля

Инструкция 
http://fkn.ktu10.com/?q=node/6974

Еще инструкция 

http://fkn.ktu10.com/?q=node/6965

Качаем puttygen.exe
https://www.chiark.greenend.org.uk/~sgtatham/putty/latest.html

Не получилось пока заюзать...