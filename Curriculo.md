# Prompt Mestre — Otimização de Currículo para ATS
**Versão 3.0 — Consolidada e Corrigida**

> Combina o melhor do Gemini v1 e DeepSeek v2, com correções de vulnerabilidades críticas
> e adição de diretrizes técnicas ausentes em ambas as versões anteriores.

---

## Como Usar

1. Copie tudo a partir da linha `=== INÍCIO DO PROMPT ===`
2. Cole em qualquer LLM (Claude, ChatGPT, Gemini, DeepSeek)
3. Preencha os campos da **PARTE 4 — DADOS DE ENTRADA**
4. Revise o currículo gerado antes de formatar no Word ou Google Docs
5. Converta para PDF usando "Salvar como PDF" do próprio editor — nunca impressora de terceiros
6. Valide com as ferramentas abaixo antes de enviar a candidatura

---

## Ferramentas Gratuitas de Validação ATS (2026)

Validar **após** receber o currículo reescrito e **antes** de enviar a candidatura.

| Ferramenta | URL | Plano gratuito | Melhor para |
|---|---|---|---|
| **Jobscan** | jobscan.co | 5 análises/mês | Score ATS vs. vaga específica — referência do mercado |
| **KudosWall ATS Checker** | pro.kudoswall.com/resume-analyzer | Ilimitado, sem cadastro | Pontuação rápida (0-100), sem barreiras |
| **Enhancv** | enhancv.com | Ilimitado | ATS + legibilidade para recrutador humano |
| **Resume Worded** | resumeworded.com | Limitado | Feedback contextual linha a linha |
| **Novorésumé** | novoresume.com/tools/ats-resume-checker | Gratuito | Diagnóstico rápido de formatação e keywords |

> **Estratégia de uso recomendada:**
> - Use o **KudosWall** para testes rápidos a cada iteração (sem limite).
> - Use o **Jobscan** como validação final antes de enviar (mais preciso, porém limitado).
> - Score abaixo de 75? Revise o Resumo Profissional e a seção de Habilidades com base no feedback gerado.

---

## O Que Foi Corrigido Nesta Versão

| Problema identificado | Onde existia | Correção aplicada |
|---|---|---|
| Seção "Palavras-chave Técnicas" no rodapé | DeepSeek v2 | **Removida.** ATS modernos detectam como keyword stuffing e podem penalizar |
| Formato de arquivo não especificado | Ambos | DOCX como padrão, com instrução de conversão para PDF |
| Contato em Header/Footer do editor | Ambos | Instrução explícita: tudo no corpo do documento |
| Layout de múltiplas colunas não proibido | Ambos | Coluna única obrigatória |
| Nomes de seção sem padrão definido | Ambos | Padrão PT (EN) estabelecido com lista exata |
| Datas sem formato consistente | Ambos | MM/AAAA obrigatório em todo o documento |
| Caracteres especiais sem definição clara | Ambos | Lista de permitidos e proibidos |
| Nenhuma ferramenta de validação sugerida | Ambos | 5 ferramentas gratuitas indicadas com estratégia de uso |

---
---

=== INÍCIO DO PROMPT ===

## PAPEL E OBJETIVO

Aja como um Recrutador Sênior de Alta Performance e Arquiteto de Currículos para ATS,
especializado em criar documentos que alcancem ranqueamento máximo em sistemas como
Greenhouse, Workday, Lever, Taleo e iCIMS, e que sejam simultaneamente persuasivos e
convincentes para recrutadores humanos.

Sua missão: reescrever meu currículo para a vaga fornecida, transformando-o no currículo
do candidato ideal — máxima pontuação no ATS e alta atratividade para o avaliador humano.

Execute cada instrução na ordem apresentada, sem omitir nenhuma etapa.

---

## PARTE 1 — BLINDAGEM TÉCNICA DO FORMATO

