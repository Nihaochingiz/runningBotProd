docker run --name my-mysql-db -e MYSQL_ROOT_PASSWORD=my-secret-pw -e MYSQL_DATABASE=mydatabase -e MYSQL_USER=myuser -e MYSQL_PASSWORD=mypassword -p 3306:3306 -d mysql:latest


docker run --name my-mysql-db -e MYSQL_ROOT_PASSWORD= -e MYSQL_DATABASE=mydatabase -e MYSQL_USER=myuser -e MYSQL_PASSWORD=mypassword -p 3306:3306 -d mysql:latest

Это создаст контейнер с именем `my-mysql-db`, устанавливающий базу данных с именем `mydatabase`, пользователем `myuser` и паролем `mypassword`. Порт контейнера MySQL будет проксирован на порт 3306 вашего компьютера.

docker run --name mysql-db -e MYSQL_ROOT_PASSWORD=0000 -e MYSQL_DATABASE=runningDB -e MYSQL_USER=ilyafofanov -e MYSQL_PASSWORD=0000 -p 3306:3306 -d mysql:latest


docker exec -it mysql mysql -u ilyafofanov -p runningdb


```bash
docker exec -it d92ed3e733d7 mysql -u ilyafofanov -p runningdb
```

docker exec -it d92ed3e733d7 mysql -u ilyafofanov -p runningdb можно ли тут также указывать хост и порт
`TOKEN = "7182270825:AAEsMmT1pGlAt0ks10zAa9fsopo9voKdbw4"`

`DB_USERNAME = "ilyafofanov"`

`DB_PASSWORD = "0000"`

`DB_NAME = "runningDB"`

`DB_HOST = "localhost"`

`DB_PORT="3306"`



```bash
docker exec -it d92ed3e733d7 mysql -u ilyafofanov -p -h 172.17.0.2 -P 3306 runningDB
```
**172.17.0.2**
docker inspect d92ed3e733d7

****Работает****
docker exec -it d92ed3e733d7 mysql -u ilyafofanov -p -h 172.17.0.2 -P 3306 runningDB

Копирование файла
```bash
docker cp C:\runningBot\create.sql CONTAINER_ID:/create.sql
```

docker cp C:\runningBot\create.sql d92ed3e733d7:/create.sql

Запустить create.sql

```bash
docker exec -i CONTAINER_ID mysql -u YOUR_USERNAME -pYOUR_PASSWORD DATABASE_NAME < /create.sql
```


docker exec -it d92ed3e733d7 mysql -u ilyafofanov -p -h 172.17.0.2 -P 3306 runningDB < /create.sql


```Plain
mysql -u ilyafofanov -p -h 172.17.0.2 -P 3306 runningDB < create.sql
```


Get-Content create.sql | docker exec -i container_name mysql -u username -ppassword database_name



docker run --name my-mysql-db -e MYSQL_ROOT_PASSWORD=0000 -e MYSQL_DATABASE=runningdb -p 3306:3306 -d mysql:latest



docker run --name mysql-db -e MYSQL_ROOT_PASSWORD=0000 -e MYSQL_DATABASE=runningdb -p 3306:3306 -d mysql:latest
Работает
docker exec -it mysql-db mysql -uroot -p runningdb -e "CREATE TABLE running_statistics (date DATE, distance VARCHAR(10), time VARCHAR(10));"
```sql
SHOW DATABASES;
```
```bash
docker exec -it mysql-db mysql -uroot -p
```

1 запуск
docker run --name mysql-db -e MYSQL_ROOT_PASSWORD=0000 -e MYSQL_DATABASE=runningdb -p 3308:3306 -d mysql:latest
2, далее
docker exec -it mysql-db mysql -uroot -p runningdb -e "CREATE TABLE running_statistics (date DATE, distance VARCHAR(10), time VARCHAR(10));"

**Инструкция**
1. docker run --name mysql-db -e MYSQL_ROOT_PASSWORD=0000 -e MYSQL_DATABASE=runningdb -p 127.0.0.1:3308:3306 -d mysql:latest
2. docker exec -it mysql-db mysql -uroot -p runningdb -e "CREATE TABLE running_statistics (date DATE, distance VARCHAR(10), time VARCHAR(10));"
3. docker exec -it mysql-db mysql -uroot -p
4.  ```sql
SHOW DATABASES;
```
5. use runningdb;
6. SELECT * FROM running_statistics;
7. docker build -t golang-bot .
8. docker run golang-bot