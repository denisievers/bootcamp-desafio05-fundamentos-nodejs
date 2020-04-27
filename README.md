<h1 align="center">
    <img alt="GoStack" src="https://rocketseat-cdn.s3-sa-east-1.amazonaws.com/bootcamp-header.png" width="200px" />
</h1>

<h3 align="center">
  Desafio 05: Primeiro projeto Node.js
</h3>

## :rocket: Sobre o desafio

Neste desafio, foi desenvolvido uma aplicação que deve armazenar transações financeiras de entrada e saída, permitindo o cadastro e a listagem dessas transações.

### Rotas da aplicação

- **` POST /transactions`**: A rota deve receber **title**, **value**, **type** dentro do corpo da requisição, sendo **type** o tipo da transação, que deve ser **income** para entradas (depósitos) ou **outcome** para saídas (retiradas). Ao cadastrar uma nova transação, ela é armazenada dentro de um objeto com o seguinte formato:

```
{
  "id": "uuid",
  "title": "Salário",
  "value": 3000,
  "type": "income"
}
```

- **` GET /transactions`**: retorna uma listagem com todas as transações cadastradas, junto com o valor de soma de entradas, retiradas e total de crédito. Essa rota deve retornar um objeto com o formato a seguir:

```
{
  "transactions": [
    {
      "id": "uuid",
      "title": "Salário",
      "value": 4000,
      "type": "income"
    },
    {
      "id": "uuid",
      "title": "Freela",
      "value": 2000,
      "type": "income"
    },
    {
      "id": "uuid",
      "title": "Pagamento da fatura",
      "value": 4000,
      "type": "outcome"
    },
    {
      "id": "uuid",
      "title": "Cadeira Gamer",
      "value": 1200,
      "type": "outcome"
    }
  ],
  "balance": {
    "income": 6000,
    "outcome": 5200,
    "total": 800
  }
}
```
