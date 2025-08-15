# Salesforce ETL Pipeline (n8n)

**Tags:** etl, automation, n8n, salesforce, snowflake  
**Tools:** n8n, Salesforce REST API, Snowflake, Kafka (optional), Python (utilities)  
**Timeline:** 2025-08 | **Role:** Solution Developer (POC)

## 1) What this does
Automates extraction of objects from **Salesforce** via REST API, applies basic transforms, and loads curated data into **Snowflake**. Designed as an **n8n** workflow to demonstrate a portable, low-code ETL for CRM analytics and reporting.

## 2) Key artifacts
- `/workflow/salesforce_etl_pipeline_n8n.json` — n8n export (import in n8n → Workflows → Import)
- `/sql/` — DDL & staging queries
- `/screenshots/` — flow overview & node configs

## 3) Highlights
- POC integrates **Salesforce migration via REST** with **Kafka-based ingestion** (optional module)
- Modular nodes for retries, error handling, and secrets via env variables
- Ready to extend for downstream **Tableau/Power BI**

## 4) How to run
1. Import the JSON workflow into your n8n instance.  
2. Set environment variables (SF credentials, Snowflake DSN) or n8n credentials.  
3. Execute or schedule via n8n Cron node.

## 5) Notes & next steps
- Add incremental load (CDC) using `SystemModstamp`  
- Add data quality checks and alerts  
