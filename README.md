# 🐬 MySQL com Docker

Este repositório contém instruções para subir um container MySQL usando Docker de forma rápida e prática.

## 🚀 Subindo o MySQL com Docker

Você pode rodar rapidamente um container MySQL utilizando o comando abaixo:

```
docker run -d \
  --name mysql-container \
  -e MYSQL_ROOT_PASSWORD=rootpassword \
  -e MYSQL_DATABASE=meu_banco \
  -e MYSQL_USER=usuario \
  -e MYSQL_PASSWORD=senha123 \
  -p 3306:3306 \
  -v mysql_data:/var/lib/mysql \
  mysql:8.0
```

## Acessando o MySQL via terminal:

```
docker exec -it mysql-container mysql -u root -p
```

Digite a senha rootpassword quando solicitado.

## Conectando com o DBeaver ou Workbench
Se estiver utilizando um cliente gráfico para bancos de dados, use as seguintes configurações:
- Host: localhost
- Porta: 3306
- Usuário: usuario ou root
- Senha: senha123 ou rootpassword
- Banco: meu_banco