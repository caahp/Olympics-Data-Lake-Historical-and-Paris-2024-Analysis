```markdown
# 🏅 Exploratory Data Analysis of the Olympic Games (1896-2024)

## 📖 Project Description

This project conducts a comprehensive exploratory data analysis (EDA) of the Olympic Games, utilizing two primary datasets: a historical collection covering the period from 1896 to 2016, and a specific dataset for the Paris 2024 games.

The main goal is to extract insights into the evolution of medal standings, the growth of different sports, and gender participation. The project also features in-depth analyses of sports powerhouses, with a special focus on Brazil's performance. The entire workflow is organized following a Data Lake architecture (Raw, Bronze, Gold) for clear data processing and presentation.

## 📊 Analyses Included

The main notebook (`.ipynb`) performs the following analyses:

* **Medal Standings Evolution:** Tracks the medal distribution by country since 1988, highlighting dominant nations.
* **Growth of Sports:** Identifies the sports that have grown the most in terms of athlete participation and visualizes the evolution of the most popular sports.
* **Gender Evolution:** Analyzes the proportion of athletes by gender in major sports over time (based on historical data).
* **In-depth Analysis of Brazil's Performance:**
    * Brazil's medal count evolution by edition, with a spotlight on Rio 2016.
    * A ranking of the most successful sports for the country.
    * A comparison of performance in team vs. individual sports.
* **Clash of Titans:** A comparative analysis of the historical performance between Brazil and Cuba.
* **The Age of Champions:** A study on the evolution of the average age of Olympic medalists across the decades.

## 🛠️ Technologies Used

* **Language:** Python 3
* **Key Libraries:**
    * Pandas (Data manipulation and analysis)
    * Matplotlib & Seaborn (Data visualization)
    * Kaggle API & KaggleHub (Data ingestion)
    * PyArrow (Reading and writing Parquet files)
* **Environment:** Google Colab (Jupyter Notebook)

## 🗂️ Project Structure (Data Lake)

The project is organized following a Data Lake architecture with three primary layers to ensure data quality and traceability:

```

olympics-datalake/
│
├── raw/
│   \# Raw data, exactly as downloaded from the sources (CSVs, etc.)
│   ├── olympics\_historico\_results.csv
│   ├── olympics\_historico\_bio.csv
│   ├── paris2024\_\*.csv
│   └── \*.json (Metadata describing each data source)
│
├── bronze/
│   \# Cleaned, standardized, and integrated data, ready for analysis (Parquet format)
│   ├── medalhas\_1986\_2024.parquet
│   ├── participantes\_1986\_2024.parquet
│   ├── genero\_historico.parquet
│   └── \*.json (Metadata describing each processed table)
│
└── gold/
\# Final layer with the results of the analyses
├── analise\_medalhas/
│   ├── medalhas\_summary.csv (Summary table)
│   └── medalhas\_plot.png (Generated chart)
│   └── metadata.json
├── ... (other analysis folders)

```

## 🚀 How to Run the Project

To replicate this analysis, follow the steps below:

#### 1. Prerequisites
* A [Kaggle](https://www.kaggle.com/) account.
* A Google account to use [Google Colab](https://colab.research.google.com/).

#### 2. Get Your Kaggle API Key
* Log in to your Kaggle account and navigate to your account settings (`https://www.kaggle.com/settings`).
* In the "API" section, click on **"Create New Token"**.
* This will download a file named `kaggle.json` to your computer. Keep this file handy.

#### 3. Running the Notebook
1.  Open the main notebook from this repository in Google Colab.
2.  Run the initial cells for installation and folder creation.
3.  When you first run **Cell 3**, it will require your `kaggle.json` file. In the left-hand menu of Colab (folder icon), click "Upload" and select the `kaggle.json` file you downloaded.
4.  After the upload is complete, Cell 3 and all subsequent cells will execute successfully, downloading the data and performing all the analyses.

## 📈 Results and Findings

The analysis revealed several interesting trends:
* Brazil's performance shows consistent growth, with a clear peak during the Rio 2016 Olympic Games, suggesting a "home-field advantage."
* The comparison between Brazil and Cuba illustrates a transition of power in Latin America, with Cuba dominating in the late 20th century and Brazil rising since the 2000s.
* The average age of medalists has remained relatively stable over time, with notable variations in specific sports like Artistic Gymnastics (younger athletes) and Equestrianism (older athletes).

## ✍️ Author

* **Caroline Souza**
* **Yara De Oliveira**


``
