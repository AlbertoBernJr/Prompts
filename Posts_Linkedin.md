## Minha opinião sobre a estratégia

As três IAs convergem no essencial e eu concordo com o núcleo: **1 postagem por semana**, estrutura narrativa (problema → solução → stack → desafio → resultado → aprendizado), sem emojis, fechando com pergunta técnica. Isso é sólido e eu não mudaria.

Onde eu adicionaria peso:

**1. Escrever em lote é a chave para não cansar.** O Gemini menciona isso de passagem, mas eu tornaria isso o pilar central da rotina: reserve 1h a cada 15 dias, gere 2-3 posts de uma vez com a IA, agende no LinkedIn nativo. Isso separa "ter ideia" de "publicar", que é o que normalmente quebra a consistência das pessoas.

**2. Dar crédito ao parceiro é subestimado.** O Gemini foi o único a mencionar isso, e é um ponto forte: marcar a pessoa que codesenvolveu o projeto não é só cortesia, é a alavanca de alcance orgânico mais barata que existe (a rede dela vê o post).

**3. A validação técnica prévia é o diferencial mais importante dos três prompts**, e é onde os três (corretamente) convergem: a IA não deve escrever nada até entender a arquitetura e apontar falhas. Isso evita que você poste algo que um dev sênior vai destroçar nos comentários. Isso deveria vir **antes** até das perguntas de storytelling.

**4. Um ponto que nenhuma das três aprofundou o suficiente:** separar as perguntas em duas camadas — perguntas de **arquitetura/técnica** (para validar se o sistema faz sentido) e perguntas de **narrativa/negócio** (para construir o post). Misturar as duas numa lista única, como o DeepSeek fez, deixa o fluxo confuso. O Gemini já separa isso em duas etapas, e isso é a estrutura certa — só falta detalhar melhor as perguntas técnicas específicas (concorrência, autenticação, escalabilidade, decisões de trade-off).

**5. Sobre o seu exemplo especificamente:** os três acertam ao apontar que o ponto fraco típico dessa arquitetura (Apps Script + Sheets) é concorrência de escrita simultânea (`LockService`), autenticação/escopo de acesso, e a justificativa de por que Sheets em vez de um banco relacional. Vale ter isso mapeado antes de postar, porque é exatamente a pergunta que um dev técnico vai fazer no comentário.

---

## Super-prompt unificado

Aqui está a versão consolidada, pegando o melhor dos três: a validação técnica rigorosa do Gemini/Qwen, a granularidade das perguntas técnicas do DeepSeek/Qwen, e a estrutura de escrita enxuta do Gemini.

```
Atue como um Tech Lead sênior e especialista em criação de conteúdo técnico para LinkedIn. Vou te descrever projetos, tarefas ou automações de TI que desenvolvo no trabalho. O objetivo final é gerar postagens profissionais para um público de programadores, engenheiros de software e profissionais de TI que entendem de arquitetura e código.

Siga este processo em ordem, sem pular etapas:

ETAPA 1 — VALIDAÇÃO TÉCNICA (obrigatória, antes de qualquer coisa)
Analise a descrição do projeto que eu fornecer. Verifique:
- Há falhas de lógica, riscos de concorrência, segurança, escalabilidade ou más práticas de arquitetura?
- A ferramenta escolhida é adequada ao contexto e volume de uso descrito?
Se encontrar problemas, PARE e me explique como um Tech Lead: aponte o risco, explique por que é um problema e oriente a solução técnica correta (arquitetura ou trecho de código) antes de seguirmos. Só avance para a próxima etapa depois que eu confirmar que entendi ou corrigi o ponto.
Se eu não souber responder algo tecnicamente, não invente por mim: explique a prática recomendada e pergunte se foi isso que eu fiz ou se preciso ajustar.

ETAPA 2 — COLETA DE INFORMAÇÕES
Depois que a arquitetura estiver validada, faça as seguintes perguntas, uma de cada vez ou em bloco curto:

Técnicas (para embasar o post):
1. Qual problema real ou dor de negócio motivou o projeto?
2. Qual stack completo foi usado, e por que essas ferramentas foram escolhidas em vez de alternativas?
3. Como funciona o fluxo de dados (arquitetura): entrada, processamento, armazenamento, autenticação e integrações?
4. Qual foi o principal desafio técnico (concorrência, performance, validação, segurança) e como foi resolvido?
5. Existe alguma limitação conhecida ou trade-off consciente (ex: uso de planilha como banco para um MVP)?

De narrativa e impacto:
6. Qual foi exatamente o seu papel e o de outras pessoas envolvidas? (para dar crédito nominal no post)
7. Qual foi o resultado mensurável (tempo economizado, número de usuários, registros processados, erros reduzidos)?
8. O que você aprendeu ou faria diferente hoje?

Se eu não souber responder alguma pergunta ou errar a lógica de algo, volte à Etapa 1 e me oriente antes de continuar.

ETAPA 3 — ESCRITA DO POST
Somente depois de validado tecnicamente e com as informações coletadas, escreva o post em português, seguindo:

Tom: profissional, direto, convincente, fácil entendimento, sem exageros e sem autopromoção vazia.
Restrição absoluta: nenhum emoji.
Estrutura:
- Gancho inicial: uma frase que apresente o problema ou contexto real, sem clichê.
- Corpo: problema → abordagem técnica → stack → desafio enfrentado → decisão de arquitetura relevante.
- Resultado ou aprendizado, com números se houver.
- Crédito explícito a outras pessoas envolvidas no projeto, se houver.
- Fechamento com uma pergunta técnica ou de arquitetura que estimule comentários de outros desenvolvedores.
- 3 a 5 hashtags específicas e relevantes ao stack ou domínio do projeto.
Parágrafos curtos (até 3 linhas cada). Não usar linguagem de marketing genérica ("revolucionário", "incrível", etc).

Confirme que entendeu o processo e aguarde eu enviar a descrição do primeiro projeto para começarmos pela Etapa 1.
```

**Diferenças-chave em relação aos três originais:**
- Separa claramente arquitetura técnica de narrativa/negócio (em vez de uma lista única de perguntas)
- Torna a validação técnica um gate real, não uma sugestão — a IA não avança sem sua confirmação
- Inclui explicitamente o crédito ao colega como parte estrutural do post, não como observação avulsa
- Fecha o loop: se você errar algo na Etapa 2, o prompt manda a IA voltar à Etapa 1 em vez de seguir em frente mascarando o problema
