# cupcake-e-commerce-database
Banco de dados para o projeto e-commerce de cupcakes

[![Postgresql](https://img.shields.io/badge/Postgresql-17-blue?logo=postgresql&color=rgb(98,148,189))](https://www.postgresql.org/)
[![Docker](https://img.shields.io/badge/Docker%20Desktop-4.5-blue?logo=docker&color=rgb(37,96,255))](https://www.docker.com/products/docker-desktop/)
[![DBeaver](https://img.shields.io/badge/DBeaver-25-brown?logo=dbeaver&color=rgb(56,41,35))](https://dbeaver.io/)

## Instruções:

### Executar o Banco de Dados localmente:

-  Para executar localmente o servidor de banco de dados Postgresql do projeto, execute o comando abaixo na raiz deste repositório:

```bash
docker-compose up -d
```
### Criação do Banco de Dados cupcake:

-  Conecte ao banco de dados usando alguma ferramenta como DBeaver ou equivalente
-  Execute os comandos sql:

```sql
CREATE DATABASE cupcake;
CREATE USER postgres WITH PASSWORD 'password';
ALTER ROLE postgres SET client_encoding TO 'utf8' ;
ALTER ROLE postgres SET default_transaction_isolation TO 'read committed' ;
ALTER ROLE postgres SET timezone TO 'UTC' ;
GRANT ALL PRIVILEGES ON DATABASE cupcake TO postgres ;
```
-  As tabelas serão criadas automaticamente a partir das migrations do Django, quando o backend for executado conectado ao Banco de Dados.

### Finalizar o Banco de Dados local

-  Para finalizar a execução do servidor, execute o comando abaixo na raiz deste repositório:

```bash
docker-compose down
```

## Autor

-  **Nome:** Artur de Paula Coutinho
-  **RGM:** 29655960
-  **Curso:** Engenharia de Software
-  **Instituição:** UNICID
