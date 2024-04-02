
# Todo List com Asp.NET 6.0

## Rotas da API para Gerenciamento de Tarefas

Este documento descreve as rotas da API disponíveis para gerenciar seus itens de tarefas. Essas rotas são implementadas na classe `HomeController`.

## URL Base

`http://localhost:<porta>/api/`

Substitua `<porta>` pela porta real em que seu aplicativo ASP.NET Core está rodando.

## Rotas

1. **GET /todos**: Recupera uma lista de todos os itens de tarefas.
2. **GET /todos/{id}**: Recupera um item de tarefa específico pelo seu ID.
3. **POST /todos**: Cria um novo item de tarefa. O corpo da requisição deve conter um objeto JSON representando o novo item de tarefa, com propriedades como `titulo` e `feito`.
4. **PUT /todos/{id}**: Atualiza um item de tarefa existente identificado pelo seu ID. O corpo da requisição deve conter um objeto JSON com as propriedades atualizadas do item de tarefa.
5. **DELETE /todos/{id}**: Exclui um item de tarefa pelo seu ID.

## Formato do Corpo da Requisição (para POST e PUT)

```json
{
  "title": "Sua Tarefa Aqui",
  "done": false,
  "createdAt": "2024-04-02T00:00:00"
}
```


## Estruturas de Pastas
```
TodoApi
  |—— .gitignore
  |—— Controllers
  |    |—— HomeController.cs
  |—— Data
  |    |—— AppDbContext.cs
  |—— Migrations
  |—— Models
  |    |—— Todo.cs
  |—— Program.cs
  |—— Properties
  |    |—— launchSettings.json
  |—— app.db
  |—— app.db-shm
  |—— app.db-wal
  |—— appsettings.Development.json
  |—— appsettings.json
  |—— bin
  |—— obj
  |—— todoApi.csproj
  |—— todoApi.sln
```