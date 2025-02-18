# Iniciando projeto node
Abrir terminal na pasta do projeto
npm init -y 
-y para responder tudo com sim

## LIB express
npm i express

## Criar server.js
Adicionar "type": "module", no arquivo package.json.

## Thunder Client
Um plugin que funciona como o POSTMAN

Para fazer com que o servidor reinicie toda vez que salvar um arquivo
node --watch server.js

## MongoDB
User DB
thiag0benites2023
pass
0C4ekvHCglvGMOy3

mongodb+srv://thiag0benites2023:0C4ekvHCglvGMOy3@cluster0.eevdq.mongodb.net/?retryWrites=true&w=majority&appName=Cluster0

No site acessar o menu Network access. Esta configurado para acessar so do meu IP.
Clicar em editar e selecionar ALLOW ACCESS FROM ANYWHERE

Acessar o menu Database access editar e colocar usuario como admin
Clicar em
Built-in role e selecionar Atlas Adm

## Instalar o Prisma.io
Lib para poder manipular o mongodb via codigo.
Acessar
https://www.prisma.io/docs/getting-started/setup-prisma/start-from-scratch/mongodb/creating-the-prisma-schema-typescript-mongodb

npm install prisma --save-dev

 npx prisma init

 Vai criar .env onde vamos configurar a conexao com o bd.
 Para pegar a sting de conexao no site acessar o banco clicar em connect>drivers

 Reparar que na string de conexao depois de mongodb.net/deve se colocar o nome do BD que no caso e Cluster0

 mongodb+srv://thiag0benites2023:0C4ekvHCglvGMOy3@cluster0.eevdq.mongodb.net/Cluster0?retryWrites=true&w=majority&appName=Cluster0

 Na arquivo prisma/schema.prisma

 datasource db {
  provider = "mongodb"
  url      = env("DATABASE_URL")
}

Neste link https://www.prisma.io/docs/getting-started/setup-prisma/start-from-scratch/mongodb/creating-the-prisma-schema-typescript-mongodb

Estao os models que vamos utilizar no schema.prisma

Depois de configurar os schemas rodar 
npx prisma db push

Instalar o prisma client
npm install @prisma/client

Para abrir uma interface grafica para ver os dados do banco
npx prisma studio

## Instalar o cors
Permite que o front acesse a api
npm install cors