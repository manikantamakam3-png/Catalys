Architecture Diagram:
<img width="737" height="593" alt="image" src="https://github.com/user-attachments/assets/d8f4e149-98b1-4a61-9c5a-79ce570a1d64" />

1️⃣ Raw Notebook

Reads source files (CSV & JSON)

Loads data into raw storage

No transformations applied

2️⃣ Curated Notebook

Cleans data

Removes duplicates

Handles null values

Standardizes schema

3️⃣ Consumption Notebook

Joins player and match data

Performs aggregations:

Total runs

Total wickets

Player performance metrics

4️⃣ Run Notebook

Orchestrates execution of:

Raw → Curated → Consumption

Ensures dependency order


🧾 Sample Transformations

Deduplication using window functions

Aggregation using GROUP BY

Joins between fact and dimension tables

✅ Data Quality Checks

Null value validation

Duplicate record removal

Schema validation

Basic consistency checks

🔧 Technologies Used

Databricks (PySpark + SQL)

ADLS (Storage)

CSV & JSON data formats

▶️ How to Run

Upload sample data to storage

Import notebooks into Databricks

Execute the run notebook

Verify output in consumption layer

⚠️ Assumptions

Source data is available and accessible

Schema changes are minimal or controlled

Data volume is moderate (not large-scale production)

Player IDs are consistent across datasets

🚧 Limitations

No real-time/streaming ingestion

Limited error handling for corrupted files

No advanced data validation rules

No automated alerting system

Performance tuning is basic (not optimized for large data)

❗ Exceptions & Error Handling

Missing or null critical fields are filtered out

Duplicate records are handled using window functions

Schema mismatches may cause pipeline failure

Invalid records are currently not stored separately (can be enhanced)
