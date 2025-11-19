🎯 Objetivo do Projeto- Criando um Relatório Vendas e Lucros com Data Analytics com Power BI

- Remodelar a Página 1 do relatório para alinhar visualmente e estruturalmente com o padrão adotado nas demais páginas, garantindo consistência de layout, estilo e experiência do usuário.
- Desenvolver uma Página 2 dedicada exclusivamente aos visuais e medidas utilizadas pela professora no módulo do desafio, com foco em replicabilidade e referência técnica. Os visuais foram destacados e segmentados conforme necessário para facilitar a análise.
- Implementar indicadores de alternância de visualizações dentro de um mesmo espaço da página, permitindo a troca dinâmica entre gráficos sem sobreposição visual.
- Criar botões de navegação entre páginas, incluindo um botão “Home” para retorno à página principal, promovendo uma navegação fluida e intuitiva entre seções do relatório.
- Aplicar função de cores personalizada para destacar visualmente métricas ou categorias relevantes, reforçando a hierarquia de informação e facilitando a leitura dos dados.
- Construir agrupamentos temporais para análise por semestre, permitindo comparações agregadas entre períodos e facilitando a leitura de tendências.
- Incorporar visualização em formato de histograma para representar a distribuição de dados de forma clara e estatisticamente relevante.

![Visualização da Página 3](Docs/pagina3.png)

Estrutura do projeto
🟩 Página Principal — Visão Executiva
A primeira página do relatório apresenta uma visão consolidada das principais métricas de desempenho comercial, com foco em indicadores de volume e valor de vendas. A estrutura foi otimizada para facilitar a leitura e promover uma análise rápida e eficaz.
Componentes principais:
- Gráfico de linha “Vendas por Período”
Representa a evolução temporal das vendas, permitindo identificar tendências e sazonalidades ao longo dos meses.
- Treemap “Total de Vendas por País”
Exibe a distribuição geográfica das vendas por país. Inclui um botão de navegação que alterna para uma visualização em mapa geográfico, oferecendo uma perspectiva espacial mais intuitiva.
- Visualização de Vendas por Segmento
Apresenta os dados segmentados por tipo de cliente ou canal. A visualização é dinâmica, com um botão de alternância que permite trocar entre gráfico de pizza e gráfico de barras, conforme a preferência analítica.
- Sistema de Navegação entre Páginas
Botões estilizados com ícones personalizados foram implementados para facilitar a transição entre as páginas do relatório, promovendo uma experiência de navegação fluida e intuitiva.

🟨 Página 2 — Detalhes de Vendas
Esta página foi projetada para oferecer uma análise detalhada e comparativa entre produtos e períodos mensais, com foco em volume de vendas e desempenho por categoria. A estrutura favorece a leitura horizontal e a alternância entre visuais para facilitar a exploração dos dados.
Componentes principais:
- Histograma de Unidades Vendidas por Mês
Representa a distribuição mensal das unidades vendidas, permitindo identificar padrões de concentração e variações sazonais.
- [Visual Detalhada → Visualização Detalhada] de Vendas Mensais por Produto
Apresenta os valores de vendas por produto ao longo dos meses. Inclui um botão de navegação que alterna para uma visualização agregada por semestre, facilitando a análise por períodos consolidados.
- Gráfico Horizontal “Vendas por Produto”
Exibe os produtos com maior volume de vendas.

