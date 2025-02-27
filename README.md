```markdown
# Event-Driven ETL Pipeline using Databricks and GCP

## What is this?
This is an **ETL pipeline** that processes order data using **Databricks and Delta Lake**. It loads, transforms, and merges data efficiently while handling duplicates.

## What we do in it?
1. **Load Data**: Read order CSV files from **Databricks File Store (DBFS)**.
2. **Stage Data**: Store raw data in a **staging Delta table (`orders_stage`)**.
3. **Process Data**: Move processed files to an **archive folder**.
4. **Merge Data**: Upsert new records into the **final Delta table (`orders_target`)**.

## How to Run?
1. Upload CSV files to `/Volumes/incremental_load/default/orders_data/source/`.
2. Run `orders_stage_load.ipynb` to stage data.
3. Run `orders_target_load.ipynb` to merge data into the final table.


```

