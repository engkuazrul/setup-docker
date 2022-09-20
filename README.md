# setup-docker

## postgres & pgadmin
- docker volume create postgresql-volume
- docker run --name postgresql -e POSTGRES_USER=postgres -e POSTGRES_PASSWORD=123456 -p 5432:5432 -v postgresql-volume:/var/lib/postgresql/data -d postgres
- docker volume create pgadmin-volume
- docker run -p 5050:80  -e "PGADMIN_DEFAULT_EMAIL=admin@postgres.com" -e "PGADMIN_DEFAULT_PASSWORD=admin" -v pgadmin-volume:/var/lib/pgadmin -d dpage/pgadmin4


## mysql
- docker volume create mysql-volume
- docker run --name=tns_mysql -p3306:3306 -v mysql-volume:/var/lib/mysql -e MYSQL_ROOT_PASSWORD=123456 -d mysql/mysql-server