> Esta é a etapa mais crítica. Falhas de formato podem zerar a pontuação ATS
> independentemente da qualidade do conteúdo. Execute antes de escrever qualquer palavra.

### 1.1 Formato e Layout

- Formato do arquivo: `.DOCX`
- Conversão para PDF: usar exclusivamente "Salvar como PDF" ou "Exportar para PDF" do
  próprio editor (Word ou Google Docs). Impressoras PDF de terceiros geram arquivos
  baseados em imagem que o ATS não consegue ler.
- **Layout de coluna única — obrigatório, sem exceções**
- Proibido: colunas múltiplas, tabelas, caixas de texto, bordas decorativas, imagens,
  gráficos, ícones, barras de progresso de habilidades
- Fontes permitidas: Arial, Calibri ou Helvetica
  - Nome do candidato: 14pt a 16pt, negrito
  - Títulos de seção: 12pt, negrito
  - Corpo do texto: 10pt a 11pt
- Margens: 1,5 cm a 2,0 cm em todos os lados
- Espaçamento entre linhas: 1,15 a 1,5

### 1.2 Regras de Caracteres

**Proibidos — causam falha no parser ATS:**
- Travessão decorativo (—) — substituir por hífen simples (-)
- Aspas curvas ou inteligentes (" " ' ') — substituir por aspas retas ("")
- Setas (-> ou →)
- Símbolos gráficos (checkmark, estrela, quadrado preenchido, etc.)
- Emojis de qualquer tipo
- Qualquer ícone ou símbolo não-ASCII

**Permitidos:**
- Hífen simples (-)
- Ponto (.), vírgula (,), parênteses (), barra (/), asterisco (*)
- Bullet padrão (•) — usar um único estilo em todo o documento

**Acentuação portuguesa (ã, ç, é, ê, á, â, etc.): OBRIGATÓRIA.**
São caracteres UTF-8 padrão, reconhecidos por todos os ATS modernos.
A restrição acima refere-se exclusivamente a símbolos decorativos não-texto.

### 1.3 Informações de Contato

**Regra crítica:** nunca colocar dados de contato em Header ou Footer do editor de texto.
Esses campos são invisíveis para a maioria dos parsers ATS.

Todo o conteúdo deve estar no corpo principal do documento, logo abaixo do nome.

Formato do bloco de contato:

```
[Nome Completo — 14pt a 16pt, negrito]
[Cidade, Estado] - [+55 (XX) XXXXX-XXXX] - [email@dominio.com]
[linkedin.com/in/seuperfil] - [github.com/seuperfil] - [portfolio.com] (se aplicável)
```

- URLs em texto simples, sem hiperlink colorido ou sublinhado
- Não incluir: foto, CPF, RG, data de nascimento, estado civil

### 1.4 Formato de Datas

- **Padrão obrigatório em todo o documento:** MM/AAAA
- Correto: `03/2021 - 08/2024` | `01/2023 - Presente`
- Proibido: `Jan/2021`, `Janeiro de 2021`, `2021-2024`, `2021 a 2024`
- Consistência absoluta em todas as seções do documento

### 1.5 Nomenclatura das Seções

**Padrão:** nome em português seguido da tradução em inglês entre parênteses.
Isso maximiza a compatibilidade com ATS configurados em qualquer idioma.

Usar exatamente estes cabeçalhos:

```
Resumo Profissional (Professional Summary)
Habilidades Técnicas (Technical Skills)
Experiência Profissional (Professional Experience)
Formação Acadêmica (Education)
Certificações e Cursos (Certifications)
Idiomas (Languages)
```

Não criar seções com nomes criativos ou personalizados fora deste padrão.
A seção de contato fica no topo sem título de seção.

---

## PARTE 2 — LÓGICA DE PONTUAÇÃO ATS

**Princípio central:** qualidade de contexto supera quantidade de repetição.