🟦 Página 3 — Destaques de Vendas
A terceira página do relatório é dedicada à análise aprofundada dos principais destaques comerciais, com foco em desempenho por produto, período e região. As visualizações foram organizadas para facilitar a identificação de padrões de alta performance e correlações entre métricas-chave.
Componentes principais:
- Gráfico de Colunas — Top 3 Meses por Produto
Exibe os três meses com maior volume de vendas, segmentado por produto. Cada produto é representado por uma cor distinta, destacando visualmente os itens de maior impacto.
- Gráfico de Dispersão — Vendas, Unidades Vendidas e Lucro
Relaciona as principais métricas por produto e mês, permitindo identificar correlações entre volume de vendas, quantidade comercializada e rentabilidade.
- Gráfico Combinado — Representatividade dos Top 3 Produtos por País
Visualização integrada que combina colunas empilhadas e barras horizontais para representar o total de vendas por país, destacando quanto os três produtos líderes contribuem para o volume geral em cada região. Essa abordagem permite uma análise cruzada entre concentração de receita por produto e distribuição geográfica de desempenho, facilitando a identificação de mercados estratégicos e produtos de maior impacto comercial.
- Gráfico Horizontal — Top 5 Meses em Vendas e Lucros
Identifica os cinco meses com maior desempenho financeiro, considerando simultaneamente volume de vendas e lucratividade. Permite análise temporal comparativa.

✅ Funcionalidades Implementadas
- Aplicação de princípios de UX: contraste, proporção áurea, hierarquia visual.
- Segmentações sincronizadas entre páginas.
- Botões de navegação com ícones representativos.
- Alternância de gráficos via botão de indicador.
- Estilização consistente: paleta de cores, tipografia e espaçamento.
- Gráficos otimizados para storytelling visual.

🧩 Fórmulas e Modelagem
A modelagem do relatório foi construída com base em boas práticas de DAX, visando performance, legibilidade e flexibilidade analítica. Abaixo estão os principais recursos implementados:
- Medida base de vendas
TotalVendas = SUM(FinancialSample[Sales])
Soma total das vendas, utilizada como métrica principal em diversos visuais.
- Formatação temporal personalizada
AnoMesAbrev = FORMAT('Calendario'[Date], "YYYY - MMM")
Criação de coluna para exibição de período no formato “Ano - Mês abreviado”, utilizada em gráficos e segmentações.
- Agrupamento de produtos para análise em histograma
Produtos foram categorizados em faixas de volume ou desempenho para facilitar a visualização da distribuição em histogramas.
- Função para divisão por semestre
Implementada lógica DAX para classificar datas em primeiro ou segundo semestre, permitindo análises agregadas por período:
Semestre = IF(MONTH('Calendario'[Date]) <= 6, "1º Semestre", "2º Semestre")
- Fórmulas para Top N dinâmico
Utilização de funções como TOPN, RANKX e CALCULATE para identificar os principais produtos, países ou meses com base em critérios de vendas ou lucro.
- Fórmulas específicas para Top 5 meses por vendas em produto
Construídas medidas e tabelas auxiliares para destacar os cinco meses com maior volume de vendas por produto, com ordenação correta e segmentação visual.
- Uso de medidas em vez de colunas calculadas para melhor performance.
- Ordenação correta de meses por chave numérica.
- Documentação das fórmulas e transformações para reuso.

report.pbix         — arquivo principal do Power BI  
README.md           — este arquivo  

docs/  
└── relatorio.png   — captura do relatório  

assets/  
├── icones/         — ícones utilizados nos botões de navegação  
├── temas/          — arquivos de tema (.json) aplicados ao relatório  
└── imagens/        — imagens complementares usadas nos visuais ou como plano de fundo  


▶️ Como usar
- Abra report.pbix no Power BI Desktop.
- Navegue pelas páginas usando os botões de navegação.
- Explore os gráficos interativos e segmentações.
- Na Página 3, observe os Top 3 meses por produto e o país líder em vendas.

▶️ Próximos passos sugeridos
- Adicionar uma página de onboarding para orientar usuários finais.
- Incluir testes de qualidade de dados e checkpoints de performance.

⚡ Teste de Performance
- Avaliação feita com Performance Analyzer do Power BI.
- Visuais principais apresentam tempos de execução otimizados.
- Matrizes com alta cardinalidade exigem atenção futura para escalabilidade.
✍️ Autor
Victor Biscaia
linkedin: https://www.linkedin.com/in/victor-biscaia-097603371/
