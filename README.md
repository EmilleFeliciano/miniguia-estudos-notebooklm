# 📘 Caderno Temático — Fundamentos de APIs REST

> Projeto prático para o desafio da DIO sobre aprendizagem ativa com Inteligência Artificial e NotebookLM.

![Status](https://img.shields.io/badge/status-concluído-brightgreen)
![Tema](https://img.shields.io/badge/tema-APIs%20REST-blue)
![Foco](https://img.shields.io/badge/foco-HTTP%20%7C%20OpenAPI%20%7C%20Segurança-orange)

## Sobre o projeto

Este repositório apresenta um **Caderno Temático sobre Fundamentos de APIs REST**, construído com apoio de Inteligência Artificial como ferramenta de aprendizagem ativa.

O material foi organizado para transformar fontes técnicas abertas em um guia de estudo objetivo, com:

- curadoria de fontes;
- perguntas estratégicas para investigação;
- engenharia de prompts;
- registro de variações e dificuldades;
- síntese dos conhecimentos;
- glossário;
- prompts reutilizáveis para futuras revisões.

O objetivo não é apenas obter respostas de uma IA, mas **aprender a formular perguntas, verificar informações nas fontes e consolidar conhecimento de forma estruturada**.

---

## 🎯 Contexto e objetivos

### Tema escolhido

**Fundamentos de APIs REST**

### Por que estudar este tema?

APIs fazem parte da integração entre sistemas, aplicações web, aplicativos móveis, serviços internos e soluções de terceiros. Para quem atua ou pretende atuar em TI, compreender HTTP, recursos, métodos, códigos de status, documentação e segurança é uma base importante para trabalhar com sistemas modernos.

### Objetivo geral

Construir uma visão prática e estruturada sobre APIs REST, compreendendo como uma API HTTP é organizada, consumida, documentada e protegida.

### Objetivos específicos

Ao final do estudo, pretendo ser capaz de:

1. Explicar o que é uma API e como funciona o modelo cliente-servidor.
2. Diferenciar recurso, endpoint, URI/URL, método HTTP, header e body.
3. Explicar o uso de GET, POST, PUT, PATCH e DELETE.
4. Interpretar os principais códigos de status HTTP.
5. Compreender o papel do JSON em APIs.
6. Identificar conceitos básicos de autenticação e autorização.
7. Entender a finalidade do OpenAPI.
8. Reconhecer riscos comuns de segurança em APIs.
9. Analisar uma API simples a partir de sua documentação.
10. Utilizar prompts estruturados para revisar e aprofundar o conhecimento.

---

# 📚 1. Curadoria de fontes

As fontes abaixo foram selecionadas por serem abertas, técnicas e provenientes de organizações/projetos reconhecidos.

| # | Fonte | Conteúdo utilizado | Motivo da seleção |
|---|---|---|---|
| 1 | MDN Web Docs — Overview of HTTP | Fundamentos de HTTP, cliente-servidor, requisição e resposta | Fonte técnica de referência para Web |
| 2 | MDN Web Docs — HTTP Request Methods | GET, POST, PUT, PATCH, DELETE e propriedades dos métodos | Ajuda a entender a semântica dos métodos |
| 3 | Microsoft Learn — Azure REST API Reference | Estrutura de requisições/respostas REST, headers, body e status | Apresenta REST de maneira aplicada |
| 4 | OpenAPI Initiative — OpenAPI Specification | Descrição e documentação de APIs HTTP | Base para compreender documentação de APIs |
| 5 | OWASP — API Security Top 10 | Principais riscos de segurança específicos de APIs | Introduz segurança e visão de DevSecOps |

### Links das fontes

1. MDN — Overview of HTTP  
   https://developer.mozilla.org/en-US/docs/Web/HTTP/Guides/Overview

2. MDN — HTTP request methods  
   https://developer.mozilla.org/en-US/docs/Web/HTTP/Reference/Methods

3. Microsoft Learn — Azure REST API Reference  
   https://learn.microsoft.com/en-us/rest/api/gettingstarted/

4. OpenAPI Specification  
   https://spec.openapis.org/oas/

5. OWASP API Security Top 10  
   https://owasp.org/www-project-api-security/

> **Uso no NotebookLM:** essas páginas podem ser adicionadas como fontes pelo endereço web. O objetivo é manter as respostas da IA vinculadas às fontes selecionadas, reduzindo o risco de respostas sem fundamentação.

---

# 🤖 2. Engenharia de prompts

A estratégia utilizada foi evoluir de perguntas amplas para perguntas com:

- contexto;
- objetivo;
- restrição de fontes;
- formato de saída;
- comparação;
- exemplos;
- verificação de entendimento.

## Prompt inicial

```text
Explique o que é uma API REST.
```

### Problema identificado

A pergunta é ampla. Uma resposta pode ser correta, mas superficial, e não necessariamente cobrir HTTP, recursos, métodos, status codes, documentação e segurança.

---

## Prompt refinado 1 — explicação estruturada

```text
Com base somente nas fontes deste caderno, explique o que é uma API REST para alguém que está começando em TI.

Organize a resposta em:
1. definição;
2. modelo cliente-servidor;
3. recurso e endpoint;
4. métodos HTTP;
5. requisição;
6. resposta;
7. exemplo prático.

Para cada conceito técnico, cite a fonte utilizada.
```

### Melhoria

A pergunta passou a definir:

- nível do estudante;
- fontes permitidas;
- estrutura da resposta;
- necessidade de referências;
- exemplo prático.

---

## Prompt refinado 2 — comparação

```text
Compare GET, POST, PUT, PATCH e DELETE.

Crie uma tabela com:
- objetivo;
- exemplo de endpoint;
- uso típico;
- alteração de dados;
- característica de idempotência quando aplicável.

Não invente regras que não estejam sustentadas pelas fontes. Ao final, destaque as diferenças que um iniciante mais costuma confundir.
```

### Melhoria

A comparação reduz respostas genéricas e facilita a revisão posterior.

---

## Prompt refinado 3 — troubleshooting

```text
Analise esta situação:

"Um cliente enviou POST /usuarios e recebeu 201. Depois enviou GET /usuarios/15 e recebeu 404."

Explique hipóteses tecnicamente possíveis sem afirmar uma causa que não possa ser determinada apenas pelos códigos.

Separe:
- o que o status code informa;
- o que ele não informa;
- quais dados adicionais eu deveria investigar.
```

### Aprendizado

Um código HTTP representa uma parte do resultado da operação. Ele não substitui a investigação de logs, payload, headers, rota, autenticação/autorização e regras da aplicação.

---

## Prompt refinado 4 — segurança

```text
Usando a fonte da OWASP como referência principal, explique os riscos de segurança de APIs para um desenvolvedor iniciante.

Para cada risco:
- explique em linguagem simples;
- dê um exemplo hipotético;
- indique a ideia geral de mitigação;
- diferencie autenticação de autorização quando necessário.

Não transforme a explicação em tutorial de exploração.
```

### Melhoria

O prompt orienta a IA a ensinar segurança de maneira defensiva, conectando conceito, exemplo e mitigação.

---

# 🩹 3. Cicatrizes do aprendizado / Troubleshooting

A expressão "cicatrizes" representa os erros, dúvidas e ajustes que fizeram parte do processo de investigação.

## Cicatriz 1 — confundir API com REST

**Problema:** tratar API e REST como sinônimos.

**Correção:** API é uma interface que permite comunicação entre software. REST é um estilo arquitetural. Uma API pode utilizar HTTP e seguir princípios REST, mas os termos não são equivalentes.

**Aprendizado:** antes de decorar métodos, é necessário separar "o que é uma API" de "como uma API pode ser projetada".

---

## Cicatriz 2 — tratar endpoint e recurso como a mesma coisa

**Problema:** usar os termos indistintamente.

**Correção conceitual:**

- **recurso:** entidade/conceito exposto pela API, como usuários;
- **URI/rota:** identificação/localização utilizada para acessar o recurso;
- **endpoint:** ponto de interação disponibilizado pela API, normalmente associado a uma rota e a uma operação HTTP.

**Aprendizado:** uma rota sozinha não explica toda a operação; o método HTTP também importa.

---

## Cicatriz 3 — decorar status codes sem entender o contexto

**Problema:** memorizar `200`, `201`, `400`, `401`, `403`, `404` e `500` como se fossem respostas absolutas.

**Correção:** códigos devem ser interpretados dentro da operação realizada e da documentação da API.

Exemplo:

- `401` está relacionado à ausência ou falha de autenticação;
- `403` indica que a requisição foi entendida, mas o acesso à operação/recurso não é permitido naquele contexto;
- `404` indica que o recurso solicitado não foi encontrado, embora detalhes exatos dependam da aplicação.

**Aprendizado:** status code é evidência, não diagnóstico completo.

---

## Cicatriz 4 — assumir que PUT e PATCH são iguais

**Problema:** ambos podem ser associados a "atualização".

**Correção:** o HTTP define semânticas diferentes. PUT é utilizado para substituir a representação atual do recurso alvo pelo conteúdo da requisição; PATCH aplica modificações parciais.

**Aprendizado:** não basta saber o nome do método; é necessário conhecer sua semântica.

---

## Cicatriz 5 — acreditar que documentação é apenas um texto explicativo

**Problema:** considerar OpenAPI apenas como uma página de documentação.

**Correção:** a OpenAPI Specification define uma forma padronizada e independente de linguagem para descrever APIs HTTP, podendo alimentar ferramentas de documentação, geração de código e testes.

**Aprendizado:** documentação de API também pode ser um artefato técnico estruturado.

---

# 📖 4. Miniguia de estudo

## 4.1 O que é uma API?

API significa **Application Programming Interface**.

Uma API define uma forma estruturada para que softwares interajam. Em uma API HTTP, um cliente envia uma requisição para um servidor e recebe uma resposta.

Exemplo conceitual:

```text
Cliente
   |
   | GET /usuarios/15
   v
API
   |
   | 200 OK
   | {"id":15,"nome":"Ana"}
   v
Cliente
```

---

## 4.2 O modelo cliente-servidor

Uma comunicação HTTP normalmente envolve:

### Cliente

É quem inicia a requisição.

Exemplos:

- navegador;
- aplicativo mobile;
- frontend;
- outro servidor;
- ferramenta de testes.

### Servidor

Recebe a requisição, executa regras da aplicação e produz uma resposta.

---

## 4.3 Anatomia de uma requisição

Uma requisição HTTP pode conter:

```http
GET /usuarios/15 HTTP/1.1
Host: api.exemplo.com
Accept: application/json
Authorization: Bearer TOKEN
```

Principais partes:

- método HTTP;
- caminho/rota;
- headers;
- eventualmente body.

---

## 4.4 Anatomia de uma resposta

Exemplo:

```http
HTTP/1.1 200 OK
Content-Type: application/json

{
  "id": 15,
  "nome": "Ana"
}
```

A resposta pode conter:

- status code;
- headers;
- body.

---

# 5. Principais métodos HTTP

| Método | Ideia principal | Exemplo |
|---|---|---|
| GET | obter uma representação/recurso | `GET /usuarios/15` |
| POST | enviar dados para criação/processamento | `POST /usuarios` |
| PUT | substituir a representação do recurso alvo | `PUT /usuarios/15` |
| PATCH | aplicar alteração parcial | `PATCH /usuarios/15` |
| DELETE | remover um recurso | `DELETE /usuarios/15` |

### Regra mental

```text
GET     → consultar
POST    → criar/enviar
PUT     → substituir
PATCH   → alterar parcialmente
DELETE  → remover
```

Essa associação é uma simplificação didática. A semântica real deve ser consultada na documentação do método HTTP e na documentação da API.

---

# 6. Status codes

Os códigos de resposta HTTP são divididos em cinco grandes classes:

| Faixa | Significado |
|---|---|
| 1xx | informação |
| 2xx | sucesso |
| 3xx | redirecionamento |
| 4xx | erro relacionado à requisição |
| 5xx | erro relacionado ao servidor |

Alguns códigos importantes:

| Código | Uso comum |
|---|---|
| 200 | requisição processada com sucesso |
| 201 | recurso criado com sucesso |
| 204 | sucesso sem conteúdo na resposta |
| 400 | requisição inválida |
| 401 | autenticação necessária/ausente ou inválida |
| 403 | acesso não permitido |
| 404 | recurso não encontrado |
| 409 | conflito com o estado atual |
| 500 | erro interno do servidor |

> A documentação específica da API continua sendo a referência para o comportamento exato de cada operação.

---

# 7. JSON

JSON é um formato muito utilizado para representar dados em APIs.

Exemplo:

```json
{
  "id": 15,
  "nome": "Ana",
  "email": "ana@example.com"
}
```

Vantagens práticas:

- estrutura simples;
- fácil leitura humana;
- amplo suporte em linguagens;
- adequado para representar objetos e listas.

---

# 8. Autenticação x autorização

### Autenticação

Responde:

> "Quem é você?"

Exemplo: apresentação de credenciais ou token.

### Autorização

Responde:

> "O que você pode fazer?"

Exemplo: um usuário autenticado pode consultar seus próprios dados, mas não necessariamente alterar dados de outro usuário.

Essa diferença é especialmente importante para segurança de APIs.

---

# 9. Segurança de APIs

A OWASP mantém o **API Security Top 10**, que reúne riscos específicos relevantes para APIs.

Entre os riscos abordados na edição 2023 estão:

1. Broken Object Level Authorization;
2. Broken Authentication;
3. Broken Object Property Level Authorization;
4. Unrestricted Resource Consumption;
5. Broken Function Level Authorization;
6. Unrestricted Access to Sensitive Business Flows;
7. Server Side Request Forgery;
8. Security Misconfiguration;
9. Improper Inventory Management;
10. Unsafe Consumption of APIs.

### Princípio prático

Não basta verificar se o usuário está autenticado.

É necessário avaliar, conforme a aplicação:

- qual usuário está realizando a ação;
- qual recurso está sendo acessado;
- quais propriedades podem ser alteradas;
- qual função está sendo chamada;
- quais dados podem ser retornados;
- quais serviços externos são consumidos.

---

# 10. OpenAPI

A **OpenAPI Specification** fornece uma forma padronizada e independente de linguagem para descrever APIs HTTP.

Uma descrição OpenAPI pode representar informações como:

- endpoints;
- métodos;
- parâmetros;
- respostas;
- schemas;
- autenticação;
- informações da API.

Exemplo simplificado:

```yaml
openapi: 3.1.0

info:
  title: API de Usuários
  version: 1.0.0

paths:
  /usuarios/{id}:
    get:
      summary: Busca um usuário
      parameters:
        - name: id
          in: path
          required: true
          schema:
            type: integer
      responses:
        "200":
          description: Usuário encontrado
        "404":
          description: Usuário não encontrado
```

A especificação pode ser utilizada por ferramentas para documentação, geração de código e testes.

---

# 11. Exemplo completo de fluxo

Imagine uma aplicação de cadastro de usuários.

### Criar usuário

```http
POST /usuarios
Content-Type: application/json

{
  "nome": "Maria",
  "email": "maria@example.com"
}
```

Resposta possível:

```http
201 Created
Content-Type: application/json

{
  "id": 21,
  "nome": "Maria",
  "email": "maria@example.com"
}
```

### Consultar usuário

```http
GET /usuarios/21
```

Resposta:

```http
200 OK

{
  "id": 21,
  "nome": "Maria",
  "email": "maria@example.com"
}
```

### Alterar parcialmente

```http
PATCH /usuarios/21
Content-Type: application/json

{
  "nome": "Maria Silva"
}
```

### Remover

```http
DELETE /usuarios/21
```

Uma API real pode utilizar outros campos, regras, autenticação, paginação, versionamento e respostas específicas.

---

# 🧠 12. Checklist de revisão

Antes de considerar o conteúdo dominado, consigo responder:

- [ ] O que é uma API?
- [ ] O que é HTTP?
- [ ] Qual é a função de cliente e servidor?
- [ ] O que é um recurso?
- [ ] O que é um endpoint?
- [ ] Para que serve GET?
- [ ] Qual a diferença entre POST e PUT?
- [ ] Qual a diferença entre PUT e PATCH?
- [ ] Para que serve DELETE?
- [ ] O que significa a classe 2xx?
- [ ] Qual a diferença conceitual entre 401 e 403?
- [ ] O que é JSON?
- [ ] Qual a diferença entre autenticação e autorização?
- [ ] Para que serve OpenAPI?
- [ ] Por que segurança de API precisa considerar autorização por objeto?
- [ ] Consigo interpretar uma requisição e uma resposta HTTP?

---

# 🗂️ 13. Glossário

| Termo | Definição curta |
|---|---|
| API | Interface que permite interação estruturada entre componentes de software |
| REST | Estilo arquitetural associado a sistemas distribuídos |
| HTTP | Protocolo utilizado para comunicação na Web e em APIs |
| Cliente | Componente que inicia uma requisição |
| Servidor | Componente que recebe a requisição e produz uma resposta |
| Recurso | Entidade/conceito exposto por uma API |
| Endpoint | Ponto de interação de uma API |
| URI | Identificador de um recurso |
| URL | Localizador de recurso que inclui informações para acesso |
| Método HTTP | Indica a intenção da operação HTTP |
| Header | Metadado transmitido na requisição ou resposta |
| Body | Conteúdo principal da mensagem HTTP |
| Status code | Código que indica o resultado da requisição |
| JSON | Formato textual estruturado para representação de dados |
| Autenticação | Processo de verificar identidade |
| Autorização | Processo de determinar permissões |
| Token | Credencial/dado utilizado para representar ou conceder acesso |
| OpenAPI | Especificação para descrever APIs HTTP |
| Schema | Estrutura esperada dos dados |
| Idempotência | Propriedade na qual múltiplas requisições equivalentes têm o mesmo efeito pretendido no estado do servidor, conforme a semântica HTTP |
| CORS | Mecanismo de segurança relacionado a requisições entre diferentes origens em navegadores |
| Paginação | Técnica de dividir grandes conjuntos de resultados em páginas |
| Versionamento | Estratégia para administrar mudanças de contrato de uma API |

---

# ♻️ 14. Prompts reutilizáveis

## Prompt 1 — resumo

```text
Use somente as fontes deste caderno.

Resuma [TEMA] para uma pessoa iniciante em TI.

Estruture em:
- definição;
- conceitos fundamentais;
- exemplo;
- erros comuns;
- resumo em 5 linhas.

Sempre diferencie fato documentado de inferência.
```

## Prompt 2 — revisão ativa

```text
Faça 10 perguntas sobre [TEMA], uma por vez.

Não revele a resposta antes de eu responder.

Depois de cada resposta:
1. diga se está correta;
2. explique o que faltou;
3. cite a fonte correspondente;
4. faça a próxima pergunta.
```

## Prompt 3 — comparação

```text
Compare [CONCEITO A] e [CONCEITO B].

Monte uma tabela com:
- definição;
- objetivo;
- quando usar;
- exemplo;
- diferença principal;
- erro comum de iniciante.

Use somente as fontes fornecidas.
```

## Prompt 4 — análise de erro

```text
Analise este cenário de API:

[COLE O CENÁRIO]

Separe a análise em:
1. fatos observáveis;
2. hipóteses possíveis;
3. informações que estão faltando;
4. testes que ajudariam a confirmar a causa;
5. conclusão limitada ao que as evidências permitem afirmar.

Não invente informações.
```

## Prompt 5 — preparação para entrevista

```text
Com base nas fontes deste caderno, simule uma entrevista técnica de nível iniciante sobre APIs REST.

Faça uma pergunta por vez.

Depois da minha resposta:
- avalie tecnicamente;
- corrija imprecisões;
- explique uma resposta melhor;
- informe qual conceito da fonte sustenta a explicação.
```

## Prompt 6 — transformar documentação em estudo

```text
Transforme a documentação abaixo em um material de estudo:

[DOCUMENTAÇÃO]

Produza:
- resumo;
- conceitos-chave;
- tabela de referência;
- exemplo;
- perguntas de revisão;
- glossário;
- pontos que merecem aprofundamento.

Não acrescente informação externa sem identificá-la.
```

## Prompt 7 — auditoria da resposta da IA

```text
Revise sua própria resposta anterior.

Classifique cada afirmação como:
- diretamente sustentada pela fonte;
- inferência razoável;
- informação que precisa de verificação.

Aponte qualquer afirmação excessivamente genérica ou potencialmente ambígua.
```

---

# 📌 15. Conclusões do estudo

O estudo mostrou que compreender APIs REST exige mais do que memorizar métodos HTTP.

Os principais aprendizados foram:

1. **HTTP é a base da comunicação**, fornecendo semântica para requisições, respostas, métodos, headers e status codes.
2. **Métodos HTTP possuem semânticas próprias**, por isso GET, POST, PUT, PATCH e DELETE não devem ser tratados apenas como palavras-chave.
3. **Status codes precisam ser interpretados em contexto** e não substituem logs ou investigação técnica.
4. **OpenAPI transforma a documentação da API em um artefato estruturado**, útil para pessoas e ferramentas.
5. **Segurança de APIs envolve autorização, autenticação, validação, configuração, inventário e consumo seguro de serviços**, entre outros aspectos.
6. **Prompts mais específicos produzem respostas mais úteis para estudo**, especialmente quando definem fontes, formato, nível de conhecimento e critérios de verificação.
7. **A IA funciona melhor como ferramenta de investigação e revisão quando suas respostas são confrontadas com fontes**, em vez de serem tratadas automaticamente como verdade.

---

# 🚀 16. Como reproduzir este estudo no NotebookLM

1. Criar um notebook no NotebookLM.
2. Adicionar as 5 fontes listadas em `fontes/fontes.md`.
3. Utilizar os prompts de `estudos/prompts-e-cicatrizes.md`.
4. Comparar as respostas da IA com as fontes.
5. Registrar dúvidas, erros e ajustes de prompts.
6. Usar `estudos/miniguia.md` como síntese final.
7. Revisar o conteúdo antes de publicar o repositório.

---

# 📁 Estrutura do repositório

```text
miniguia-estudos-notebooklm/
├── README.md
├── fontes/
│   └── fontes.md
└── estudos/
    ├── miniguia.md
    └── prompts-e-cicatrizes.md
```

---

## 🏆 Competências demonstradas

Este projeto demonstra:

- pesquisa técnica;
- curadoria de fontes;
- pensamento crítico;
- engenharia de prompts;
- documentação;
- organização de conhecimento;
- fundamentos de APIs;
- fundamentos de segurança;
- uso responsável de IA;
- capacidade de transformar informação técnica em material de estudo.

---

## 👩‍💻 Autoria

**Emille Feliciano**

Projeto desenvolvido para o desafio da **DIO — Caderno Temático com NotebookLM**.

---

## 📄 Licença

Este repositório contém material autoral de síntese e referências externas. As fontes externas permanecem sujeitas às respectivas licenças e termos de uso.

O conteúdo autoral deste repositório pode ser utilizado para fins de estudo e portfólio.
