# Conectores

## Como as referências a ferramentas funcionam

Os arquivos deste plugin usam `~~categoria` como marcador para a ferramenta que você conectar naquela categoria. O plugin descreve o fluxo por categoria, não por produto, então funciona com qualquer ferramenta equivalente.

## Conectores usados por este plugin

| Categoria | Marcador | Opções |
|---|---|---|
| Navegador controlável | `~~navegador` | Claude in Chrome, Control Chrome, ou qualquer extensão que permita navegar e ler páginas |

## O que é obrigatório

**Um navegador controlável é obrigatório.** O LinkedIn não expõe API pública de leitura de desempenho de post nem de SSI para perfil pessoal. Todo o trabalho de análise, agendamento e engajamento acontece pela interface web, com você já logado na sua conta.

Sem navegador conectado, o plugin ainda funciona em modo reduzido: consegue escrever e revisar posts aplicando o método, mas não consegue ler suas métricas, agendar publicações nem executar o engajamento diário. Nesse caso ele vai pedir que você cole os números manualmente.

## O que NÃO é usado

Este plugin não pede acesso a e-mail, calendário, CRM, banco de dados nem armazenamento em nuvem. Todo o estado dele vive em arquivos markdown na pasta do seu projeto.
