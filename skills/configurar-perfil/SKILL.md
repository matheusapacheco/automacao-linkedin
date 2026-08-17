---
name: configurar-perfil
description: Configura o plugin para o perfil, o nicho e os casos reais do usuário, criando os arquivos de memória que todas as outras skills leem. Acione na PRIMEIRA vez que qualquer skill deste plugin for usada e o arquivo perfil.md não existir. Também acione quando o usuário disser "configurar meu perfil", "atualizar meu posicionamento", "mudei de área", "quero trocar meus pilares de conteúdo", ou quando pedir para revisar quais casos ele pode usar como prova.
---

# Configurar perfil

Cria a base de contexto que o plugin inteiro consome. Sem ela, as outras skills não têm posicionamento, casos nem histórico para trabalhar, e vão produzir conteúdo genérico.

## Quando rodar

Rodar quando `perfil.md` não existir na raiz da pasta de trabalho, ou quando o usuário pedir para revisar o posicionamento. Antes de perguntar qualquer coisa, checar se os arquivos já existem e ler o que houver.

## Passo 1: coletar o contexto

Fazer as perguntas com AskUserQuestion, agrupadas, nunca uma a uma. O que precisa ser descoberto:

**Posicionamento (o mais importante)**
- Em que o usuário quer ser reconhecido como referência? Pedir uma resposta específica, não uma área ampla.
- Do que ele NÃO quer ser referência, mesmo sabendo fazer? Essa negativa vale tanto quanto a afirmativa, porque impede o conteúdo de derivar para o assunto errado.
- Qual é o cenário ou setor onde ele atua? (serve de contexto recorrente nas histórias)

**Público**
- Quem ele quer que leia? Cargo, senioridade, momento de carreira.
- O que esse público teme e o que deseja profissionalmente?
- Existe algum assunto proibido, tema sensível ou coisa que já deu problema antes?

**Provas disponíveis**
- Quais resultados reais ele pode citar, com número? Pedir de 4 a 8, cada um com contexto, o que foi feito e o número.
- Algum deles tem restrição de confidencialidade ou não pode ser nomeado?

**Restrições pessoais**
- Ele está empregado e quer evitar sinalizar busca de emprego? (muda a forma de contar histórias de automação e de portfólio)
- Existe assunto que não pode aparecer? (finanças pessoais, cliente sob NDA, etc.)

**Operação**
- Quantos posts por semana e em quais dias?
- Prefere escrever em qual idioma?

## Passo 2: escrever os arquivos de memória

Criar quatro arquivos na raiz da pasta de trabalho. Eles são o estado do plugin entre sessões.

**`perfil.md`** — posicionamento, público, restrições, cadência. Incluir uma seção "Do que NÃO falar" bem explícita, porque ela é consultada antes de cada sugestão de tema.

**`banco-de-casos.md`** — um bloco por caso, no formato: contexto, problema, decisão tomada, número do resultado, restrição de uso, e um campo "última vez usado" que começa vazio. Esse campo evita fadiga de caso, que é medida e real.

**`aprendizados-publico.md`** — criar com a estrutura pronta e vazia: log de desempenho, insights, temas para dobrar a aposta, o que otimizar, perfil do público. As outras skills preenchem semana a semana.

**`log-engajamento.md`** — criar vazio, com colunas de data, status, pessoa e post. É a memória de quem já foi contactado.

## Passo 3: calibrar o método

Explicar em poucas linhas que o plugin já vem com moldes de gancho validados em dados de outro perfil (ver a skill `metodo-de-gancho`), e que esses moldes são ponto de partida, não verdade absoluta. Depois de umas 3 semanas de dados próprios, o `aprendizados-publico.md` do usuário passa a valer mais que os exemplos que vieram no plugin.

Deixar isso claro evita que o usuário siga um molde que não funciona para o público dele.

## Passo 4: confirmar e encerrar

Mostrar um resumo do que foi gravado, apresentar os arquivos criados, e dizer qual é o próximo passo natural: rodar `planejamento-semanal` para a primeira leva de posts, ou `leitura-de-metricas` primeiro, se ele já publica há algum tempo e quer partir de dados reais.
