# Customer Analytics & Revenue Intelligence Platform

A production-grade customer analytics and revenue intelligence project built on the public Online Retail II dataset. This repository packages an end-to-end data analytics workflow for a portfolio-ready 2027 hiring profile, covering ETL, warehouse modeling, business SQL, customer analytics, machine learning, and executive dashboards.

## Executive summary

This project is designed to answer modern retail and subscription-style business questions such as:
- Which customers create the most value?
- Which products drive the most revenue?
- How do customer cohorts behave over time?
- Which customers are at risk of churn?
- What is the projected revenue trajectory?
- Which decision-ready dashboards can help leadership act faster?

## Project scope

- Data ingestion from a public ecommerce dataset
- Medallion architecture: Bronze, Silver, Gold
- Python ETL pipelines for ingestion and transformation
- SQL dimensional modeling
- 40 business SQL queries
- Customer segmentation via RFM
- Cohort analysis
- Customer Lifetime Value (CLV)
- Churn analysis
- Revenue forecasting
- XGBoost churn prediction with SHAP explanations
- Business dashboard artifacts: executive, sales, customer insights
- CI/CD via GitHub Actions
- Docker support
- Portfolio-quality documentation

## Dataset

This project uses the public Online Retail II dataset.

### Download instructions
1. Open the UCI dataset page: https://archive.ics.uci.edu/ml/datasets/Online+Retail+II
2. Download the Excel workbook `online_retail_II.xlsx`
3. Save the file to `data/raw/online_retail_II.xlsx`

Alternative public source: search Kaggle for `Online Retail II` and download a compatible file into the same raw data directory.

## Repository structure

```text
customer-analytics-revenue-intelligence-platform/
├── .github/
│   └── workflows/
│       └── ci.yml
├── dashboard/
│   ├── executive_dashboard.svg
│   ├── sales_dashboard.svg
│   └── customer_insights_dashboard.svg
├── data/
│   ├── README.md
│   ├── raw/
│   ├── bronze/
│   ├── silver/
│   └── gold/
├── docs/
│   ├── architecture.md
│   ├── business_report.md
│   ├── data_dictionary.md
│   └── project_documentation.md
├── notebooks/
│   ├── 01_download_and_explore.ipynb
│   └── 02_eda_and_feature_engineering.ipynb
├── sql/
│   ├── 01_schema.sql
│   ├── 02_dimensional_models.sql
│   ├── 03_business_queries.sql
│   └── README.md
├── src/
│   ├── analytics/
│   │   ├── __init__.py
│   │   ├── rfm.py
│   │   ├── cohort.py
│   │   ├── clv.py
│   │   ├── churn.py
│   │   └── forecasting.py
│   ├── dashboard/
│   │   ├── __init__.py
│   │   └── streamlit_app.py
│   ├── etl/
│   │   ├── __init__.py
│   │   ├── bronze.py
│   │   ├── silver.py
│   │   ├── gold.py
│   │   └── pipeline.py
│   ├── ml/
│   │   ├── __init__.py
│   │   └── churn_model.py
│   ├── config.py
│   └── __init__.py
├── tests/
│   ├── README.md
│   └── test_config.py
├── .gitignore
├── .dockerignore
├── .env.example
├── Dockerfile
├── docker-compose.yml
├── requirements.txt
├── LICENSE
├── README.md
└── .github/workflows/ci.yml
```

## Quick start

```bash
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
python src/etl/pipeline.py
```

## Dashboard

Launch the analytics app:

```bash
streamlit run src/dashboard/streamlit_app.py
```

## Docker

```bash
docker build -t customer-analytics-platform .
docker run -p 8501:8501 customer-analytics-platform
```

Or with Docker Compose:

```bash
docker-compose up --build
```

## Data engineering flow

```text
Raw ecommerce data
        ↓
Bronze layer: raw ingestion + validation
        ↓
Silver layer: dedupe, null repair, type normalization
        ↓
Gold layer: analytics-ready fact/dimension dataset
        ↓
SQL analytics + ML predictions + dashboard reporting
```

## Key analytics modules

- RFM segmentation
- Cohort analysis
- Customer lifetime value
- Churn analysis
- Revenue forecasting
- XGBoost churn prediction
- SHAP explanations

## Core SQL models

- FactSales
- DimCustomer
- DimProduct
- DimDate

## Deliverables included

- End-to-end ETL pipeline in Python
- SQL data model and business queries
- Portfolio-ready business report
- Data dictionary
- Dashboard mockups and vector exports
- Deployment and CI/CD scaffolding
- Project documentation and architecture diagram

## Documentation

- `docs/architecture.md`
- `docs/business_report.md`
- `docs/data_dictionary.md`
- `docs/project_documentation.md`

## License

MIT

## Portfolio note

This project is designed to be interview- and portfolio-ready for senior analyst, analytics engineer, BI, or data science roles in 2027 hiring cycles.
