# 🤖 Prompts e Cicatrizes — Engenharia de Prompts

## 1. Estratégia

O processo foi estruturado em quatro níveis:

```text
Pergunta ampla
     ↓
Pergunta contextualizada
     ↓
Pergunta com restrições e formato
     ↓
Pergunta com verificação crítica
```

A intenção foi evitar respostas genéricas e transformar a IA em uma ferramenta de aprendizagem ativa.

---

# 2. Registro dos testes

## Teste A — pergunta ampla

### Prompt

> Explique o que é uma API REST.

### Limitação

A pergunta não define nível, fontes, profundidade ou formato.

### Ajuste

Adicionar contexto, fontes e critérios de saída.

---

## Teste B — pergunta contextualizada

### Prompt

> Explique o que é uma API REST para um iniciante em TI e dê exemplos.

### Resultado esperado

Resposta mais acessível, porém ainda existe risco de generalização.

### Ajuste

Solicitar que a resposta use somente as fontes do notebook e organize os conceitos.

---

## Teste C — pergunta com fontes e estrutura

### Prompt

> Com base somente nas fontes deste caderno, explique o que é uma API REST para alguém que está começando em TI. Organize em definição, cliente-servidor, recurso, endpoint, métodos HTTP, requisição, resposta e exemplo. Cite a fonte de cada conceito.

### Resultado

Maior rastreabilidade e melhor organização para estudo.

### Aprendizado

Definir o formato da saída é tão importante quanto definir o assunto.

---

# 3. Teste de comparação

### Prompt

> Compare GET, POST, PUT, PATCH e DELETE em uma tabela. Inclua objetivo, exemplo de endpoint, alteração de dados e idempotência. Não invente regras que não estejam sustentadas pelas fontes.

### Aprendizado

A solicitação de uma tabela facilita comparação e revisão.

A restrição "não invente" também orienta a IA a distinguir documentação de inferência.

---

# 4. Teste de troubleshooting

### Prompt

> Um cliente enviou POST /usuarios e recebeu 201. Depois enviou GET /usuarios/15 e recebeu 404. Explique hipóteses possíveis sem afirmar uma causa que não possa ser determinada apenas pelos códigos. Separe o que o status informa, o que não informa e quais dados adicionais devem ser investigados.

### Aprendizado

Um bom prompt pode impedir que a IA transforme uma hipótese em diagnóstico.

---

# 5. Teste de segurança

### Prompt

> Usando a OWASP como fonte principal, explique os riscos de segurança de APIs para um desenvolvedor iniciante. Para cada risco, explique em linguagem simples, dê um exemplo hipotético e indique uma ideia geral de mitigação.

### Aprendizado

Foi útil combinar:

- fonte principal;
- público-alvo;
- estrutura;
- exemplos;
- mitigação.

---

# 6. Prompt final reutilizável

```text
Você é meu tutor de APIs REST.

Use prioritariamente as fontes fornecidas neste notebook e não trate conhecimento externo como se viesse das fontes.

Para o tema [TEMA]:

1. explique o conceito para iniciante;
2. apresente a definição técnica;
3. dê um exemplo prático;
4. diferencie conceitos parecidos;
5. aponte erros comuns;
6. faça 5 perguntas de revisão;
7. indique quais fontes sustentam cada parte;
8. destaque qualquer ponto que exija verificação adicional.

Se houver informação insuficiente nas fontes, diga explicitamente que a informação não está disponível nelas.
```

---

# 7. Principais cicatrizes

## Cicatriz: API ≠ REST

A API é uma interface; REST é um estilo arquitetural.

## Cicatriz: endpoint ≠ apenas URL

A operação também depende do método HTTP e do contrato da API.

## Cicatriz: status code ≠ diagnóstico

Um `404`, por exemplo, informa uma condição sobre a requisição, mas não explica sozinho toda a causa no sistema.

## Cicatriz: PUT ≠ PATCH

Ambos podem participar de operações de atualização, mas possuem semânticas diferentes.

## Cicatriz: autenticação ≠ autorização

Identificar o usuário não significa automaticamente conceder permissão para qualquer operação.

## Cicatriz: IA ≠ fonte de verdade

A resposta precisa ser comparada com documentação e fontes confiáveis.

---

# 8. Critério de qualidade utilizado

Uma resposta foi considerada mais útil quando:

- respondia exatamente à pergunta;
- estava vinculada às fontes;
- apresentava exemplos;
- separava fato de inferência;
- evitava generalizações;
- facilitava revisão posterior;
- indicava incertezas quando existiam.

---

# 9. Meta de aprendizagem

Ao repetir este processo em outros assuntos, manter a sequência:

```text
Definir tema
   ↓
Selecionar fontes
   ↓
Perguntar
   ↓
Comparar resposta com fontes
   ↓
Identificar lacunas
   ↓
Refinar prompt
   ↓
Testar novamente
   ↓
Consolidar conhecimento
```
