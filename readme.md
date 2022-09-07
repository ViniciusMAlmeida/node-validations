# Aula 07 - Validações, throw Error

## Dependencias do projeto:

npm i nodemon sequelize-cli -D

npm i express pg pg-hstore sequelize jsonwebtoken bcryptjs express-async-errors 
<br><br>

## Configuração do projeto:

acessar diretório `./src/db` e rodar o comando `npx sequelize-cli init`

mudar a extensão do arquivo ./src/db/config/config.json para `.js` e exportar o
objeto de configuração

criar um arquivo `.sequelizerc` na raiz do projeto, configurar o path dos
diretórios

alterar a extensão (.json para .js) do arquivo de configuração `/src/db/models/index.js`
na linha 8, variável `config`
<br><br>

## Comandos do sequelize-cli:

criar migration
`npx sequelize-cli model:generate --name User --attributes firstName:string,lastName:string,email:string`

rodar migration
`npx sequelize-cli db:migrate`

desfazer migration
`npx sequelize-cli db:migrate:undo`


## Passos da aula

Partindo da aula anterior: <br>
Criar a classe AppError <br>
Importar a lib `express-async-errors` logo após a importação do `express` <br>
Criar o errorHandler, e adicionar no após a última rota <br>
Criar o UserService e transferir as reponsabilidades de regra de negócio para esta camada <br>
