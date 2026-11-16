# Customer Analytics & Revenue Intelligence Platform

A portfolio-ready, end-to-end customer analytics and revenue intelligence project built on the Online Retail II dataset.

## Overview

This project demonstrates a complete data stack covering data ingestion, data engineering, SQL dimensional modeling, business analytics, ML-driven churn prediction, and executive dashboard storytelling. It is designed to look like a senior analyst or analytics engineer portfolio project for 2027 hiring.

## Scope

- Public ecommerce dataset ingestion and ETL
- Bronze / Silver / Gold medallion architecture
- Fact and dimension tables in SQL
- 40 business SQL queries
- RFM segmentation, cohort analysis, CLV, churn, revenue forecasting
- XGBoost churn prediction with SHAP explanations
- Power BI / dashboard artifacts
- CI/CD with GitHub Actions and Docker support

## Repository layout

```text
.
├── .github/workflows/
├── dashboard/
├── data/
├── docs/
├── notebooks/
├── sql/
├── src/
├── tests/
├── .gitignore
├── Dockerfile
├── README.md
├── docker-compose.yml
├── requirements.txt
├── LICENSE
└── .env.example
```

## Dataset

We use the Online Retail II dataset from UCI.

Download instructions:

1. Visit https://archive.ics.uci.edu/ml/datasets/Online+Retail+II
2. Download `online_retail_II.xlsx`
3. Save to `data/raw/online_retail_II.xlsx`
4. Run the ETL pipeline to transform it into Bronze -> Silver -> Gold layers

## Quick start

```bash
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
python src/etl/pipeline.py
```

## Docker

```bash
docker build -t customer-analytics-platform .
docker run -p 8501:8501 customer-analytics-platform
```

## Documentation

See `docs/` for:
- project documentation
- architecture overview
- data dictionary
- business report

## Key deliverables

- ETL pipelines in Python
- SQL dimensional models
- 40 analytical SQL queries
- RFM analysis and segmentation
- Cohort analysis
- CLV and churn analysis
- revenue forecasting
- churn prediction with XGBoost
- dashboard mockups and design assets
- CI/CD pipeline

## License

MIT
