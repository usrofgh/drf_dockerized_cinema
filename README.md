# Dockerized DRF Cinema
<i>Interesting project which describes real cinema with all necessary features</i>

## Installation
<hr>

Clone the repository <br>
If want - specify another folder name where `cinema`

```shell
git clone https://github.com/usrofgh/drf_dockerized_cinema.git cinema
cd cinema
python -m venv venv
pip install -r requirements.txt

```
#### Linux:
```shell
source venv/bin/activate
export POSTGRES_HOST=POSTGRES_HOST
export POSTGRES_DB=POSTGRES_DB
export POSTGRES_USER=POSTGRES_USER
export POSTGRES_PASSWORD=POSTGRES_PASSWORD
export SECRET_KEY=SECRET_KEY
export DEBUG=True
```
#### Windows
```shell
source venv\Scripts\activate
SET venv/bin/activate
SET POSTGRES_HOST=POSTGRES_HOST
SET POSTGRES_DB=POSTGRES_DB
SET POSTGRES_USER=POSTGRES_USER
SET POSTGRES_PASSWORD=POSTGRES_PASSWORD
SET SECRET_KEY=SECRET_KEY
SET DEBUG=True
```
Next

```shell
docker-compose build
docker compose up
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


## Endpoints
<hr>

#### Cinema
![cinema_demo_swagger.png](cinema_demo_swagger.png)

#### User
![user_demo_swagger.png](user_demo_swagger.png)