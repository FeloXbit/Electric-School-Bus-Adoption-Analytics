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
- [Dataset Link] (Provide the actual link here)

### ETL Processing Steps:
1. **Ingestion:** Extract data from the source API and store it in Google Cloud Storage (GCS).
2. **Processing:** Load raw data into BigQuery and apply necessary transformations.
3. **Transformation:** Use dbt to model and clean the data for analytics.
4. **Visualization:** Create interactive dashboards in Looker/Tableau to display insights.

## Repository Structure

```
📂 etl-pipeline-project
 ┣ 📂 data_ingestion
 ┣ 📂 transformations
 ┣ 📂 dashboards
 ┣ 📜 README.md  # Project documentation
 ┣ 📜 kestra_workflow.yaml  # ETL workflow definition
 ┗ 📜 requirements.txt  # Dependencies
```

## How to Run

1. Clone the repository:
   ```sh
   git clone https://github.com/your-username/etl-pipeline-project.git
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



