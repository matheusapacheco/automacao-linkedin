---
name: engajamento-diario
description: Monta a rotina diária de engajamento no LinkedIn: encontra pessoas certas para conectar e posts de terceiros para comentar com insight real, sempre parando para aprovação humana antes de enviar qualquer coisa. Acione quando o usuário disser "engajamento do dia", "quem eu conecto hoje", "acha posts pra eu comentar", "vamos subir meu SSI", "rotina diária do LinkedIn", ou quando uma tarefa agendada diária de engajamento disparar.
---

# Engajamento diário

Alimenta os pilares de "encontrar as pessoas certas" e "interagir com insights" do SSI. Essa rotina complementa os posts; sozinha ela não constrói autoridade, mas sem ela o alcance dos posts não sai da própria bolha.

## Gate humano, sem exceção

**Esta skill NUNCA envia convite nem publica comentário por conta própria.** Ela pesquisa, monta a lista, escreve os rascunhos e PARA, esperando aprovação explícita numa conversa.

Isso vale inclusive quando a skill é disparada por uma tarefa agendada. Nesse caso o resultado é um relatório, e a execução acontece depois, quando o usuário revisar. Não interpretar "roda a rotina diária" como autorização para enviar.

## Passo 1: ler a memória

Ler `log-engajamento.md` antes de qualquer busca. Ele guarda quem já foi contactado e em quais posts já se comentou. Não repetir pessoa nem post dos últimos 14 dias.

Ler também `perfil.md` para saber qual é o perfil-alvo de conexão. Ele muda com o tempo, conforme o gargalo do SSI se desloca.

## Passo 2: encontrar 10 pessoas

Buscar com `~~navegador` 10 perfis que batam com o alvo definido em `perfil.md`. Critérios que aumentam a taxa de aceite:
- Segundo grau, com conexões em comum
- Mesmo setor ou mesmo tipo de produto
- Atividade recente na plataforma (perfil morto não retribui)

Montar a lista com nome, cargo, empresa e por que aquela pessoa faz sentido. Uma linha por pessoa, sem enfeite.

## Passo 3: encontrar 2 ou 3 posts para comentar

Procurar posts recentes e relevantes do nicho onde haja algo real a dizer. Para cada um, escrever um rascunho de comentário.

**O padrão de comentário que funciona** (medido: comentários assim rendem milhares de impressões, elogio genérico rende dezenas):
- Contar uma construção pessoal concreta, com a ferramenta nomeada, o que ela faz e o resultado
- Ou trazer um dado ou um caso que complementa o que o autor disse
- Nunca elogio genérico ("excelente post!", "muito bom, parabéns")
- Nunca discordar de forma seca, sem oferecer nada em troca

Comentário bom é um mini-post. Ele é lido por toda a audiência do autor, que costuma ser maior que a sua, e é por isso que rende tanto.

## Passo 4: apresentar e esperar

Entregar o relatório com as 10 pessoas e os comentários propostos. Perguntar o que aprovar. Aceitar aprovação parcial, é comum o usuário cortar um ou dois.

## Passo 5: executar o aprovado

Só depois do sim explícito:
- Enviar convite sem nota (nota reduz taxa de aceite em conexão fria)
- Publicar os comentários aprovados, exatamente como foram aprovados

## Passo 6: registrar

Escrever em `log-engajamento.md`: data, status (ENVIADO ou PROPOSTO), pessoas e posts. Esse arquivo é a memória entre execuções, porque cada rodada agendada começa sem o contexto da conversa anterior.

Fechar as abas que a rotina abriu.

## Como o alvo evolui

O perfil-alvo de conexão não é fixo. Revisar quando o SSI estagnar: se o pilar de relacionamento já está bom e o de "encontrar as pessoas certas" está travado, o alvo provavelmente está errado, geralmente porque está mirando pares em vez de pessoas que abrem portas (liderança da área, recrutadores especializados, quem decide contratação).
