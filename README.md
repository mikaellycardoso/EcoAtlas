# 🌳 EcoAtlas: Análise de Impacto Climático e Expansão Urbana em Vitória-ES (2021-2024)

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![Power BI](https://img.shields.io/badge/Power_BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=for-the-badge&logo=jupyter&logoColor=white)

## 📌 Sobre o Projeto
O **EcoAtlas** é um projeto de Análise de Dados ponta a ponta que investiga a relação entre a supressão vegetal (desmatamento urbano) e a variação da temperatura média na cidade de Vitória, Espírito Santo, durante o ciclo de 2021 a 2024. O objetivo é utilizar dados públicos para provar, estatística e visualmente, os impactos climáticos das mudanças na cobertura vegetal do município.

## ❓ O Problema de Negócio
Com o avanço da expansão urbana, questiona-se o impacto direto da perda de áreas verdes no microclima local. A hipótese central deste projeto testa se a redução de hectares de vegetação possui uma correlação matemática positiva com o aumento das temperaturas médias registradas na cidade.

## 🛠️ Metodologia e Ferramentas
O projeto foi desenvolvido seguindo o ciclo completo de Ciência de Dados:

1. **Extração de Dados (Data Gathering):** Coleta de dados climáticos diários via **INMET** (Instituto Nacional de Meteorologia) e dados anuais de cobertura vegetal via **MapBiomas**.
2. **Limpeza e Tratamento (Python/Pandas):** Uso de Jupyter Notebooks para tratamento de valores nulos, conversão de tipagem de datas e mesclagem (Merge) de bases de granularidades diferentes (diária vs. anual).
3. **Análise Exploratória e Estatística (Python/Seaborn/SciPy):** Aplicação de Gráficos de Dispersão e cálculo do Coeficiente de Correlação de Pearson para validação de hipóteses.
4. **Visualização de Dados e Storytelling (Power BI):** Desenvolvimento de um dashboard interativo focado na experiência do usuário (UX), contendo mapas de calor, tooltips dinâmicos e métricas de impacto (ex: conversão de hectares para campos de futebol). Linguagem DAX utilizada para inteligência de tempo e categorização de estações do ano.

## 📊 Principais Descobertas e Validação Estatística
Ao cruzar a base diária do INMET com os dados anuais do MapBiomas, a análise estatística no Python revelou os seguintes números:

* **Coeficiente de Correlação (r):** `0.157`
* **P-valor:** `0.0000`

**Conclusão Analítica:** O p-valor de `0.0000` demonstra uma **tendência estatisticamente significativa** de aquecimento associada à perda de vegetação. A correlação de `0.157` (positiva, porém moderada) reflete a realidade de um modelo submetido ao forte ruído da sazonalidade natural (estações do ano), provando que, mesmo com as quedas bruscas de temperatura no inverno, a supressão vegetal puxa a linha de tendência térmica geral para cima.

## 💻 Como reproduzir este projeto
1. Clone este repositório: `git clone https://github.com/mikaellycardoso/EcoAtlas.git`
2. Instale as dependências: `pip install pandas matplotlib seaborn scipy`
3. Os dados brutos e tratados estão na pasta `data/`.
4. Execute os scripts na pasta `notebooks/` na ordem numérica para reproduzir a limpeza e o teste estatístico.
5. O arquivo `.pbix` do dashboard está disponível na raiz do projeto para visualização no Power BI Desktop.

---
**Desenvolvido por:** Mikaelly
*Estudante de Sistemas de Informação e aspirante a Cientista de Dados, com foco em transformar dados complexos em decisões de negócio.*
