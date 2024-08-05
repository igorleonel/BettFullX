# 1. BettFullX

A BetFullX, é uma plataforma de apostas que surgiu em 2019 aproveitando a legislação que permite apostas esportivas, e tem enfrentado desafios significativos desde o final de 2022. A empresa tem perdido espaço para concorrentes devido a uma queda na performance das odds oferecidas, que são menos atrativas para os apostadores em comparação com outras plataformas.

Sendo assim, a empresa pretende contratar um serviço que forneça dados via API para aprimorar seus KPIs, obter uma visibilidade completa dos jogos e garantir informações detalhadas e precisas para uma análise mais eficaz, resultando em melhores performances nas odds.

Antes de treinar algoritmos, a necessidade da BetFullX é ter os principais KPIs estratégicos organizados em uma única ferramenta, permitindo que os clientes possam consultá-los facilmente e tomar decisões simples, porém importantes, com base em informações precisas e detalhadas sobre os jogos.

Para acompanhar os principais indicadores e ajudar a melhorar a performance das odds, a BetFullX precisa ter as seguintes métricas:

## Análise Por Rodada

1. Análise por Rodada
2. Gols, com média por partida
3. Chutes a gol, com média por partida
4. Passes, com precisão e média por partida
5. Faltas, com total de cartões e média por partida
6. Total de Partidas
7. Porcentagem de vitórias em casa, como visitante e empate
8. Análise por fases do campeonato (Qualificatória, Play-offs, Fase de Grupos, Oitavas, Quartas, Semi e Final)
9. Análise por Times
10. Análise por Casa/Visitante
11. Análise de Correlação.

## Análise por Confronto

1. Vitórias
2. Gols
3. Posse
4. Chutes
5. Chutes a gol
6. Posse de bola
7. Passes
8. Precisão de passes
9. Impedimentos
10. Escanteios

## Análise Estatísticas

1. Quantos gols são esperados que um time qualquer faça?
2. Quantos gols cada time selecionado faz na média?
3. Quantos gols cada time selecionado recebe na média?
4. Estimar quantos gols cada time vai fazer, baseado em quantos gols eu espero que o outro time tome a mais do que a média.
5. Quais são os possíveis placares?
6. Qual a probabilidade de um time fazer um certo número de gols, dada a FREQUÊNCIA MÉDIA ESPERADA de gols?

# 2. Premissas do Negócio

1. A análise foi realizada com dados da Champions League 2023, coletados entre 01/01/2023 e 31/12/2023.
2. Os dados foram extraídos da [API-Football](https://www.api-football.com/documentation-v3#section/Introduction) utilizando Python.
3. Os testes foram realizados via [Postnam](https://www.postman.com/).
4. Para armazenar e transformar os dados, utilizou-se o BigQuery em conjunto com SQL.
5. A visualização dos dados foi feita no Power BI.

# 3. Estratégia da Solução

## Entendimento
**Objetivo:** Melhorar a precisão das odds e aumentar a competitividade da BetFullX no mercado de apostas esportivas.

**Ferramentas:**

1. **Postman:** Para testar e validar as chamadas à API.
2. **Python:** Para a extração e transformação dos dados.
3. **Google Cloud Console:** Para armazenamento e processamento dos dados.
4. **BigQuery:** Para consultas SQL e criação de views.
5. **Power BI:** Para visualização e compartilhamento de insights.
6. **Dax:** Para criação dos KPI's e da modelagem de dados.

## Solução
**Objetivo:** Desenvolver e implementar a solução técnica para extrair, transformar e visualizar os dados.

**Passos:**

**Extração dos Dados:**

Desenvolvimento de scripts em Python para fazer chamadas à API-Football e extrair dados detalhados da Champions League 2023, incluindo gols, passes, faltas, escanteios, cartões e impedimentos.
Execução de testes com Postman para garantir que as chamadas à API retornem os dados corretos.

**Transformação dos Dados:**

Utilização de Python para limpar e transformar os dados extraídos, garantindo consistência e qualidade.
Carregamento dos dados transformados no BigQuery para armazenamento.

**Cargas Incrementais:**

Implementação de um processo automatizado para realizar cargas incrementais, assegurando que apenas novos dados sejam adicionados ao banco de dados, mantendo-o sempre atualizado.

**Análise e Modelagem dos Dados:**

Utilização de consultas SQL no BigQuery para criação de views e modelagem dos dados.
Geração de KPIs robustos, como média de gols por partida, precisão de passes, faltas e cartões, total de partidas, e porcentagem de vitórias em casa e fora.

## Implementação
**Objetivo:** Automatizar o processo, visualizar os dados e garantir acesso fácil às informações.

**Passos:**

**Visualização dos Dados:**

Criação de dashboards interativos no Power BI para visualização dos KPIs e análises.
Utilização do DAX para modelagem matemática.
Configuração de relatórios e gráficos que permitem uma visão clara e detalhada do desempenho dos times e das odds.

**Hospedagem na Nuvem:**

Hospedagem dos dashboards do Power BI na nuvem para garantir acesso em qualquer dispositivo conectado à internet.
Configuração de permissões de acesso para diferentes níveis de usuários.

## 4. Top 3 Insights de dados



## 5. O produto final do projeto

Painel online, hospedado em um Cloud e disponível para acesso em qualquer dispositivo conectado à internet.

O painel pode ser acessado através desse link: https://igor-project-cury-company.streamlit.app/

## 6. Conclusão

O objetivo desse projeto é melhorar as odds para os clientes e fornecer um conjuntos de gráficos e/ou tabelas que exibam os melhores indicadores dos jogos em tempo real. Da visão das odds, podemos concluir que as análises estatísticas como correlações, gols esperados e  probabilidade de placar foram acertivos de acordo com os resultado reais dos jogos.
