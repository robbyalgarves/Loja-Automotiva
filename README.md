# Loja Automotiva – Auto Prime Custom (AC1)

Projeto desenvolvido para a entrega da AC1, utilizando Power BI, com foco em **análise de dados** aplicada ao contexto de uma loja automotiva.

---

##  Objetivo do Projeto
Desenvolver um **dashboard interativo** para análise do **potencial de mercado da Região Metropolitana de São Paulo (RMSP)**, combinando dados públicos de **frota de veículos** com um **cenário de faturamento fictício por município**, incluindo uma visão temporal mensal.

O projeto segue os princípios do **manifesto ágil**, priorizando **software em funcionamento** como principal evidência de progresso.

---

## Dados Utilizados

### Frota de Veículos
Os dados de frota de veículos utilizados no projeto possuem **recorte da Região Metropolitana de São Paulo (RMSP)** e foram obtidos a partir de **bases públicas oficiais**, como o **RENAVAM**.  
Esses dados representam o **total de veículos por município**, sendo utilizados para dimensionar o tamanho do mercado automotivo em cada região.

Devido ao tamanho do arquivo original de frota, o **CSV completo não foi incluído neste repositório**, pois excede o limite de armazenamento do GitHub.  
A análise completa pode ser verificada por meio do **arquivo PBIX** disponível neste repositório e no **vídeo de demonstração da AC1**.

### Faturamento
Os dados de faturamento são **totalmente fictícios**, criados exclusivamente para **fins acadêmicos**, com o objetivo de **simular análises comerciais** por município e por período, conforme orientações da disciplina.

---

##  Funcionalidades do Dashboard (AC1)

- Gráfico de **Frota de Veículos por Município**
- Gráfico de **Faturamento Fictício por Município**
- Card de **Total de Faturamento**
- Card de **Ticket Médio (estimado)**
- Segmentador de **Mês/Ano** para análise temporal
- Dashboard com **identidade visual própria**

### Observação sobre o Ticket Médio
O indicador de **Ticket Médio** representa uma **estimativa acadêmica**, calculada a partir do faturamento fictício, considerando uma média de atendimentos por município.  
Esse indicador tem como objetivo **apoiar análises comparativas** entre municípios e períodos, não representando dados reais de vendas.

---

## Gerenciamento do Projeto
O acompanhamento e a organização das atividades foram realizados por meio de um **Board Kanban**, utilizando o **GitHub Projects**, onde estão registradas as tarefas relacionadas à AC1 e seu status de conclusão.

* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *

## ✅ AC2 – Desempenho de Serviços (Jan–Jun/2025)

Na AC2 foi implementada a funcionalidade **Desempenho de Serviços**, com o objetivo de analisar o faturamento por tipo de serviço no primeiro semestre de 2025 (Jan–Jun).

### Funcionalidades:
- Slicer de Mês/Ano (Jan/25 – Jun/25)
- Indicador de Faturamento Total – Serviços Automotivos
- Indicador de Faturamento do Serviço Líder (Mês)
- Ranking de faturamento por serviço (gráfico de colunas)
- Participação percentual por serviço (gráfico de rosca)

Todos os visuais respondem dinamicamente ao mês selecionado, caracterizando uma funcionalidade completa e independente em relação à AC1.

### Fonte dos dados:
- Frota: RENAVEC (dados públicos – RMSP)
- Faturamento e serviços: dados fictícios para fins acadêmicos

## ✅ AC3 – Evolução do Faturamento (Jul–Dez/2025)

Nesta entrega foi desenvolvida a funcionalidade de **Evolução do Faturamento**, com foco na análise temporal do faturamento da loja automotiva Auto Prime Custom no segundo semestre de 2025.

### Funcionalidades:
- Segmentação de Mês/Ano (Jul–Dez)
- Indicador de faturamento total do período
- Indicador de crescimento do faturamento
- Gráfico de linha com a evolução temporal
- Gráfico de colunas com comparação mensal

Todos os visuais respondem dinamicamente à segmentação de Mês/Ano.

✅ Prova Final – Demanda por Serviços na RMSP (Jan–Mar/2026)

Na Prova Final foi implementada a funcionalidade **Demanda por Serviços na RMSP**, com o objetivo de identificar municípios com maior potencial de necessidade de serviços automotivos a partir da análise de sinistros de trânsito.

A análise utiliza dados reais obtidos no Portal de Dados Abertos do Estado de São Paulo, no conjunto **Eventos de Sinistro**, disponibilizado pelo Sistema de Informações Gerenciais de Sinistros de Trânsito (Infosiga).

Para esta entrega, foi utilizado um recorte dos meses de Janeiro, Fevereiro e Março de 2026.

Funcionalidades:
- Slicer de Mês/Ano (Jan/26 – Mar/26)
- Indicador de Total de Sinistros
- Indicador de Índice de Demanda
- Mapa ArcGIS apresentando a distribuição geográfica da demanda por município
- Gráfico de colunas com o Índice de Demanda por Município
- Tabela de apoio com município, total de sinistros, índice de demanda e serviço sugerido
- Menu lateral de navegação entre as abas do dashboard

O **Índice de Demanda** foi criado para ponderar os sinistros de acordo com sua gravidade, atribuindo maior peso às ocorrências graves. Dessa forma, a análise considera não apenas a quantidade de ocorrências, mas também seu impacto potencial na necessidade de serviços automotivos.

Todos os visuais respondem dinamicamente ao filtro de Mês/Ano, permitindo analisar a variação da demanda ao longo do período selecionado.

A funcionalidade caracteriza-se como uma nova análise em relação às entregas anteriores, pois utiliza dados reais de sinistros para apoiar a identificação de oportunidades estratégicas de atuação para a Auto Prime Custom.

Fonte dos dados:
- Frota: RENAVEC (dados públicos – RMSP)
- Faturamento e serviços: dados fictícios para fins acadêmicos
- Sinistros de trânsito: Portal de Dados Abertos do Estado de São Paulo – Eventos de Sinistro  
  https://dadosabertos.sp.gov.br/dataset/eventos-de-sinistro

Modelo de Dados – MER:
Foi desenvolvido o arquivo **MER_Demanda_Servicos_RMSP.png**, contendo o modelo entidade-relacionamento da Prova Final, com PK, FK, atributos e relacionamento entre as entidades.

Entidades do MER:
- **Municipios**
  - PK cod_ibge
  - municipio

- **Sinistros**
  - PK id_sinistro
  - FK cod_ibge
  - data_sinistro
  - ano_sinistro
  - mes_sinistro
  - municipio
  - tp_sinistro_primario
  - qtd_gravidade_grave
  - qtd_gravidade_leve
  - latitude
  - longitude
  - MesAno_Prova
  - MesAno_Ordem
  - Servico Sugerido

Relacionamento:
- Municipios 1 : N Sinistros



