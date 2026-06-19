# 📓 Caderno Temático de IA: Reserva de Emergência e Organização Financeira Pessoal

> Projeto desenvolvido com o **NotebookLM** como ferramenta de estudo ativo, aplicando curadoria de fontes, engenharia de prompts e organização do conhecimento sobre um tema financeiro introdutório.

---

## 1. Contexto e Objetivos

### Por que esse tema?

Escolhi **reserva de emergência e organização financeira pessoal** porque é a base de qualquer planejamento financeiro saudável — e também porque é diretamente relevante para a minha realidade: estou em transição de carreira (saindo de uma trajetória focada em concursos de segurança pública para áreas como Judiciário, Ministério Público, Receita Federal e INSS), o que significa um período de renda mais instável. Entender como dimensionar e construir uma reserva de emergência é, na prática, parte do meu próprio planejamento neste momento.

### Objetivos de estudo

- [ ] Entender o conceito de reserva de emergência e por que ela é o primeiro passo da educação financeira;
- [ ] Aprender a calcular o tamanho ideal da reserva considerando perfil de renda (CLT vs. renda variável/autônomo);
- [ ] Identificar os critérios técnicos para escolher onde alocar a reserva (liquidez, segurança, rentabilidade);
- [ ] Compreender dados reais sobre o comportamento financeiro dos brasileiros em relação à poupança e ao endividamento;
- [ ] Construir um conjunto de prompts reutilizáveis para revisar este e outros temas financeiros no futuro.

---

## 2. Curadoria de Fontes

Foram selecionadas **5 fontes abertas**, priorizando órgãos oficiais e instituições reconhecidas, para garantir confiabilidade do conteúdo carregado no NotebookLM:

