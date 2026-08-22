# Prompt Modelo — Documentação de Projeto (README / Portfólio HTML)

> **Como usar:** copie o bloco relevante (Versão 1 ou Versão 2), preencha os
> campos `[...]` com respostas curtas e diretas (não precisa escrever bonito,
> isso é trabalho da IA), e envie para o Claude (ou outra IA).

> **Premissas fixas em ambos os prompts:**
> - Público-alvo: pessoas **sem conhecimento técnico**. Linguagem simples, sem jargão, sem termos de programação sem explicação.
> - **Sem emojis** em nenhuma parte do texto gerado.
> - Objetividade máxima: frases curtas, direto ao ponto, sem repetição, sem floreio, sem "encher linguiça".

---

## Versão 1 — README.md completo (para o repositório do projeto)

### PROMPT (copie a partir daqui)

Aja como um redator técnico e escreva a documentação de um projeto para o meu
portfólio, seguindo esta estrutura: Título de impacto → Problema → Solução/Valor
→ Funcionalidades → Demonstração visual → Como funciona → Diferenciais →
Resultados → Tecnologias.

**Regras obrigatórias:**
- O leitor é uma pessoa **sem conhecimento técnico**. Explique tudo em linguagem simples, evite termos técnicos sem explicação, e se precisar usar um termo técnico, explique em poucas palavras entre parênteses.
- **Não use emojis** em nenhum lugar do texto.
- Seja **objetivo**: frases curtas, sem repetição de ideias, sem adjetivos vagos ("incrível", "poderoso", "revolucionário"), sem parágrafos de enchimento. Se uma informação pode ser dita em uma frase, não use três.
- Não invente informações, links, métricas ou funcionalidades que eu não tenha fornecido. Se um campo abaixo estiver vazio ou "não se aplica", simplesmente omita essa parte do texto — não crie um genérico no lugar.
- Use Markdown, com títulos e bullets, para facilitar a leitura.

Aqui estão as informações do projeto:

1. **Nome do projeto:** [ex: Criação Cartões Avaliação Nominal]

2. **Frase de impacto (opcional, ou deixo a IA criar):** [ex: automatiza a geração
   de cartões nominais, eliminando X horas de trabalho manual]

3. **Qual era o problema/cenário antes da ferramenta existir?**
   [descreva o processo manual, a dor, o tempo gasto, os erros que aconteciam]

4. **Quem sofria com esse problema (público-alvo dentro do meu contexto)?**
   [ex: professores, equipe de RH, eu mesmo no meu trabalho — mesmo sem saber programar]

5. **O que a ferramenta entrega de benefício concreto?**
   [ex: reduz de 4h para 15min; elimina erros de digitação; escala para 500 itens]

6. **Quais as 3 a 5 funcionalidades principais?** (liste, uma por linha)
   - [funcionalidade 1]
   - [funcionalidade 2]
   - [funcionalidade 3]

7. **Como funciona, em linhas gerais?**
   [explique o fluxo: entrada → processamento → saída, sem termos técnicos]

8. **Quais tecnologias/ferramentas foram usadas?**
   [ex: Python, Pandas, Excel, Pillow, Tkinter]

9. **Por que essa abordagem e não outra?** (opcional)
   [ex: escolhi X em vez de Y porque...]

10. **Tem métricas ou resultados?** (opcional — omita se não tiver)
    [ex: tempo antes x depois, quantidade de itens processados, taxa de erro]

11. **Links:**
    - Repositório/código: [cole a URL]
    - Vídeo de demonstração no YouTube: [cole a URL completa do vídeo]
    - Outro (planilha modelo, exemplo público): [cole a URL ou "não se aplica"]

12. **Alguma observação extra que eu queira destacar?**
    [qualquer coisa que não se encaixou acima, ou "não se aplica"]

**Formato de saída:** Markdown, pronto para colar em um README.md.

---

## Versão 2 — Card HTML do portfólio (GitHub Pages)

