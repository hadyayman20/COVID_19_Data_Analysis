# 🦠 COVID-19 Global Data Analysis

An exploratory data analysis (EDA) of the global COVID-19 pandemic using the [Our World in Data](https://ourworldindata.org/coronavirus) dataset covering data cleaning, trend analysis, country comparisons, correlation analysis, and interactive choropleth maps.

![Python](https://img.shields.io/badge/python-3.9%2B-blue)
![License](https://img.shields.io/badge/license-MIT-green)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange)

## 📊 Project Overview

The notebook walks through a complete analysis pipeline:

1. **Data Loading & Inspection** — shape, types, missing values
2. **Data Cleaning & Preprocessing** — dropping sparse columns, forward-filling cumulative counters, imputing static country features by median, deriving month/week/death-rate fields
3. **Exploratory Data Analysis** — global and per-country trends, top-10 countries by case count, correlation heatmap, weekly/monthly aggregates
4. **Interactive Choropleth Maps** — world maps of total cases and total deaths by country (Plotly)
5. **Conclusions & Insights** — summary of key findings

## 🔑 Key Insights

- Case totals are heavily concentrated in a handful of highly populous countries (US, India, Brazil), with total cases strongly correlated with population size rather than being a pure measure of outbreak severity.
- Global new deaths peaked in mid-April 2020 and declined afterward even as new cases kept climbing through the following months consistent with expanded testing and improved treatment over time.
- `total_deaths` and `total_cases` are very strongly correlated, as expected.

## 📁 Dataset

This project uses the **Our World in Data COVID-19 dataset** (`owid-covid-data.csv`), included in this repo. It's a snapshot of the OWID data.

## 🚀 Getting Started

### Prerequisites
- Python 3.9+

### Installation
```bash
git clone https://github.com/hadyayman20/covid19-data-analysis.git
cd covid19-data-analysis

python -m venv venv
source venv/bin/activate      # on Windows: venv\Scripts\activate

pip install -r requirements.txt
```

### Run
```bash
jupyter notebook covid19_analysis.ipynb
```

## 🗂️ Project Structure
```
covid19-data-analysis/
├── covid19_analysis.ipynb   # Main analysis notebook
├── owid-covid-data.csv       # Dataset (OWID COVID-19 data)
├── requirements.txt          # Python dependencies
├── LICENSE
├── .gitignore
└── README.md
```

## 🛠️ Built With
- [pandas](https://pandas.pydata.org/) & [NumPy](https://numpy.org/) — data manipulation
- [Matplotlib](https://matplotlib.org/) & [Seaborn](https://seaborn.pydata.org/) — static visualizations
- [Plotly](https://plotly.com/python/) — interactive choropleth maps

## 📄 License
This project is licensed under the MIT License — see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments
Data provided by [Our World in Data](https://ourworldindata.org/coronavirus), based on official sources including the WHO and Johns Hopkins CSSE.
