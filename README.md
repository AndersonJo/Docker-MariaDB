# mariadb-docker
Dockerized MariaDB 10.0.22 

https://github.com/docker-library/mariadb/blob/2a8c48a54d8210241861740ea76b5aedf4da681f/10.0/Dockerfile

### Build
```
docker build -t mariadb .
```

### Master Database
```
docker run --name account -p 3340:3306 --volume /dbs/account:/var/lib/mysql -e MYSQL_ROOT_PASSWORD=1234 -d mariadb:latest
```

### Slave Database
```
docker run --name replica1 -p 3341:3306 --volume /dbs/replica1:/var/lib/mysql --link account:master  -e MYSQL_ROOT_PASSWORD=1234 -d mariadb:latest
```



