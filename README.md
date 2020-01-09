# JavaElasticAPM

### LOCAL MYSQL SETUP INSTRUCTIONS
```docker run --name some-mysql -e MYSQL_ROOT_PASSWORD=my-secret-pw -p 3306:3306 -d mysql
docker run -it --rm mysql mysql -h172.23.5.60 -uroot -p
CREATE USER 'fooUser' IDENTIFIED BY 'test123';
GRANT ALL PRIVILEGES ON *.* TO 'fooUser'@'172.23.5.60’;
FLUSH PRIVILEGES;
docker run -it --rm mysql mysql -h172.23.5.60 -ufooUser -p
create database demoprj;
use demoprj;
create table demo(id int(10), string varchar(20));
