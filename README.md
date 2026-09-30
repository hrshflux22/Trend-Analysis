
# 📈 Market Trend & Sentiment Analysis AI: Retail Perception & Sales Forecasting Pipeline

[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://www.python.org/)
[![Jupyter](https://img.shields.io/badge/Jupyter-Lab-F37626.svg)](https://jupyter.org/)
[![Pandas](https://img.shields.io/badge/Pandas-1.5+-150458.svg)](https://pandas.pydata.org/)
[![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-Latest-F7931E.svg)](https://scikit-learn.org/)

An automated **Data Analytics & Machine Learning Pipeline** for product market trend evaluation, customer review sentiment classification, and sales correlation modeling. Built on Python processing workflows, this system analyzes multi-category product performance, extracts NLP sentiment metrics from review datasets, and evaluates the direct impact of customer perception on sales trajectories.

---

## 📌 Features & Architecture

```text
[Raw Review & Multi-Sheet Datasets]
           │
           ▼
┌───────────────────────────────┐
│   Data Ingestion & Cleaning   │ ──► Preprocessed Tables, Segmented Categories
└───────────────────────────────┘
           │
           ▼
┌───────────────────────────────┐
│  Sentiment Analysis Engine    │ ──► Polarity Scores, Subjectivity, Tone Metrics
└───────────────────────────────┘
           │
           ▼
┌───────────────────────────────┐
│   Market Trend Analytics      │ ──► Growth Vectors, Stationary/Declining Segments
└───────────────────────────────┘
           │
           ▼
┌───────────────────────────────┐
│  Sales Correlation Dashboard  │ ──► Sentiment vs. Revenue Signals & Correlation Reports
└───────────────────────────────┘
```

1. **Market Trend Modeling**: Aggregates multi-file time-series data across 81 sub-category sheets (`a1.xlsx` – `a81.xlsx`) to classify growing, stationary, and declining product lines.
2. **Sentiment Classification**: Employs Natural Language Processing (NLP) to evaluate batch customer reviews and derive polarity and subjectivity metrics.
3. **Sentiment-to-Sales Correlation**: Maps customer feedback shifts directly against sales trajectories using statistical correlation models to project revenue impact.
4. **Checkpoint Architecture**: Leverages modular CSV checkpoints (`df-checkpoint.csv`, `df1`–`df14`) to ensure reproducible pipeline stages and fast data recovery.
5. **Interactive Notebook Workflow**: Modularized Jupyter Notebooks dedicated to specific analytical stages from raw data ingestion to final sales impact output.


## 📊 Dataset & Processing Summary

* **Primary Source**: Integrated market trend tracking sheets (`Final Trend analysis(...).xlsx`, `b.xlsx`)
* **Sub-category Coverage**: 81 individual product tracking spreadsheets (`a1.xlsx` through `a81.xlsx`)
* **Pipeline Checkpoints**: 14 intermediate execution states (`df1` to `df14`)

### Pipeline Module Overview

| Notebook / Module | Primary Function | Core Metrics / Output | Status |
| --- | --- | --- | --- |
| `Trend_Analysis.ipynb` | Exploratory Trend Analysis | Normalized Sales & Segment Growth | Complete |
| `Sentiment_Analysis.ipynb` | Sentiment Classification | Polarity Scores & Tone Metrics | Complete |
| `Multiple Reviews.ipynb` | Batch Review Processing | Multi-item Review Summaries | Complete |
| `sentiment_sales_analysis(actual).ipynb` | Sentiment vs. Revenue Mapping | Pearson Correlation & Demand Signals | Complete |
| `Usage_and_market_trend_analysis(actual).ipynb` | Usage & Adoption Analytics | Long-term Trend Trajectories | Complete |

---

## ⚡ Quick Start (Local Run)

### 1. Clone & Set Up Virtual Environment

```bash
git clone [https://github.com/your-username/Trend-Analysis-main.git](https://github.com/your-username/Trend-Analysis-main.git)
cd Trend-Analysis-main

# Activate environment
.\venv\Scripts\activate  # Windows
source venv/bin/activate # Linux/Mac

```

### 2. Install Dependencies

```bash
pip install pandas numpy matplotlib seaborn nltk scikit-learn openpyxl jupyter

```

### 3. Run Pipeline Notebooks

```bash
# Launch Jupyter Environment
jupyter notebook

# 1. Exploratory Data Cleaning & Baseline Trends
# Open and run: Trend_Analysis.ipynb

# 2. Extract Sentiment Metrics from Review Sets
# Open and run: Sentiment_Analysis.ipynb

# 3. Process Batch Reviews
# Open and run: Multiple Reviews.ipynb

# 4. Correlate Sentiment Metrics with Sales Output
# Open and run: sentiment_sales_analysis(actual).ipynb

# 5. Generate Usage and Market Trend Analysis
# Open and run: Usage_and_market_trend_analysis(actual).ipynb

```

---

## 📁 Repository Structure

```text
Trend-Analysis-main/
├── CSV and Excel Files/             # Raw and processed datasets
│   ├── Final Trend analysis(...).xlsx
│   ├── a1.xlsx - a81.xlsx           # Sub-category datasets
│   └── b.xlsx                       # Consolidated metric input
├── Market_Trend_analysis.ipynb      # Main market trend evaluation
├── Sentiment_Analysis.ipynb         # Sentiment classification model
├── Trend_Analysis.ipynb             # Exploratory data analysis
├── Usage_and_market_trend_analysis(actual).ipynb # Usage trend correlation
├── sentiment_sales_analysis(actual).ipynb        # Sentiment vs. sales correlation
├── Multiple Reviews.ipynb           # Batch customer review processing
├── df-checkpoint.csv                # Pipeline state checkpoints
└── README.md

```

---

## ☁️ Deployment & Execution Notes

1. Ensure all datasets under `CSV and Excel Files/` maintain their exact file names and sheet structures prior to executing pipeline notebooks.
2. If expanding dataset coverage, append additional product files (`a82.xlsx`, etc.) into `CSV and Excel Files/` and update path configurations inside `Market_Trend_analysis.ipynb`.
3. Intermediate data stages are continuously saved into `df-checkpoint.csv` to allow execution recovery without reprocessing entire historical review logs.

```

```