> Pensado especificamente para o formato de card compacto que você já usa
> (título + vídeo + descrição curta + tags + botões + rodapé) — não é um README,
> então o texto tem que ser bem mais enxuto.

### PROMPT (copie a partir daqui)

Aja como um redator técnico especializado em portfólios de projetos. Vou te dar
o template HTML que já uso no meu GitHub Pages e as informações de um novo
projeto. Quero que você gere **apenas o conteúdo das seções internas** (título,
subtítulo, descrição, tags e botões), mantendo exatamente a mesma estrutura de
classes CSS e o mesmo padrão de texto usado nos meus projetos anteriores.

**Regras obrigatórias:**
- O leitor é uma pessoa **sem conhecimento técnico**. Linguagem simples e direta, sem termos técnicos sem explicação.
- **Não use emojis** em nenhuma parte do conteúdo (título, descrição, tags, botões).
- Seja **objetivo**: no máximo 2 parágrafos curtos na descrição, mais uma lista de funcionalidades. Sem adjetivos vagos, sem floreio, sem repetir a mesma ideia de formas diferentes.
- Não invente links, métricas ou funcionalidades que eu não informei. Se um dado opcional não for fornecido, omita a frase — não crie um genérico no lugar.
- Extraia o ID do vídeo do link do YouTube que eu fornecer e monte o `src` do iframe já no formato de embed (`https://www.youtube.com/embed/ID_DO_VIDEO`), mesmo que eu cole o link no formato `youtube.com/watch?v=` ou `youtu.be/`.
- Preencha o `href` dos botões exatamente com os links que eu fornecer. Se eu não fornecer um link, não crie o botão correspondente.
- Gere o HTML pronto para eu colar direto no arquivo, já substituindo `<title>`, `<h1>`, `.subtitle`, o `src` do iframe, os parágrafos de `.description`, as `<span class="tag">` e o `href` dos botões.

### Dados do projeto:
- **Nome do projeto:** [ex: Criação Cartões Avaliação Nominal]
- **Frase de impacto (subtítulo, uma linha):** [ex: Sistema automatizado para geração de cartões de avaliação nominal]
- **Problema que existia antes:** [processo manual, tempo gasto, erros comuns — em linguagem simples]
- **Como a ferramenta resolve isso:** [ideia central da solução, em 1-2 frases, sem termos técnicos]
- **Funcionalidades principais (3 a 6, uma por linha):**
  - [funcionalidade 1]
  - [funcionalidade 2]
  - [funcionalidade 3]
- **Tecnologias usadas (para virar tags):** [ex: Python, Pandas, Excel, Pillow, Tkinter]
- **Resultados/métricas (opcional — omita se não tiver):** [ex: reduziu de 4h para 15min]
- **Link do repositório (para o botão "Ver código"):** [cole a URL]
- **Link do vídeo no YouTube:** [cole a URL completa — qualquer formato, ex: `youtube.com/watch?v=ID` ou `youtu.be/ID`]
- **Outro link opcional (planilha modelo, demo pública):** [cole a URL ou "não se aplica"]

### Template HTML atual (mantenha a mesma estrutura e classes):
[cole aqui o código HTML completo do seu template]

---

## Checklist antes de publicar (evitar erros comuns)

- [ ] O link do vídeo está no formato `/embed/` e não `/watch?v=` (o iframe não funciona com o link normal do YouTube).
- [ ] O `href` do botão "Ver código" aponta para a pasta/arquivo certo do repositório, não para a raiz do GitHub.
- [ ] Nenhum campo opcional que você deixou em branco virou uma frase genérica ou inventada no texto gerado — releia e remova qualquer coisa que pareça "preenchida" pela IA sem você ter informado.
- [ ] Não sobrou nenhum emoji no texto (título, descrição, tags, botões).
- [ ] O texto está compreensível para alguém sem conhecimento técnico — se um termo técnico aparecer, tem que estar explicado.
- [ ] A descrição não ficou longa demais para o espaço do card (teste visualmente antes de publicar).
- [ ] As tags de tecnologia batem com o que foi realmente usado no projeto.
