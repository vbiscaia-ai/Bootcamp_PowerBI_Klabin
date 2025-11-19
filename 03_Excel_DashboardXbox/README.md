# 📊 Dashboard de Comparação de Vendas 2024  
**Game Pass Minecraft x EA Play Plus**

## 🎯 Objetivo
O objetivo deste dashboard é realizar a **comparação mês a mês das vendas no ano de 2024** entre dois serviços de assinatura de jogos:  
- **Game Pass do Minecraft**  
- **EA Play Plus**

A análise foi construída em Excel, utilizando Tabelas Dinâmicas, Segmentações e **gráfico pictórico**, com foco em transformar dados brutos em **informações visuais e acionáveis**.

---

## 🖼️ Destaque Visual: Gráfico Pictórico
O dashboard utiliza um **gráfico pictórico** para representar visualmente os dados de vendas, tornando a análise mais intuitiva e atrativa.

![Gráfico Pictórico](https://raw.githubusercontent.com/vbiscaia-ai/Dashboard-xbox/main/docs/pictorio.png)

---

## 🐞 Erro Descoberto e Aprendizado
Durante o desenvolvimento identificamos um problema causado por **títulos de colunas parecidos**.  
- O campo referente ao **Minecraft** estava **contando valores de linhas onde não havia marcação de "SIM"**.  
- Isso gerou **valores fantasmas**, inflando os resultados e comprometendo a confiabilidade da análise.

### 🔎 Impacto em um ambiente real
Em produção, esse tipo de erro pode:  
- Levar a **decisões equivocadas** de investimento ou marketing.  
- Gerar **relatórios inconsistentes** para gestores.  
- Comprometer a **credibilidade da área de dados**.  

A correção desse detalhe foi essencial para garantir que o dashboard refletisse a realidade.

---

## 📉 Insights Obtidos
Com os dados corrigidos foi possível identificar:  
- **Janeiro e Fevereiro** apresentaram valores **bem abaixo da média anual**.  
- Esses desvios recomendam investigação de causas (sazonalidade, falha em campanhas, problemas de dados) e ações corretivas.

---

## 🖼️ Menu de Segmentação de Meses
O dashboard conta com um **menu interativo de meses**, que permite:  
- **Clicar em um mês** para análise isolada.  
- **Clicar, segurar e arrastar** para selecionar vários meses simultaneamente.

![Menu de Segmentação de Meses](https://raw.githubusercontent.com/vbiscaia-ai/Dashboard-xbox/main/docs/menu_dashboard.png)

---

## 📂 Acesso ao Arquivo
O arquivo do dashboard está disponível para download:

[📥 Baixar DASH_BOARD_XBOX_VENDAS.xlsx](https://raw.githubusercontent.com/vbiscaia-ai/Dashboard-xbox/main/docs/DASH_BOARD_XBOX_VENDAS.xlsx)

---

## 🚀 Reflexão Pessoal
Este projeto foi um marco na minha jornada:  
- Ao identificar e corrigir o erro, comecei a **pensar como analista de dados**.  
- A construção do primeiro dashboard me mostrou o impacto de **transformar dados em informação**.  
- Cada ajuste no relatório aumentou minha confiança e capacidade analítica.

---

## 💡 Sugestão de Melhoria
- Criar uma **versão do dashboard totalmente em inglês**, para facilitar o compartilhamento com públicos internacionais.

---

## 👤 Autor
**Victor Biscaia**  
[GitHub: @vbiscaia-ai](https://github.com/vbiscaia-ai)
[Linkedin: @Victor_Biscaia] (https://www.linkedin.com/in/victor-biscaia-097603371/)