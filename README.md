## Node API

Uma simples API feita em NodeJS para manipular um banco de dados MySQL.

### Instalação

1. Clone o repositório
2. Entre na pasta do projeto
3. Instale as dependências
```bash
npm install
```
4. Crie um arquivo `.env` na raiz do projeto com as seguintes variáveis de ambiente:
```bash
PORT=
CONNECTION_STRING=mysql://yourusername:yourpassword@localhost:port/your_database
```
5. Execute o projeto
```bash
npm start
```

### Rotas

| Método | Caminho | Descrição |
| ------ | ------ | --------- |
| GET    | /clientes | Retorna todos os clientes |
| GET    | /clientes/:id | Retorna o cliente com o ID especificado |
| POST   | /clientes | Insere um novo cliente |
| PATCH  | /clientes/:id | Atualiza o cliente com o ID especificado |
| DELETE | /clientes/:id | Exclui o cliente com o ID especificado |

### Exemplo de requisição

#### GET /clientes

Retorna todos os clientes

```bash
curl -X GET http://localhost:3000/clientes
```

#### GET /clientes/:id

Retorna o cliente com o ID especificado

```bash
curl -X GET http://localhost:3000/clientes/1
```

#### POST /clientes

Insere um novo cliente

```bash
curl -X POST http://localhost:3000/clientes \
  -H 'Content-Type: application/json' \
  -d '{
    "nome": "João",
    "idade": 30,
    "uf": "SP"
  }'
```

#### PATCH /clientes/:id

Atualiza o cliente com o ID especificado

```bash
curl -X PATCH http://localhost:3000/clientes/1 \
  -H 'Content-Type: application/json' \
  -d '{
    "nome": "João",
    "idade": 30,
    "uf": "SP"
  }'
```

#### DELETE /clientes/:id

Exclui o cliente com o ID especificado

```bash
curl -X DELETE http://localhost:3000/clientes/1
```
