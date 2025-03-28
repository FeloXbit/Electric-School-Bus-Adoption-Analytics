# ETL Pipeline Project

## Problem Description

In modern data-driven environments, businesses rely on timely and well-structured data to make informed decisions. However, raw data is often scattered across various sources, requiring extraction, transformation, and loading (ETL) processes to consolidate and optimize it for analytics.

This project aims to build an end-to-end ETL pipeline using batch processing to move data from an external API source to Google Cloud Platform (GCP), process and store it efficiently in BigQuery, transform it with dbt, and visualize insights in a dashboard.

## Business Impact

By implementing this ETL pipeline, organizations can:

- **Automate data ingestion** from APIs, reducing manual effort.
- **Improve data accessibility** by storing structured data in BigQuery.
- **Enhance decision-making** through real-time insights from a visual dashboard.
- **Optimize costs** by leveraging cloud-native solutions and scalable data pipelines.

## Technologies Used

- **Cloud Platform:** Google Cloud Platform (GCP)
- **Orchestration:** Kestra
- **Storage:** Google Cloud Storage (GCS)
- **Data Warehouse:** BigQuery
- **Transformations:** dbt (Data Build Tool)
- **Visualization:** Looker / Tableau
- **Version Control:** GitHub

## Dataset: Electric School Bus Adoption in the United States

This dataset tracks electric school bus (ESB) adoption across the United States. It captures:

- The number of **committed** ESBs at the school district level.
- Details about individual buses, including **manufacturer and funding sources**.
- The timeline of ESB adoption phases and their current status.
- Socio-economic characteristics such as **poverty rates, racial composition, and air pollution levels**.

### Data Source:
- [Dataset Link] [(https://datasets.wri.org/datasets/electric-school-bus-adoption?map=eyJ2aWV3U3RhdGUiOnsibGF0aXR1ZGUiOjAsImxvbmdpdHVkZSI6MCwiem9vbSI6M30sImJhc2VtYXAiOiJsaWdodCIsImxhYmVscyI6ImRhcmsiLCJhY3RpdmVMYXllckdyb3VwcyI6W10sImxheWVyc1BhcnNlZCI6W119)]

### ETL Processing Steps:
1. **Ingestion:** Extract data from the source API and store it in Google Cloud Storage (GCS).
2. **Processing:** Load raw data into BigQuery and apply necessary transformations.
3. **Transformation:** Use dbt to model and clean the data for analytics.
4. **Visualization:** Create interactive dashboards in Looker/Tableau to display insights.

## Repository Structure

```
📂 etl-pipeline
 ┣ 📂 data_ingestion
 ┃ ┣ 📜 fetch_data.py  # Python script to extract data from API
 ┃ ┣ 📜 upload_to_gcs.py  # Script to upload data to Google Cloud Storage
 ┃ ┗ 📜 Dockerfile  # Docker setup for ingestion step
 ┣ 📂 transformations
 ┃ ┣ 📜 dbt_project/  # Contains dbt models & configurations
 ┃ ┣ 📜 transform.sql  # SQL script for initial transformations
 ┃ ┗ 📜 Dockerfile  # Docker setup for transformations
 ┣ 📂 dashboards
 ┃ ┣ 📜 dashboard.looker  # Looker dashboard config (if using Looker)
 ┃ ┣ 📜 tableau_dashboard.twbx  # Tableau workbook (if using Tableau)
 ┃ ┗ 📜 README.md  # Instructions for setting up dashboards
 ┣ 📜 README.md  # Project documentation
 ┣ 📜 kestra_workflow.yaml  # ETL workflow definition for Kestra
 ┣ 📜 requirements.txt  # Python dependencies
 ┣ 📜 docker-compose.yaml  # Docker Compose file to manage containers
 ┣ 📜 .env  # Environment variables (API keys, credentials)
 ┗ 📜 .gitignore  # Ignore unnecessary files

```

## How to Run

1. Clone the repository:
   ```sh
   git clone https://github.com/FeloXbit/Electric-School-Bus-Adoption-Analytics.git
   cd etl-pipeline-project
   ```
2. Install required dependencies:
   ```sh
   pip install -r requirements.txt
   ```
3. Deploy the Kestra workflow:
   ```sh
   kestra deployment apply kestra_workflow.yaml
   ```
4. View processed data in BigQuery and analyze insights in the dashboard.

---



