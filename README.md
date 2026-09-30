
```markdown
# 📊 Market Trend & Sentiment Analysis

An automated Data Analytics & Machine Learning Pipeline for product market trend evaluation, customer review sentiment classification, and sales correlation modeling. Built on Python data processing and Jupyter Notebook workflows, this system analyzes product performance across categories, extracts sentiment metrics from review datasets, and evaluates the impact of customer perception on sales trajectories.

---

## 📌 Features & Architecture

```text
[Raw Review & Sales Datasets]
           │
           ▼
┌───────────────────────────────┐
│   Data Cleaning & Ingestion   │ ──► Normalized Tables, Filtered Sub-categories
└───────────────────────────────┘
           │
           ▼
┌───────────────────────────────┐
│  Sentiment Analysis Engine    │ ──► Polarity Scores, Subjectivity, Subject Categories
└───────────────────────────────┘
           │
           ▼
┌───────────────────────────────┐
│   Market Trend Analytics      │ ──► Growth Vectors, Stationary/Declining Segments
└───────────────────────────────┘
           │
           ▼
┌───────────────────────────────┐
│  Sales Correlation Dashboard  │ ──► Sentiment vs. Revenue Metrics & Output Reports
└───────────────────────────────┘

```

* **Market Trend Modeling**: Aggregates multi-file time-series data (`a1.xlsx` – `a81.xlsx`) to classify growing, stationary, and declining product segments.
* **Sentiment Classification**: Employs Natural Language Processing (NLP) to process batch customer reviews and output granular polarity scores (positive, neutral, negative).
* **Sentiment-to-Sales Correlation**: Maps shifts in customer sentiment directly against sales volume to measure feedback impact on market performance.
* **Checkpoint Data Architecture**: Utilizes modular CSV checkpoints (`df-checkpoint.csv`) to manage intermediate data states efficiently during execution.

---

## 📊 Dataset & Processing Summary

* **Primary Source**: Integrated multi-sheet market trend and review log datasets (`Final Trend analysis(...).xlsx`, `b.xlsx`).
* **Sub-category Coverage**: 81 individual item tracking spreadsheets (`a1.xlsx` through `a81.xlsx`).
* **Checkpoint Pipeline**: 14 intermediate execution states (`df1` to `df14`) for reproducible data processing.

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

# Activate environment (Windows)
.\venv\Scripts\activate  

# Activate environment (Linux/macOS)
source venv/bin/activate

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

```

```
