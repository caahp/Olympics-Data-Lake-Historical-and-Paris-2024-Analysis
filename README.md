# Olympics Data Lake: Historical and Paris 2024 Analysis

This project builds a local **Data Lake** to integrate and analyze data from two main sources:

1. **Historical Olympics data (1896–2022)** – provided by [Base dos Dados](https://basedosdados.org/dataset/62f8cb83-ac37-48be-874b-b94dd92d3e2b).
2. **Paris 2024 Summer Olympics data** – provided by [Kaggle](https://www.kaggle.com/datasets/piterfm/paris-2024-olympic-summer-games).

The goal is to process, integrate, and analyze Olympic Games data, producing descriptive statistics and visualizations to answer key analytical questions.

## ⚙️ ETL Process

1. **Raw Layer (`raw/`)**
   - Store original files as downloaded.
   - Generate metadata (`metadata.json`) with dataset description, source, and collection date.

2. **Bronze Layer (`bronze/`)**
   - Convert CSV/CSV.GZ files to **Parquet**.
   - Keep metadata aligned with processed files.
   - Integrate historical and Paris 2024 data into a unified dataset.

3. **Gold Layer (`gold/`)**
   - Generate summary tables, descriptive statistics, and visualizations.
   - Store Jupyter notebooks, charts, and reports.

---

## 📊 Analytical Questions Answered

1. **How has the distribution of medals by country evolved from 1986 to Paris 2024?**  
   - Statistics: total medals per country, average per edition.  
   - Visualizations: line charts, bar plots.  

2. **Which sports grew the most in terms of participants between 1986 and 2024?**  
   - Statistics: participants per sport, historical average vs. Paris 2024, median/mode analysis.  
   - Visualizations: growth plots per sport.  

3. **How has the proportion of male vs. female athletes evolved in main sports up to Paris 2024?**  
   - Statistics: gender proportion by edition and sport.  
   - Visualizations: boxplots, stacked bar charts.  

---

## 🚀 Getting Started

### Requirements
- Python 3.10+
- Pandas
- PyArrow
- Jupyter Notebook
- KaggleHub (for downloading Paris 2024 dataset)
