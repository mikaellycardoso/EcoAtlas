# 🌳 EcoAtlas: Data Intelligence Against Urban Warming
### Statistical Analysis of Vegetation Loss & Temperature Rise — Vitória, ES (2021–2024)

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![Power BI](https://img.shields.io/badge/Power_BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=for-the-badge&logo=jupyter&logoColor=white)
![SciPy](https://img.shields.io/badge/SciPy-8CAAE6?style=for-the-badge&logo=scipy&logoColor=white)

---

## 📌 About the Project

**EcoAtlas** is an end-to-end data science project investigating the relationship between urban deforestation and temperature variation in the city of Vitória, Espírito Santo, Brazil — from 2021 to 2024.

The goal is to use open government data to **statistically prove** the climate impact of vegetation loss at the urban micro-level, transforming raw data into actionable intelligence for public policy and ESG decision-making.

---

## ❓ The Problem

Urban heat is not just a feeling — it's a measurable consequence of planning decisions.

During daily commutes through Vitória, a clear pattern emerged: wherever urban trees were removed, the heat became noticeably worse. Open datasets on vegetation suppression (MapBiomas) and historical temperature records (INMET) existed separately, in isolated government silos. **Without crossing these datasets, the true environmental cost of urban deforestation remained invisible** — masking the formation of heat islands that directly affect the health and quality of life of the population.

---

## 🛠️ Methodology

The project follows a complete Data Science cycle:

**1. Data Extraction**
- Daily climate series via **INMET** (Brazil's National Meteorology Institute)
- Annual vegetation cover data via **MapBiomas**

**2. Data Cleaning & Processing (Python/Pandas)**
- Null value treatment and outlier detection
- Date type normalization
- Cross-granularity merging: daily climate data × annual urban geography data
- This was the core technical challenge — ensuring analytical consistency when combining datasets with incompatible time granularities

**3. Statistical Analysis (Python/SciPy/Seaborn)**
- Exploratory Data Analysis (EDA) with scatter plots and distribution charts
- Hypothesis testing: Pearson Correlation Coefficient + p-value calculation
- Seasonal noise mitigation to isolate the deforestation signal from natural temperature variation

**4. Visualization & Storytelling (Power BI/DAX)**
- Interactive geospatial dashboard with Shape Maps
- DAX Time Intelligence for seasonal filtering and trend analysis
- UX-focused design for non-technical decision-makers

---

## 📊 Key Results

| Metric | Value |
|---|---|
| Pearson Correlation (r) | 0.157 |
| p-value | 0.0000 |
| Analysis period | 2021–2024 |
| Data sources | INMET · MapBiomas |

**Conclusion:** The p-value of `0.0000` confirms a **statistically significant warming trend** associated with vegetation loss. The correlation of `0.157` — positive but moderate — reflects the reality of a model exposed to strong seasonal noise (winter temperature drops), proving that even with natural variation, vegetation suppression pulls the long-term thermal trend upward.

---

## 📊 [Access the Interactive Dashboard →](https://app.powerbi.com/reportEmbed?reportId=331ac0fc-fb54-40da-aa15-f74c0db65141&autoAuth=true&ctid=b9976b30-8143-4ac5-a408-f906b4062b85)

---

## 📁 Repository Structure

```
EcoAtlas/
├── data/
│   ├── raw/              # Original INMET and MapBiomas exports
│   └── processed/        # Cleaned and merged datasets
├── notebooks/
│   ├── 01_extraction.ipynb
│   ├── 02_cleaning.ipynb
│   ├── 03_analysis.ipynb
│   └── 04_visualization.ipynb
├── dashboard/            # Power BI .pbix file
├── outputs/              # Charts and statistical outputs
└── README.md
```

---

## 💻 How to Reproduce

```bash
# Clone the repository
git clone https://github.com/mikaellycardoso/EcoAtlas.git

# Install dependencies
pip install pandas matplotlib seaborn scipy

# Run notebooks in order
# Raw and processed data are in the /data folder
# The .pbix dashboard file is available in /dashboard
```

---

> **Technical note:** This project uses the latest cycle of consolidated data available (2021–2024), respecting the official processing and publication timelines of the cited government sources. The project will be updated as new 2025 data windows become available.

---

## 👩‍💻 Author

**Mikaelly Cardoso** — Undergraduate Researcher in AI & Data Science  
FAESA Centro Universitário Espírito-Santense · Vitória, ES, Brazil

[![LinkedIn](https://img.shields.io/badge/LinkedIn-mikaelly--cardoso-0A66C2?style=flat&logo=linkedin)](https://linkedin.com/in/mikaelly-cardoso)
[![Lattes](https://img.shields.io/badge/Lattes-CNPq-blue?style=flat)](http://lattes.cnpq.br/6340388262242435)
[![Portfolio](https://img.shields.io/badge/Portfolio-mikaellycardoso.github.io-4CAF50?style=flat)](https://mikaellycardoso.github.io/mikaelly-cardoso.github.io/)
