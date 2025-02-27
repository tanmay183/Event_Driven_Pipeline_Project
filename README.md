# Event-Driven ETL Pipeline

## What is this?
This project is an **Event-Driven ETL Pipeline** built using **Databricks and GCP** to process order data efficiently.

## What do we do in it?
- Read CSV files from Databricks File Store (**DBFS**).
- Load data into a **staging Delta table**.
- Move processed files to an **archive folder**.
- Merge new records into a **target Delta table** while removing duplicates.

## How to Run
1. Upload order CSV files to `/Volumes/incremental_load/default/orders_data/source/`.
2. Run `orders_stage_load.ipynb` to stage and archive files.
3. Run `orders_target_load.ipynb` to merge staged data into the final table.

