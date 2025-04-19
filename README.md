# Azure Synapse Analytics - Learning Log

This repository contains my notes and experiences while exploring **Azure Synapse Analytics**, a cloud-based data analytics and integration service. Synapse combines big data, data warehousing, and ETL pipelines to enable seamless querying and transformation of both structured and unstructured data in a unified environment.

## 🚀 Key Learnings

### 1. **Overview of Azure Synapse Analytics**
Azure Synapse Analytics is an integrated platform designed for enterprise-level data warehousing, big data analytics, and data integration. It allows users to perform data queries using SQL, Spark, and Data Factory pipelines within a single workspace, enabling seamless data workflows across different data sources.

### 2. **Data Storage & Configuration**
- **Azure Data Lake Storage**: Azure Synapse uses **Azure Data Lake Storage Gen2** for data and metadata storage. Each workspace is linked to a default Data Lake storage account, but external storage accounts can also be connected.
- **Table Distribution Strategies**: To optimize data processing, Synapse supports three distribution strategies:
  - **Hash-distributed**: Best for large fact tables where data is evenly distributed for efficient joins.
  - **Round-robin**: Distributes rows randomly, suited for staging or intermediate tables.
  - **Replicated**: Creates full copies of small dimension tables across all distributions to minimize data shuffle during joins.

### 3. **SQL & Data Querying**
- **Serverless SQL Pools**: Allows querying of data directly from the data lake without moving data, utilizing both **managed tables** (data and metadata managed by Synapse) and **external tables** (metadata managed by Synapse, but data resides in external storage).
- **OPENROWSET Queries**: Enables querying of external data in formats like CSV and Parquet from the Azure Data Lake using serverless SQL.
- **External Tables & Views**: Learn how to create and use external tables and views for direct querying from external data sources.

### 4. **Data Loading & Integration**
- **Loading Parquet Data**: I learned how to use the `COPY INTO` statement and **PolyBase** to load Parquet data from external sources into dedicated SQL pools for efficient querying.
- **Azure Data Factory Integration**: Azure Synapse integrates with **Azure Data Factory** for orchestrating ETL pipelines, allowing the automation of data workflows.
- **Apache Spark Pools**: Synapse provides scalable Spark Pools to run big data jobs using PySpark or Scala, suitable for large-scale data processing tasks.

### 5. **Security & Data Access**
- **Managed Identity & Linked Services**: For secure access to external data, I learned how to use **Managed Identity** with **Linked Services** in Synapse, providing a secure way to authenticate and connect to external Azure storage accounts like Azure Data Lake.

---

## 🛠️ Setup & Usage

To start working with **Azure Synapse Analytics** in your own projects, follow these steps:

1. **Set up an Azure Synapse Workspace**:
   - Create a new Synapse workspace in the Azure portal.
   - Link the workspace to Azure Data Lake Storage (either the default or external storage account).
   
2. **Create Tables & Distribute Data**:
   - Create tables with different distribution strategies (e.g., hash-distributed, round-robin, replicated).
   
3. **Query Data Using SQL**:
   - Use **serverless SQL pools** to directly query data stored in your Data Lake.
   - Use **OPENROWSET** for querying external data files (e.g., CSV, Parquet).
   
4. **Integrate with Data Factory**:
   - Build and orchestrate ETL pipelines using **Azure Data Factory** integration with Synapse.
   
5. **Secure Data Access**:
   - Set up **Managed Identity** and **Linked Services** to securely connect to external data sources like Azure Data Lake.

---

## 📚 Additional Resources

To further explore **Azure Synapse Analytics**, here are some helpful links:

- [Azure Synapse Documentation](https://learn.microsoft.com/en-us/azure/synapse-analytics/)
- [Azure Data Factory Documentation](https://learn.microsoft.com/en-us/azure/data-factory/)
- [Apache Spark Pools in Synapse](https://learn.microsoft.com/en-us/azure/synapse-analytics/spark/apache-spark-pools)

---

## 📬 Contact
For questions or collaborations:  
**📧 Email:** rare.girald@gmail.com
**🔗 LinkedIn:** https://www.linkedin.com/in/girald-bacongan-988144174/



