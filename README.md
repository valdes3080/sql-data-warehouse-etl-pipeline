# E-Commerce Data Warehouse Pipeline (EcomDW)
Overview

This project demonstrates the design and implementation of a complete end-to-end data engineering pipeline for an e-commerce analytics platform. The system simulates a production-style workflow where raw transactional data is generated, ingested through an ETL pipeline, modeled in a dimensional warehouse, and exposed through business intelligence reports.

The goal of this project is to demonstrate practical experience with data pipeline architecture, dimensional modeling, ETL orchestration, data validation, and analytics reporting.

### Project Architecture

The pipeline transforms generated transactional data into a structured analytics warehouse.

<div align="center">

Python Data Generator  
↓  
CSV Source Files  
↓  
SSIS ETL Pipeline  
↓  
Staging Tables  
↓  
Deduplication View  
↓  
Dimension Upserts  
↓  
Fact Table Load  
↓  
Validation Framework  
↓  
Run Metadata Logging  
↓  
SSRS Reporting Layer  

</div>


### 1️⃣ Warehouse Schema
The warehouse follows a star schema design optimized for analytical workloads.
![Warehouse Schema](EcomDW_Project/Images/EcomDw_Diagram.png)



### 2️⃣ SSIS Control Flow
The ETL pipeline is orchestrated using SQL Server Integration Services (SSIS).
![SSIS Control Flow](EcomDW_Project/Images/SSIS_Control_Flow.png)

# Key Pipline Stages Include:
Pipeline initialization

Staging loads

Dimension upserts

Fact table loading

Validation framework

Execution logging

---

### 3️⃣ Data Flow – File Ingestion
CSV files are processed through an SSIS data flow which performs transformations before loading staging tables.
![DataFlow](EcomDW_Project/Images/"C:\Images\DataFlow_File_Ingestion.png")
