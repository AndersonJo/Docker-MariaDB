# mariadb-docker
Dockerized MariaDB 10.0.22 


```
docker build -t mariadb .
```

```
docker run --name account -p 3340:3306 --volume /home/anderson/dbs/account:/var/lib/mysql -e MYSQL_ROOT_PASSWORD=1234 -d mariadb:latest
```
