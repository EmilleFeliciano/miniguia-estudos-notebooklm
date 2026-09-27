# 📖 Miniguia de Estudo — Fundamentos de APIs REST

## 1. Mapa mental

```text
API REST
│
├── HTTP
│   ├── Request
│   │   ├── Method
│   │   ├── URI
│   │   ├── Headers
│   │   └── Body
│   │
│   └── Response
│       ├── Status Code
│       ├── Headers
│       └── Body
│
├── Dados
│   └── JSON
│
├── Contrato
│   └── OpenAPI
│
└── Segurança
    ├── Autenticação
    ├── Autorização
    ├── Validação
    ├── Configuração
    └── Controle de acesso
```

## 2. Resumo de uma página

Uma API permite que componentes de software se comuniquem por meio de uma interface definida. Em APIs HTTP, o cliente envia uma requisição e o servidor retorna uma resposta.

Os métodos HTTP expressam a intenção da operação. Os mais utilizados em APIs são GET, POST, PUT, PATCH e DELETE, cada um com semântica própria.

A resposta HTTP contém um status code que informa o resultado da requisição. Os códigos são agrupados em cinco classes: 1xx, 2xx, 3xx, 4xx e 5xx.

JSON é um formato comum para representar dados em requisições e respostas.

Autenticação e autorização são conceitos diferentes: autenticação trata da identidade; autorização trata das permissões.

OpenAPI permite descrever uma API de maneira padronizada, possibilitando que pessoas e ferramentas entendam seu contrato.

Segurança de APIs exige atenção especial a controle de acesso, autenticação, exposição de dados, consumo de recursos, configurações e integrações externas.

## 3. Perguntas para revisão

1. O que é uma API?
2. Qual é a função do HTTP em uma API?
3. O que diferencia recurso e endpoint?
4. Quando usamos GET?
5. Qual a diferença entre PUT e PATCH?
6. O que significa um status 4xx?
7. Qual a diferença entre 401 e 403?
8. O que é JSON?
9. Qual a diferença entre autenticação e autorização?
10. Para que serve OpenAPI?
11. Por que autorização por objeto é importante?
12. Por que um status code não é suficiente para diagnosticar um incidente?

## 4. Exercício prático

Considere:

```text
GET /produtos/10
```

Responda:

- Qual é o método?
- Qual é o recurso?
- Qual é o identificador?
- Que tipo de operação é esperada?
- Qual seria uma resposta de sucesso plausível?
- Qual status poderia indicar que o produto não foi encontrado?

Depois, crie mentalmente:

```text
POST /produtos
PUT /produtos/10
PATCH /produtos/10
DELETE /produtos/10
```

Explique a intenção de cada operação.

## 5. Desafio final

Imagine uma API de biblioteca.

Recursos:

- livros;
- autores;
- usuários;
- empréstimos.

Crie uma tabela com pelo menos cinco endpoints e indique:

- método;
- rota;
- objetivo;
- status de sucesso possível;
- possíveis erros.

Depois, pergunte ao NotebookLM para revisar seu desenho usando as fontes.

## 6. Regra de ouro

> Não memorize somente "qual método usar". Entenda o recurso, a intenção da operação, a semântica HTTP, o contrato da API e as regras de segurança.
