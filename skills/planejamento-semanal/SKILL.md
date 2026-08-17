---
name: planejamento-semanal
description: Roda o planejamento semanal de conteúdo do LinkedIn de ponta a ponta: analisa o desempenho dos posts publicados, sugere temas novos com base nos dados, escreve os posts aprovados e agenda no agendador nativo do LinkedIn. Acione quando o usuário disser "planejamento da semana", "monta os posts da semana", "o que eu posto essa semana", "me dá ideias de post", "bora fazer o conteúdo", ou quando uma tarefa agendada semanal de conteúdo disparar.
---

# Planejamento semanal

Rotina completa de uma semana de conteúdo. Nunca pular o Passo 0: sugerir tema sem olhar dado é chutar.

## Pré-requisitos

Ler `perfil.md`, `banco-de-casos.md` e `aprendizados-publico.md` na pasta de trabalho. Se `perfil.md` não existir, acionar `configurar-perfil` primeiro e voltar.

## Passo 0: análise de desempenho (obrigatório)

Acionar a skill `leitura-de-metricas` para puxar os números dos posts da última semana e LER OS COMENTÁRIOS recebidos.

Os comentários são a parte mais valiosa e a mais ignorada. Eles entregam tema novo, objeção, vocabulário do público e, com frequência, o gancho do próximo post pronto. Quando alguém sênior discorda com densidade, aquilo é ouro: significa que o tema tem território disputado.

Registrar a leitura em `aprendizados-publico.md`: números crus, diagnóstico do que funcionou e do que não, e o que isso muda na curadoria.

## Passo 1: checar repetição

Conferir os assuntos e os casos usados nas últimas 4 semanas. Não repetir caso dentro dessa janela. Consultar o campo "última vez usado" em `banco-de-casos.md`.

## Passo 2: sugerir 6 temas

Entregar 6 sugestões, cada uma com:
- título curto
- ângulo em uma linha
- tipo (técnico, bastidores, aprendizado prático, opinião estratégica, resultado)
- formato recomendado
- qual caso do banco entra como prova

Regras da curadoria:
- Variar os tipos. Não concentrar tudo no mesmo pilar.
- Dobrar a aposta no que os dados mostraram que funciona, sempre com ângulo novo, nunca repetindo literal.
- Priorizar tema que veio dos comentários do público, porque já tem demanda comprovada.
- Respeitar a seção "Do que NÃO falar" de `perfil.md`.
- Todos os temas precisam orbitar o posicionamento declarado. Tema fora do posicionamento não distribui, porque o algoritmo valida a coerência entre perfil e assunto antes de entregar.

**Entregar as 6 e PARAR.** O usuário escolhe. Não escrever antes da escolha.

## Passo 3: escrever os posts escolhidos

Para cada post escolhido, acionar a skill `metodo-de-gancho` e seguir o método dela. Gerar 2 ou 3 opções de gancho, abrir com a mais forte e justificar a escolha em uma linha.

Salvar cada post em `posts/AAAA-MM-DD-slug/legenda.txt` na pasta de trabalho.

## Passo 4: aprovação humana

Mostrar o texto final e a mídia, se houver, e ESPERAR aprovação explícita. Nunca agendar nem publicar sem o usuário dizer que está aprovado.

Se ele pedir ajuste no gancho, entender o que incomodou antes de reescrever. O padrão mais comum de rejeição é o gancho estar rebaixando o leitor sem que isso seja óbvio; nesse caso, inverter para promoção resolve.

## Passo 5: agendar

Abrir o compositor do LinkedIn com `~~navegador` e usar o agendador nativo (ícone de relógio), um post por dia fixo da cadência definida em `perfil.md`.

Notas operacionais que economizam tempo:
- O compositor roda em shadow DOM. Validar sempre por screenshot, nunca confiar em introspecção de DOM.
- Se o texto tem link, o LinkedIn cria um card de preview automático. **Esse card bloqueia upload de vídeo.** Remover o card antes de subir mídia; o link continua valendo no corpo do texto.
- Para subir mídia, o input de arquivo costuma estar oculto em shadow DOM e precisa ser revelado antes de receber o arquivo. Se o upload por automação falhar, pedir para o usuário subir a mídia manualmente em vez de insistir.
- Confirmar por screenshot que a data e a hora ficaram certas antes de fechar.

## Passo 6: registrar e fechar

Atualizar `aprendizados-publico.md` com a leva agendada, os ganchos escolhidos e qualquer experimento em curso. Atualizar o campo "última vez usado" dos casos que foram usados.

Se houver experimento rodando (mudança de dia, de horário, de formato), registrar explicitamente qual é a variável e o que se espera aprender. Mudar duas variáveis na mesma semana embaralha a leitura seguinte, então avisar o usuário quando isso acontecer.

Fechar as abas do navegador que esta rotina abriu.