**Técnica LSI — Indexação Semântica Latente (obrigatória):**
Para cada palavra-chave principal da vaga, inclua ao redor dela termos relacionados:
ferramentas, conceitos e tecnologias complementares. Isso cria uma rede semântica que
simula domínio real do assunto sem repetição mecânica do mesmo termo.

> Exemplo: a palavra-chave principal "Kubernetes" gera o contexto LSI:
> orquestração de containers, Docker, pods, Helm, cluster management,
> deploys automatizados, rolling updates, CI/CD.

**PROIBIDO: keyword stuffing.**
ATS modernos detectam e penalizam densidade artificial de palavras-chave.
Um termo bem contextualizado vale mais do que o mesmo termo repetido 10 vezes.

---

### Zona de Máximo Impacto — Peso 3x
**Seções afetadas: Título do Currículo + Resumo Profissional**

**Título (linha imediatamente abaixo do nome):**
- Deve ser EXATAMENTE o título da vaga, sem modificações ou variações

**Resumo Profissional:**
- Extensão: 4 a 5 linhas — 1 parágrafo narrativo coeso (sem bullets)
- A primeira frase deve conter: título da vaga + anos de experiência compatíveis com o
  solicitado + principal requisito técnico da vaga
- Exemplo: "Engenheiro de Dados Sênior com 6+ anos de experiência em pipelines de
  dados em larga escala e arquitetura em nuvem..."
- Deve incluir: principais palavras-chave da vaga, soft skills mais exigidas e ao menos
  2 termos LSI do requisito técnico principal
- Tom: profissional, narrativo e confiante. Não é uma lista, é um parágrafo fluido.

---

### Zona de Alto Impacto — Peso 2x
**Seção afetada: Cabeçalho de cada cargo**

Estrutura padrão de cada cargo:

```
[Nome da Empresa, negrito] | [Cidade, Estado]
[Título do Cargo, negrito] | [MM/AAAA - MM/AAAA]
[Micro-frase de impacto — 1 linha, negrito, 2 a 3 palavras-chave de alto peso]
```

A micro-frase deve ser factual, em negrito, e conter as ferramentas ou metodologias
mais críticas para a vaga.

Exemplos de micro-frases corretas:

> **Liderança técnica na migração de arquitetura monolítica para microsserviços em AWS,
> com redução de 37% nos custos operacionais mensais.**

> **Desenvolvimento e manutenção de pipelines ETL em Apache Spark e BigQuery,
> processando 15 TB de dados por dia para dashboards executivos.**

---

### Zona de Consolidação — Peso 1x
**Seções afetadas: Habilidades Técnicas + Detalhamento das Experiências**

**Habilidades Técnicas — grupos semânticos sugeridos:**
- Linguagens de Programação
- Frameworks e Bibliotecas
- Cloud e Infraestrutura
- Banco de Dados
- Ferramentas e Plataformas
- Metodologias e Processos
- Soft Skills (como habilidades concretas, ex: Mentoria Técnica, Gestão de
  Stakeholders, Resolução de Conflitos, Comunicação com Times Multidisciplinares)

Dentro de cada grupo, listar primeiro as habilidades exigidas pela vaga.
Usar sinônimos e variantes dos termos já usados no Resumo para enriquecer o
vocabulário semântico sem repetição de palavras exatas.

**Detalhamento das Experiências (bullets):**
Usar variações e sinônimos dos termos das zonas 3x e 2x para enriquecer o contexto
semântico — nunca repetir as mesmas palavras exatas das seções anteriores.

---

## PARTE 3 — REGRAS DE CONSTRUÇÃO DO CONTEÚDO

### 3.1 Estrutura e Ordem do Documento

Seguir esta ordem obrigatória, sem exceções:

1. Nome e dados de contato (sem título de seção)
2. Resumo Profissional (Professional Summary)
3. Habilidades Técnicas (Technical Skills)
4. Experiência Profissional (Professional Experience)
5. Formação Acadêmica (Education)
6. Certificações e Cursos (Certifications) — incluir apenas se houver
7. Idiomas (Languages)

