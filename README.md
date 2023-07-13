## docker
```bash
# mysql (rodando na porta 3306)
docker run -it --name mysql-container-name --network="host" -e MYSQL_TCP_PORT=3306 -e MYSQL_ALLOW_EMPTY_PASSWORD=true mysql:5
```
```bash
# lista os containers com as respectivas portas
docker container ls --format "table {{.ID}}\t{{.Names}}\t{{.Ports}}" -a
```
```bash
# entranso no container
docker exec -it mysql-container-name bash
```

## mysql cli
```bash
# conectando
mysql -u root
```
```bash
# exibindo a porta q tá rodando
SHOW GLOBAL VARIABLES LIKE 'PORT';
```
