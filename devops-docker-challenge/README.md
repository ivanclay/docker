# devops-docker-challenge
Docker challenge commands

Challenge 01 -> PostgreSQL

docker container run -d -p 5432:5432 -e POSTGRES_DB=curso_docker -e POSTGRES_USER=docker_usr -e POSTGRES_PASSWORD=docker_pwd postgres

Challenge 02 -> MySQL

docker container run -d -p 3306:3306 -e MYSQL_ROOT_PASSWORD="root1234" -e MYSQL_DATABASE=docker_db -e MYSQL_USER=docker_usr -e MYSQL_PASSWORD=docker_pwd mysql

Challenge 03 -> MongoDB

docker run -d -e MONGO_INITDB_ROOT_USERNAME=mongo_usr -e MONGO_INITDB_ROOT_PASSWORD=mongo_pwd mongo
 
