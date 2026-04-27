**FINTRACK DATA PIPELINE (DATABRICKS + PYSPARK)**

 **Overview**
This project implements a real-time data pipeline using PySpark and Databricks based on the Medallion Architecture (Bronze, Silver, Gold).
The pipeline ingests raw financial transaction data, processes it through multiple layers, and generates aggregated insights for analytics.

**Architecture**

<img width="609" height="943" alt="image" src="https://github.com/user-attachments/assets/1a57bb5d-04ee-46ad-8717-d032358fa2db" />

Bronze Layer → Raw data ingestion (streaming)
Silver Layer → Data cleaning & transformation
Gold Layer → Aggregated insights for business use

**Tech Stack
**
•	PySpark
•	Databricks
•	Delta Lake
•	Structured Streaming
•	Pipeline Workflow

🥉 Bronze (Ingestion)
Reads streaming data using Auto Loader (cloudFiles)
Stores raw data in Delta tables
Handles schema inference and evolution

🥈 Silver (Transformation)
Removes null values
Deduplicates records
Applies basic data validation

🥇 Gold (Aggregation)
Performs business-level aggregations
Generates insights like total transactions, category-wise spend

**Job Execution (Databricks)**

Below shows the pipeline running in Databricks:

<img width="1859" height="475" alt="image" src="https://github.com/user-attachments/assets/cf9ce608-21fd-4892-9d96-108d0a99ac8e" />

✔️ Bronze → Silver → Gold executed successfully
✔️ Streaming ingestion working
✔️ Tables created and updated incrementally

**Sample Output / Visualization**

Example of processed data and insights:

<img width="2212" height="735" alt="image" src="https://github.com/user-attachments/assets/9391da37-893d-43fc-8b75-69f304746b87" />

<img width="1097" height="826" alt="image" src="https://github.com/user-attachments/assets/525b677c-155c-467f-9d1a-3f6a697f20f8" />


Cleaned dataset in Silver layer
Aggregated results in Gold layer
Category-wise analysis of transactions

📁 **Project Structure**

fintrack-project/
│
├── README.md
│
├── notebooks/
│   ├── bronze.ipynb
│   ├── silver.ipynb
│   ├── gold.ipynb
│
└── data/

    
**How to Run
**•	Upload notebooks to Databricks workspace
•	Attach cluster
•	Run in order:
•	bronze.ipynb
•	silver.ipynb
•	gold.ipynb
**
Key Highlights**
•	Real-time data ingestion using streaming
•	Medallion architecture implementation
•	Scalable and modular pipeline design
•	Handles schema evolution and incremental processing

**Author
HariHaran S**
****
