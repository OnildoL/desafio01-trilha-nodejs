<p align="center">
  <a href="#-tecnologias">Tecnologias</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#-desafio">Desafio</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#-como-executar">Como executar</a>&nbsp;&nbsp;&nbsp;
</p>

<br>

## ✨ Tecnologias

Esse projeto foi desenvolvido com as seguintes tecnologias:

- [Node.js](https://nodejs.org/en/)
- [Express](https://expressjs.com/pt-br/)

## 💻 Desafio

Criar uma aplicação para treinar o que aprendeu na trilha  Node.js Chapter I!

Uma aplicação para gerenciar tarefas. Será permitida a criação de um usuário com `name` e `username`, bem como fazer o CRUD das tarefas:

- Criar uma nova tarefa;
- Listar todas as tarefas;
- Alterar o `title` e `deadline` de uma tarefa existente;
- Marcar uma tarefa como feita;
- Excluir uma tarefa;

Tudo isso para cada usuário em específico (o `username` será passado pelo header).

## 🚀 Como executar

- Clone o repositório
- Instale as dependências com `yarn` ou `npm i` 
- Inicie o servidor com `yarn dev` ou `npm run dev` 

Agora você pode acessar [`localhost:3333`](http://localhost:3333) no [Insomnia](https://insomnia.rest/download) ou [Postman](https://www.postman.com/).

---

## ▶️ Rotas

### Criar um novo usuário:
POST - http://localhost:3333/users
</br>
Body params:
```JSON
{
  "name": "Onildo Lima",
  "username": "Scorpion"
}
```

### Criar uma nova tarefa:
POST - http://localhost:3333/todos
</br>
Header:
```JSON
{ 
  "username": "Scorpion" 
}
```
Body params:
```JSON
{
  "title": "Jogar bola",
  "deadline": "2021-11-02"
}
```

### Listar todas as tarefas de um usuário:
GET - http://localhost:3333/todos
</br>
Header:
```JSON
{ 
  "username": "Scorpion" 
}
```

### Atualizar uma tarefa:
PUT - http://localhost:3333/todos/4b54c045-3ef1-4ccf-8ba4-43ccfacdc613
</br>
Header:
```JSON
{ 
  "username": "Scorpion" 
}
```
Body params:
```JSON
{
  "title": "Jogar videogame",
  "deadline": "2021-11-02"
}
```

### Concluir uma tarefa:
PATCH - http://localhost:3333/todos/4b54c045-3ef1-4ccf-8ba4-43ccfacdc613/done
</br>
Header:
```JSON
{ 
  "username": "Scorpion" 
}
```

### Deletar uma tarefa:
DELETE - http://localhost:3333/todos/4b54c045-3ef1-4ccf-8ba4-43ccfacdc613
</br>
Header:
```JSON
{ 
  "username": "Scorpion" 
}
```