| # | Fonte | Tipo | Instituição | Link |
|---|-------|------|--------------|------|
| 1 | Caderno de Educação Financeira – Cidadania Financeira | PDF | Banco Central do Brasil (BCB) | [Acessar PDF](https://www.bcb.gov.br/content/cidadaniafinanceira/documentos_cidadania/Cuidando_do_seu_dinheiro_Gestao_de_Financas_Pessoais/caderno_cidadania_financeira.pdf) |
| 2 | Relatório de Letramento Financeiro | PDF | Banco Central do Brasil (BCB) | [Acessar PDF](https://www.bcb.gov.br/content/cidadaniafinanceira/documentos_cidadania/letramento/relatorio-de-letramento-financeiro.pdf) |
| 3 | Guia da Reserva de Emergência | E-book / Texto web | FEBRABAN (Meu Bolso em Dia) | [Acessar](https://meubolsoemdia.com.br/ebooks/guia-da-reserva-de-emergencia) |
| 4 | Reserva de emergência: passos para começar | Artigo web | Serasa Educação Financeira | [Acessar](https://www.serasa.com.br/blog/reserva-de-emergencia/) |
| 5 | Reserva de emergência como instrumento de proteção financeira pessoal: uma análise do cenário brasileiro | Artigo científico (PDF) | Revista Aposta — Ciencias Sociales | [Acessar](https://www.researchgate.net/publication/404140782_Reserva_de_emergencia_como_instrumento_de_protecao_financeira_pessoal_uma_analise_do_cenario_brasileiro) |

**Critério de seleção:** combinei fontes institucionais (BCB, FEBRABAN) — que garantem precisão técnica e estão alinhadas à Estratégia Nacional de Educação Financeira (ENEF) — com uma fonte jornalística/educativa (Serasa) para linguagem mais acessível, e um artigo acadêmico para trazer dados estatísticos e profundidade analítica. Essa combinação permitiu ao NotebookLM cruzar definições oficiais com dados empíricos sobre o comportamento financeiro real da população brasileira.

> 💡 Todas as fontes foram carregadas no NotebookLM como fontes de texto/PDF antes do início dos testes de prompt.

---

## 3. Engenharia de Prompts e "Cicatrizes" (Troubleshooting)

Abaixo estão as perguntas estratégicas elaboradas, as variações de prompt testadas, um resumo das respostas obtidas (com base nas fontes carregadas) e as dificuldades encontradas no processo.

### 🔍 Pergunta estratégica 1: "O que é reserva de emergência e qual sua função?"

**Prompt v1 (muito genérico):**
> "O que é reserva de emergência?"

- **Resultado:** resposta correta, mas superficial — repetiu definição de dicionário sem citar as fontes específicas carregadas.
- **Dificuldade:** prompt curto demais não força o modelo a cruzar as fontes nem a citar de onde tirou cada informação.

**Prompt v2 (refinado, pedindo citação):**
> "Com base exclusivamente nas fontes carregadas, defina o que é reserva de emergência e cite qual fonte traz essa definição."

- **Resultado:** resposta mais precisa, citando a definição do Guia FEBRABAN e complementando com a perspectiva do artigo acadêmico (poupança preventiva contra choques financeiros).
- **Aprendizado:** pedir explicitamente "com base nas fontes" e solicitar citação reduz alucinação e força o NotebookLM a ancorar a resposta no material carregado — essa é a principal "cicatriz" deste exercício.

---

### 🔍 Pergunta estratégica 2: "Quanto devo guardar de reserva de emergência?"

**Prompt v1:**
> "Quanto dinheiro eu preciso ter de reserva de emergência?"

- **Resultado:** resposta genérica de "6 meses de despesas", sem diferenciar perfil de renda.
- **Dificuldade:** a pergunta não especificou perfil profissional, então o modelo assumiu o caso médio (CLT).

**Prompt v2 (com contexto pessoal):**
> "Considerando alguém com renda variável ou em transição de carreira (não CLT), qual o intervalo de meses recomendado pelas fontes para a reserva de emergência, e por quê?"

- **Resultado:** resposta significativammente melhor — destacou que autônomos e pessoas com renda irregular devem buscar coberturas maiores (até 12 meses), conforme indicado nas fontes sobre fluxo de renda irregular.
- **Aprendizado:** personalizar o prompt com o próprio contexto de vida (renda variável, transição de carreira) trouxe uma resposta muito mais aplicável do que perguntar de forma abstrata.

---

### 🔍 Pergunta estratégica 3: "Onde investir a reserva de emergência?"

**Prompt v1:**
> "Onde devo investir minha reserva de emergência?"

- **Resultado:** resposta correta (Tesouro Selic, CDB com liquidez diária), mas sem explicar o *porquê* de cada critério.
- **Dificuldade:** resposta ficou em formato de lista solta, sem amarrar os três critérios técnicos (rentabilidade, segurança, liquidez).

**Prompt v2 (pedindo estrutura por critério):**
> "Segundo as fontes, quais são os três critérios técnicos para escolher onde alocar a reserva de emergência (liquidez, segurança, rentabilidade)? Explique cada um e dê um exemplo de investimento que atende aos três."

- **Resultado:** resposta estruturada por critério, com exemplo prático (Tesouro Selic) e explicação de cada conceito.
- **Aprendizado:** pedir uma estrutura específica (3 critérios + explicação + exemplo) no próprio prompt é mais eficaz do que esperar que o modelo organize sozinho — o NotebookLM responde melhor a perguntas com "andaime" (scaffolding) explícito.

---

### 🔍 Pergunta estratégica 4: "Qual o cenário real dos brasileiros em relação à reserva de emergência?"

**Prompt v1:**
> "Os brasileiros têm reserva de emergência?"

- **Resultado:** resposta vaga, sem números.
- **Dificuldade:** pergunta binária (sim/não) não estimula o modelo a buscar dados quantitativos nas fontes.

**Prompt v2 (pedindo dados):**
> "Quais dados estatísticos as fontes apresentam sobre o percentual de brasileiros que possuem (ou não) reserva de emergência? Cite as fontes de cada dado."

- **Resultado:** resposta rica em dados — trouxe que apenas uma minoria da população possui reserva adequada e uma parcela significativa relata alto estresse financeiro, citando os estudos de onde vieram esses números.
- **Aprendizado:** pedir dados quantitativos explicitamente é essencial quando o objetivo é extrair estatísticas de fontes mistas (institucionais + acadêmicas) — sem isso, o modelo tende a responder de forma qualitativa apenas.

---

### 📌 Principais "cicatrizes" (lições gerais de troubleshooting)

1. **Prompts vagos geram respostas vagas.** Perguntas genéricas do tipo "o que é X" tendem a gerar respostas de conhecimento geral do modelo, não necessariamente ancoradas nas fontes carregadas.
2. **Pedir citação da fonte reduz alucinação.** Adicionar "cite a fonte" ou "com base exclusivamente nas fontes carregadas" foi a mudança que mais impactou a qualidade e a verificabilidade das respostas.
3. **Contextualizar com a própria realidade gera respostas aplicáveis.** Inserir o próprio cenário (renda variável, transição de carreira) no prompt tornou as respostas práticas, não apenas teóricas.
4. **Dar "andaime" estrutural ao prompt (pedir 3 critérios, listar categorias) melhora a organização da resposta** — o NotebookLM responde melhor quando a estrutura desejada já está sugerida na pergunta.
5. **Perguntas binárias (sim/não) extraem menos valor do que perguntas que pedem dados ou comparações.**

---

## 4. Miniguia de Estudo (Entrega Final)

### 4.1 Resumo Estruturado

**O que é reserva de emergência?**
É uma quantia de dinheiro guardada com o objetivo específico de cobrir despesas inesperadas — perda de emprego, problemas de saúde, reparos urgentes — sem a necessidade de recorrer a dívidas ou comprometer o orçamento mensal. Funciona como uma "poupança preventiva" contra choques financeiros.

**Quanto guardar?**
A recomendação geral das fontes varia entre **3 a 6 meses** de despesas essenciais para quem tem renda fixa e estável (CLT), podendo se estender para **6 a 12 meses ou mais** para autônomos, freelancers ou pessoas em transição de carreira — justamente por terem fluxo de renda mais irregular.

**Cálculo prático:**
1. Liste todas as despesas fixas essenciais (moradia, alimentação, transporte, saúde);
2. Some o total mensal;
3. Multiplique por 6 (ou mais, conforme seu perfil de risco/renda);
4. Esse é o valor-alvo da sua reserva.

> Exemplo: despesas mensais de R$ 3.000 → reserva-alvo entre R$ 18.000 (6 meses) e R$ 36.000 (12 meses).

**Onde guardar a reserva?**
Três critérios técnicos devem ser observados simultaneamente:
- **Liquidez:** o dinheiro precisa estar disponível para resgate rápido (idealmente D+0 ou D+1);
- **Segurança:** baixo risco de perda do valor principal (evitar investimentos voláteis);
- **Rentabilidade:** ainda que moderada, deve ao menos superar a inflação (evitar deixar parado sem rendimento).

Exemplos que atendem aos três critérios: **Tesouro Selic**, CDBs com liquidez diária de bancos sólidos, ou fundos DI de baixa taxa de administração.

**Panorama brasileiro:**
Pesquisas recentes indicam que uma parcela relevante da população brasileira não possui reserva de emergência adequada, e grande parte relata ter enfrentado algum imprevisto financeiro no último ano — o que reforça a importância prática (e não apenas teórica) desse hábito.

---

### 4.2 Glossário de Conceitos

| Termo | Definição |
|-------|-----------|
| **Reserva de emergência** | Valor guardado especificamente para cobrir imprevistos financeiros, sem gerar endividamento. |
| **Liquidez** | Velocidade/facilidade com que um investimento pode ser convertido em dinheiro disponível. |
| **Renda fixa** | Categoria de investimento em que a remuneração segue regras predefinidas (taxa fixa, ou indexada a um índice). |
| **Tesouro Selic** | Título público pós-fixado, atrelado à taxa Selic, com alta liquidez — frequentemente recomendado para reserva de emergência. |
| **CDB (Certificado de Depósito Bancário)** | Título de renda fixa emitido por bancos; quando possui liquidez diária, pode ser usado para reserva. |
| **FGC (Fundo Garantidor de Créditos)** | Mecanismo que garante o reembolso de valores até um limite por CPF/instituição em caso de problemas no banco emissor. |
| **Letramento financeiro** | Combinação de conhecimento, habilidades e atitudes necessárias para tomar boas decisões financeiras (conceito da OCDE/INFE). |
| **Renda variável (perfil de risco)** | Perfil de quem não possui renda mensal fixa e previsível (autônomos, freelancers, profissionais em transição), exigindo reservas maiores. |
| **Inadimplência** | Situação de não cumprimento de uma obrigação financeira no prazo (atraso ou não pagamento de dívidas). |
| **Marcação a mercado** | Atualização diária do valor de um título conforme as condições de mercado, podendo gerar oscilações no preço de resgate antecipado. |

---

### 4.3 Prompts Reutilizáveis para Revisão Futura

Conjunto de prompts testados e validados, organizados por finalidade, para reutilizar em futuras sessões de estudo no NotebookLM (com este ou outros temas financeiros):

**Para extrair definições com precisão:**
```
Com base exclusivamente nas fontes carregadas, defina [CONCEITO] e indique qual fonte apresenta essa definição.
```

**Para personalizar a resposta ao seu contexto:**
```
Considerando uma pessoa com [PERFIL: renda variável / CLT / autônomo / em transição de carreira],
o que as fontes recomendam sobre [TEMA]? Justifique a recomendação.
```

**Para obter respostas estruturadas (scaffolding):**
```
Segundo as fontes, quais são os [N] critérios/fatores principais sobre [TEMA]?
Explique cada um separadamente e dê um exemplo prático.
```

**Para extrair dados estatísticos:**
```
Quais dados estatísticos as fontes apresentam sobre [TEMA]?
Cite a fonte de cada dado mencionado.
```

**Para gerar resumo de revisão rápida (antes de uma prova/entrevista):**
```
Resuma em até 5 bullet points os pontos mais importantes sobre [TEMA] segundo as fontes,
priorizando o que seria mais cobrado em uma avaliação ou entrevista.
```

**Para identificar contradições ou divergências entre fontes:**
```
Existe alguma divergência ou diferença de recomendação entre as fontes carregadas sobre [TEMA]?
Se sim, explique cada posição e de qual fonte ela vem.
```

---

## 5. Ferramentas Utilizadas

- **NotebookLM** (Google) — curadoria de fontes e testes de prompt;
- **Claude (Anthropic)** — apoio na pesquisa de fontes abertas, estruturação do miniguia, glossário e documentação deste README.

---

## 📎 Como reproduzir este estudo

1. Acesse o [NotebookLM](https://notebooklm.google.com/);
2. Crie um novo notebook e faça upload das 5 fontes listadas na seção 2;
3. Use os prompts da seção 4.3 como ponto de partida para suas próprias perguntas;
4. Compare suas respostas com o resumo da seção 4.1 para validar o entendimento.
5. https://notebooklm.google.com/notebook/94e15cc0-8acd-44bc-854d-32a88216ed4e
---

*Projeto desenvolvido como parte do desafio de projeto da [DIO](https://www.dio.me/) — uso de IA generativa para aprendizagem ativa.*