### 3.2 Seção de Experiência Profissional

**Formato padrão de cada cargo:**

```
[Nome da Empresa, negrito] | [Cidade, Estado]
[Título do Cargo, negrito] | [MM/AAAA - MM/AAAA]
[Micro-frase de impacto, negrito — Peso 2x]
- Bullet 1: responsabilidade ou conquista com contexto + ação + resultado
- Bullet 2
- Bullet 3
- Bullet 4
- Bullet 5 (máximo 6 bullets por cargo)
```

**Verbos de ação por nível de senioridade:**

| Nível | Verbos indicados |
|---|---|
| Estágio / Trainee | apoiei, colaborei, auxiliei, participei, desenvolvi |
| Júnior | implementei, desenvolvi, criei, configurei, resolvi, apoiei |
| Pleno | liderei, otimizei, gerenciei, entregei, coordenei, reduzi, automatizei |
| Sênior | arquitetei, defini, estruturei, concebi, escalei, estabeleci, conduzi |

- Cargos anteriores: verbos no passado
- Cargo atual: verbos no presente
- **Limite total do documento: máximo 2 páginas**

### 3.3 Mecanismo Anti-Inflação — Fórmula C.A.R. + I

Toda conquista com métrica numérica deve seguir esta estrutura antes de ser incluída:

- **C — Contexto:** Qual era a situação ou o problema que existia?
- **A — Ação:** O que você fez especificamente para resolver?
- **R — Resultado:** Qual foi o número ou a entrega mensurável?
- **I — Impacto:** O que esse resultado representou para o negócio ou para a equipe?

**Exemplo incorreto (inválido — genérico e inverossímil):**
> "Reduzi custos de infraestrutura em 40%."

**Exemplo correto (válido — C.A.R. + I aplicado):**
> "Após auditoria em instâncias ociosas do EC2, implementei políticas de escalabilidade
> automática e migração para instâncias spot, reduzindo custos mensais de infraestrutura
> em 37% em um ambiente de 200+ servidores, representando economia de R$ 28.000/mês."

**Regra de verossimilhança obrigatória:**
Métricas devem ser compatíveis com o nível do cargo e com o contexto real descrito.
Números inverossímeis destroem a credibilidade com recrutadores humanos.
Se não houver uma métrica precisa disponível, use estimativas realistas com qualificador:
"aproximadamente", "cerca de", "em média" — nunca invente números precisos sem base.

### 3.4 Regras Gerais de Texto

- Não usar primeira pessoa (eu, meu, minha, nosso)
- Não iniciar bullets com artigos (o, a, um, uma, os, as)
- Todo bullet deve iniciar com verbo de ação
- Usar o mesmo tempo verbal dentro de cada cargo
- Cada frase deve ter uma intenção clara: ranquear no ATS ou provar valor para o recrutador
- Não incluir referências profissionais no currículo
- Não incluir informações pessoais além do bloco de contato

---

## PARTE 4 — DADOS DE ENTRADA

> Preencha todos os campos abaixo com as informações reais antes de enviar o prompt.
> Quanto mais completo for o preenchimento, mais preciso e eficaz será o resultado.

---

**[Nome Exato da Vaga]:**

(Escreva aqui o título da vaga exatamente como aparece no anúncio)

---

**[Descrição Completa da Vaga]:**

(Cole aqui a descrição completa, incluindo: sobre a empresa, responsabilidades,
requisitos obrigatórios, requisitos desejáveis e qualquer outra informação do anúncio)

---

**[Meu Currículo e Experiências Atuais]:**

(Cole aqui seu currículo atual completo: todos os cargos, datas, responsabilidades,
projetos relevantes, formações acadêmicas e certificações)

---

**[Informações Complementares — opcional]:**

(Projetos pessoais, contribuições open source, cursos em andamento,
conquistas relevantes não documentadas no currículo atual)

---

=== FIM DO PROMPT ===
