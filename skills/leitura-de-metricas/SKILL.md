---
name: leitura-de-metricas
description: Puxa e interpreta as métricas reais do LinkedIn: impressões, reações, comentários, salvamentos e seguidores por post, além do SSI e da demografia da audiência. Acione quando o usuário perguntar "como foi meu post", "quantas impressões", "como está meu SSI", "analisa meu desempenho", "por que esse post não engajou", "quantas publicações eu já fiz", ou quando o planejamento semanal precisar do Passo 0.
---

# Leitura de métricas

Coleta o dado real e transforma em decisão editorial. Sem isso o resto do plugin opera no escuro.

## O que o LinkedIn entrega e o que não entrega

Entrega, para perfil pessoal:
- Por post: impressões, reações, comentários, compartilhamentos, salvamentos, envios, visualizações de perfil geradas e seguidores ganhos
- Agregado de 28 dias
- Demografia de quem foi alcançado: cargo, senioridade, setor, localidade, tamanho de empresa
- SSI, numa página própria, com os quatro pilares separados

**Não entrega:** horário de atividade da audiência. Isso existe só para página de empresa. Não prometer esse dado ao usuário; ele não existe para buscar.

## Onde buscar

Com `~~navegador`, já logado na conta do usuário:
- Atividade recente do perfil: a aba de publicações lista cada post com as impressões na frente
- Análise por post: cada post tem um link de "visualizar análise" que abre o detalhe completo
- Agregado: a página de análise de conteúdo, com filtro de 7, 28 ou 90 dias
- Audiência: a página de análise de público
- SSI: a página própria de social selling index

Validar sempre por screenshot. A interface roda com carregamento tardio, e leitura de DOM sozinha devolve resultado incompleto.

## Truque útil: horário exato de qualquer publicação

O identificador de cada publicação carrega o timestamp de criação embutido. Para extrair:

```js
new Date(Number(BigInt(idDaPublicacao) >> 22n))
```

O identificador aparece nos atributos dos elementos do post e nos links de análise. Isso permite reconstruir o horário exato de todo o histórico e cruzar com desempenho, o que é a única forma de responder se horário importa para aquele perfil específico.

## Como interpretar, não só reportar

Número sem leitura não serve. Sempre entregar o diagnóstico junto.

**Procurar o padrão, não o total.** Em conteúdo orgânico a distribuição é extremamente desigual: é normal 2 posts responderem por 80% ou mais do alcance de um mês. O total esconde isso. O que importa é o que separa os acertos dos fracassos.

**Cruzar sempre pelo menos duas variáveis.** Um post fraco isolado não diz nada. Três posts do mesmo autor, na mesma semana, dois do mesmo tema, com resultados de ordens de grandeza diferentes, dizem tudo. Procurar comparações naturalmente controladas dentro do próprio histórico.

**Ler os comentários, não só contá-los.** O que as pessoas escrevem é a fonte mais rica de tema novo, de objeção e de vocabulário do público. Discordância densa de alguém sênior vale mais que dez concordâncias, porque indica território disputado, que é onde o alcance nasce.

**Comparar salvamento com comentário.** Salvamento indica utilidade; comentário indica debate. São motores diferentes, e cada perfil tem um dominante. Descobrir qual é o do usuário muda o que escrever.

## Registrar

Escrever tudo em `aprendizados-publico.md`: números crus em tabela, diagnóstico, temas para dobrar a aposta, o que otimizar e refinamento do perfil do público.

Esse arquivo é cumulativo. Depois de umas 3 semanas ele passa a valer mais que qualquer benchmark de fora, inclusive mais que os exemplos que vieram neste plugin.

## Cuidado com experimento sujo

Se o usuário mudou mais de uma variável entre semanas (dia, horário, formato, tipo de gancho), avisar que a leitura fica ambígua e dizer exatamente o que não será possível concluir. É melhor admitir isso do que atribuir causa errada e gravar um aprendizado falso na memória.
