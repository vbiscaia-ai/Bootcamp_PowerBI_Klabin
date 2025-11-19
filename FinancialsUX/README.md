🚀 Projeto Atualização de Relatório Financeiro — Foco em Experiência do Usuário
🎯 Objetivo
Atualizar e aprimorar um relatório financeiro pré‑existente com foco em experiência do usuário (UX). O projeto reorganiza visuais, aplica princípios de design (posicionamento, contraste, proporção áurea) e adiciona controles de navegação e segmentação para facilitar a exploração dos dados. O relatório final possui 3 páginas.

### Página 3

![Página 3](Docs/pagina%203.png)

🗂 Estrutura do Relatório (3 páginas)
🟩 Página 1 — Visão Executiva (Relatório de Vendas)
Resumo das principais métricas, gráfico de área ajustado para séries temporais e matriz de descrição de vendas.
🟨 Página 2 — Detalhamento por Categoria(Relatório de lucros)
Reaplicação do estilo da primeira página com foco em comparação entre segmentos, países e lucros.
🟦 Página 3 — Visualização P e R 
- Gráfico (P e R): barras/colunas que mostram os 3 meses com maiores vendas, com barras por produto; cada produto recebe cor própria para identificação visual.
- Cartão (P e R): exibe o país com maior volume de vendas nos 3 meses identificados.
- A matriz da 3ª página foi alterada, porque repetia basicamente a mesma informação da matriz da primeira página. Criei um gráfico mostrando os 3 meses com maiores vendas por produto e um cartão com o país líder de vendas. Para priorizar o visual mais relevante, preservar a proporção áurea e aplicar boas práticas de storytelling, reorganizei a posição dos visuais na 3ª página..

✅ Funcionalidades Implementadas
- Aplicação de princípios de UX: posicionamento, contraste e proporção.
- Calendário gerado via DAX para suportar análise temporal consistente.
- Gráfico Top 3 meses por produto com legenda por produto.
- Cartão mostrando o país com maior vendas nos Top 3 meses.
- Matriz com descrição detalhada de vendas por trimestre.
- Botões de navegação entre páginas, usei icones representado cada página do relatório.
- Segmentações aplicadas e opcionais para sincronização entre páginas.
- botão indicador para alternar entre gráficos no mesmo espaço da pagina, de modo invisivel só aparece o botão que alterna para o outro gráfico.
- Estilização consistente (cores, tipografia, espaçamentos).

🧩 Exemplos de Fórmulas (excertos)
Total de vendas (medida base)
TotalVendas = SUM(FinancialSample[Sales])
Calendar auto(para criar um tabela de datas)
AnoMesAbrev = FORMAT('Calendario'[Date], "YYYY - MMM") (para criar uma coluna com mês e ano concatenados)


🛠 Boas Práticas Aplicadas
- Separação entre tabelas fato e dimensão.
- Calendário contínuo via DAX para consistência temporal.
- Preferência por medidas em vez de colunas calculadas quando adequado, visando performance.
- Ordenação correta de meses por chave numérica para evitar desalinhamentos em visuais.
- Documentação das transformações e fórmulas para reuso e revisão técnica.
- Uso de surrogate keys no ETL para estabilidade dos relacionamentos (quando aplicável).

📁 Estrutura do Repositório
- report.pbix — arquivo principal do Power BI (versão final)
- README.md — este arquivo
- docs/
- relatorio.png — captura do relatório

▶️ Como usar
- Abra report.pbix no Power BI Desktop.
- Navegue pelas três páginas usando os botões de navegação no relatório.
- Na Página 3 (Visualização P e R), verifique o gráfico e o cartão que mostram os Top 3 meses por produto e o país líder de vendas.
- Para ajustar o critério Top N, revise as medidas DAX e altere o parâmetro (por exemplo trocar 3 por outro valor onde aplicável).


▶️ Próximos passos sugeridos
- Documentar as fontes de dados e transformações no Power Query (ETL)..
- Criar tabela desconectada (parâmetro Top N) para permitir Top N dinâmico controlado por slicer.
- Adicionar testes rápidos de qualidade de dados e checkpoints de performance.
- Incluir um guia de onboarding (página inicial) no relatório para explicar controles e navegação a usuários finais.

⚡ Teste de Performance
Realizei testes de performance do relatório usando o Performance Analyzer do Power BI.
Foram avaliados tempo de renderização dos visuais, duração das consultas DAX e impacto de filtros/segmentações no tempo de resposta.
O que foi testado
- Tempo de carregamento da página inteira.
- Tempo individual de cada visual (gráfico, cartão, matriz).
- Duração das consultas DAX associadas às medidas críticas.

Resultados resumidos
- Visuais principais (gráfico Top 3 meses e cartão P e R) apresentam tempos de execução aceitáveis, com consultas otimizadas.
- Matrizes e visuais com grande cardinalidade mostraram maior latência; recomenda-se otimização adicional se o conjunto de dados crescer significativamente

✍️ Autor
Victor Biscaia
Salvador, Bahia — Brasil
LinkedIn
