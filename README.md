# Dockerized DRF Cinema
<i>Interesting project which describes real cinema with all necessary features</i>

## Installation
<hr>

Clone you repository <br>
If want - specify another folder name where `cinema`

```shell
git clone https://github.com/usrofgh/drf_dockerized_cinema.git cinema
cd cinema
python -m venv venv
source venv/Scripts/activate
pip install -r requirements.txt
```

Inside the directory you'll see `.env.sample` <br>
It's an example which data must
contain `.env` file which you need to create and fill

```
# .env.sample
POSTGRES_HOST=POSTGRES_HOST
POSTGRES_DB=POSTGRES_DB
POSTGRES_USER=POSTGRES_USER
POSTGRES_PASSWORD=POSTGRES_PASSWORD
```

Next, we'll build django-service, pull psql from docker-hub, create DB, apply migrations
with help next command

```shell
docker-compose up -d
```
For use all features of this project you need create a user
```shell
docker exec -it drf_dockerized_cinema-app-1 bash
python manage.py createsuperuser
```
After creating can exit
```shell
exit
```
Fine. You can use the project
[http://127.0.0.1:8000/api/cinema/](http://127.0.0.1:8000/api/cinema/)

### Connect DB into PyCharm

<hr>
If you wish you can connect DB for viewing the tables
<br>

```
Database Tab -> Click Plus -> Data Source -> PostgreSQL
Specify all necessary data and specify(!) 5433 port
```

## Features

<hr>

- JWT authenticated (access, refresh through API)
- Admin panel
- Documentation: [swagger](http://127.0.0.1:8000/api/doc/swagger/), [redoc](http://127.0.0.1:8000/api/doc/redoc/)</li>

- Managing tickets and orders
- CRUD for resources through API and admin panel
- Filter movies by genres, actors, title

