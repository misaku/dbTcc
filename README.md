# Docker
link: [https://www.docker.com/](https://www.docker.com/)
após baixar é recomendando usar o hyper-v do windows
```js
//Comandos iniciais
docker run hello-world
//Com esse comando o docker instala o primeiro container e faz um auto teste
//OBS sempre que um container nao funcionar tente resetar o docker e dar um stop e start no container
//o reset do docker é feito pelo daemon mas o stop e start pode ser feito com esses comandos
docker stop nomecontainer
docker start nomecontainer
```
# PostgreSQL e Postgre + Postgis
link documentação:
- [oficial](https://www.postgresql.org)
- [postgresql-docker](https://hub.docker.com/_/postgres/)
- [postgresql+postgis-docker](https://hub.docker.com/r/kartoza/postgis/)

comandos:
```js
docker pull postgres
docker run --name nome-container-postgres -e POSTGRES_PASSWORD=senhapostgres -e POSTGRES_USER=usuarioPostgres -p 5432:5432 -d -t postgres
//outra opção de imagem é o postgres com o postgis que tem geolocalização mesmo parametros se quiser mudar usuario e sennha por padrao user e senha são docker
docker pull kartoza/postgis
docker run --name nome-container -p 5432:5432 -d -t kartoza/postgis
//para acessar o banco pode usar o pgadmnin ou outra interface, e pela linha de comando docker segue os comandos abaixo
docker exec -it nome-container bash
//com esse comando vc consegue entrar na maquina e depois só usar p psql pra dar os comandos do postgres
```
# MongoDB
link documentação:
- [oficial](https://www.mongodb.com/)
- [mongo-docker](https://hub.docker.com/_/mongo/)

comandos:
```js
docker pull mongo
docker run --name nome-container -p 27017:27017 -d -t mongo
//para acessar o banco pode usar o pgadmnin ou outra interface, e pela linha de comando docker segue os comandos abaixo
docker exec -it nome-container bash
```
# Postgre-XL
link documentação:
- [oficial](https://www.postgres-xl.org/)
- [Postgre-XL-docker](https://hub.docker.com/r/tiredpixel/postgres-xl/)

comandos:
```js
docker pull tiredpixel/postgres-xl
docker run --name nome-container -p 5432:5432 -d -t tiredpixel/postgres-xl
//para acessar o banco pode usar o pgadmnin ou outra interface, e pela linha de comando docker segue os comandos abaixo
docker exec -it nome-container bash
```
# Apache Ignite
link documentação:
- [oficial](https://ignite.apache.org/)
- [apacheignite-docker](https://hub.docker.com/r/apacheignite/ignite/)

comandos:
```js
sudo docker pull apacheignite/ignite
//Na teoria seria parecido com os outros mas nao sei ainda qual porta roda
docker run --name nome-container -d -t apacheignite/ignite
//para acessar o banco pode usar o pgadmnin ou outra interface, e pela linha de comando docker segue os comandos abaixo
docker exec -it nome-container bash
```
