# Webapi

Este projeto foi configurado com as tecnologias .net core version 2.2 onde expõe endpoints como integração na parte do back-end.

## Tecnologias e padrões utilizados

- ASP.NET Core 2.2
- Entity Framework Core 2.2.
- SQL Server para database.
- Visual Studio Code.
- DDD

## Build

Executar `dotnet build` para buildar o projeto.

## Running

Executar `dotnet run` para executar o projeto. 

## Configure

Para configurar o ambiente de produção antes de executar o projeto, no arquivo Webapi/Data/Dao.cs, defina o ambiente em que o projeto irá rodar como "producao ou teste" assim ele irá saber de onde irá buscar a fonte de dados.

## Swagger 

Como ambiente de documentação da api, está configurado com o framework swagger na versão 4.0.1, ao executar a aplicação no passo 'Running' basta ir no endereço https://localhost:porta/swagger que irá visualizar a documentação da api.

## Docker

Para configurar o ambiente no container, execute `dotnet publish -o ./dist` para gerar build da aplicação, depois execute o comando `docker build -t webapi-mac:1.0 .` para criar a imagem. Depois execute `docker container run -p 5001:80 webapi-mac:1.0` para executar no container.
(Não esquecer de colocar `http` nos services da aplicação angular)