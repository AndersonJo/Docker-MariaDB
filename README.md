# mariadb-docker
Dockerized MariaDB 10.0.22 


```
docker build -t mariadb .
```

Master Database
```
docker run --name account -p 3340:3306 --volume /dbs/account:/var/lib/mysql -e MYSQL_ROOT_PASSWORD=1234 -d mariadb:latest
```

Slave Database
```
docker run --name replica1 -p 3341:3306 --volume /dbs/replica1:/var/lib/mysql --link account:master  -e MYSQL_ROOT_PASSWORD=1234 -d mariadb:latest
```
