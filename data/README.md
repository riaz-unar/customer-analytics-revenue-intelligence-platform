# Dataset

Download the UCI Online Retail II workbook from https://archive.ics.uci.edu/dataset/502/online+retail+ii and place it at `data/raw/online_retail_II.xlsx`. The original dataset is not committed; it is large and subject to its source terms. To use another compatible public ecommerce extract, provide a CSV or Excel file with invoice, stock code, description, quantity, invoice date, price, customer ID, and country columns (common UCI column names are normalized by the pipeline).

Run `python -m src.etl.pipeline --input data/raw/online_retail_II.xlsx`. Parquet outputs are written to `data/bronze`, `data/silver`, and `data/gold` and are intentionally gitignored.
