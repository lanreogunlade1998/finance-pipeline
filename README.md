# finance-pipeline
End-to-end data pipeline for stock trading analytics using Databricks
# 📊 Finance Trading Data Pipeline

[![Databricks](https://img.shields.io/badge/Databricks-FF3621?style=for-the-badge&logo=databricks&logoColor=white)](https://databricks.com/)
[![Azure](https://img.shields.io/badge/Azure-0078D4?style=for-the-badge&logo=microsoftazure&logoColor=white)](https://azure.microsoft.com/)
[![Apache Spark](https://img.shields.io/badge/Apache_Spark-E25A1C?style=for-the-badge&logo=apachespark&logoColor=white)](https://spark.apache.org/)
[![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)

## 📌 Project Overview

**A complete end-to-end data pipeline built on Databricks and Azure for stock trading analytics.**

This project demonstrates a production-ready data engineering solution that processes user registration, profile updates, trade transactions, and trading session data. It follows the **Medallion Architecture** (Bronze → Silver → Gold) to transform raw data into actionable business intelligence.

---

## 🎯 Business Problem

A stock trading platform needs to:
- Ingest and process millions of trades daily
- Track user profiles and their changes over time
- Monitor trading sessions across multiple exchanges
- Generate business insights for stakeholders

**The Solution:** A scalable, cloud-native data pipeline that transforms raw trading data into clean, aggregated business intelligence ready for dashboards and reporting.

---

## 🏗️ Architecture

### Medallion Layer Architecture

<img width="2720" height="3040" alt="finance_pipeline_detailed_architecture" src="https://github.com/user-attachments/assets/8c46a88c-1382-47d7-a93f-ac206c7d00bb" />



## 🛠️ Technologies Used

| Category | Technology |
|----------|------------|
| **Cloud Platform** | Microsoft Azure (Data Lake Storage Gen2) |
| **Data Processing** | Databricks + Apache Spark (PySpark) |
| **Storage Format** | Parquet (columnar storage) |
| **Data Modeling** | Star Schema (Dimensions & Facts) |
| **Version Control** | Git + GitHub |
| **Languages** | Python, SQL |

---

## 📂 Repository Structure
<img width="2830" height="1680" alt="finance_pipeline_repo_structure" src="https://github.com/user-attachments/assets/68e960af-e295-4add-afa3-26ee0948f4e0" />


## 📊 Data Model

### Dimension Tables
| Table | Description | Fields |
|-------|-------------|--------|
| **dim_users** | User information (deduplicated) | user_id, name, age, location |
| **dim_securities** | Stock reference data | symbol, company_name, exchange, sector |

### Fact Tables
| Table | Description | Fields |
|-------|-------------|--------|
| **fact_trades** | Trade transactions | user_id, symbol, action, quantity, price, value |
| **fact_sessions** | Trading sessions | mac_address, exchange, start_time, duration |

---

## 📈 Business Insights Generated

### 1. Portfolio Performance
- Track each user's holdings
- Calculate current portfolio value
- Monitor average entry prices

### 2. Trading Volume Analysis
- Most actively traded stocks
- Buy vs sell distribution
- Exchange comparison (NASDAQ vs NYSE)

### 3. User Activity Metrics
- Identify top traders
- Trading patterns and behavior
- Session engagement analytics

### 4. Market Insights
- Sector performance trends
- Stock price movement tracking
- Exchange trading volume comparison

---

## 🚀 Key Features

| Feature | Description |
|---------|-------------|
| **CDC Processing** | Handles Change Data Capture for user profile updates |
| **Data Deduplication** | Window functions to keep only the latest user profiles |
| **Star Schema** | Clean dimensional modeling for efficient querying |
| **Parquet Storage** | Columnar storage for better compression and performance |
| **End-to-End Pipeline** | From raw ingestion to business-ready aggregations |

---

## 💡 What I Learned

### Technical Skills
✅ Building scalable data pipelines with Databricks and Spark  
✅ Processing nested JSON structures  
✅ Implementing CDC (Change Data Capture) logic  
✅ Designing Star Schema dimensional models  
✅ Transforming data through Medallion Architecture  

### Business Skills
✅ Understanding financial trading data flows  
✅ Creating business intelligence for decision making  
✅ Building reproducible, documented projects  

---

## 🔧 How to Run This Project

### Prerequisites
- Databricks workspace
- Azure Storage Account
- GitHub account

### Setup
1. Clone this repository
2. Upload notebooks to Databricks
3. Configure Azure storage connection
4. Run notebooks in order:
   - `01_Bronze_Ingestion`
   - `02_Silver_Transformations`
   - `03_Gold_Aggregations`

---

## 📈 Results Summary

| Metric | Results |
|--------|---------|
| **Users Processed** | 5 |
| **Trades Analyzed** | 16 |
| **Portfolio Holdings** | 8 |
| **Stocks Tracked** | 9 |
| **Exchanges Covered** | 2 (NASDAQ, NYSE) |

---

## 🎯 Future Enhancements

- [ ] Automate pipeline with Databricks Jobs
- [ ] Create interactive dashboard with Power BI
- [ ] Add data quality checks (Great Expectations)
- [ ] Implement incremental loading for scaling
- [ ] Add more data sources (market data, news feeds)

---

## 🤝 Connect With Me

[![GitHub](https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/lanreogunlade1998)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/)
[![Email](https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:your.email@example.com)

---

## 📅 Project Timeline

| Phase | Duration |
|-------|----------|
| **Bronze Layer** | 30 minutes |
| **Silver Layer** | 45 minutes |
| **Gold Layer** | 30 minutes |
| **Documentation** | 20 minutes |
| **Total** | ~2 hours |

---

## 📚 References

- [Databricks Documentation](https://docs.databricks.com/)
- [Apache Spark Guide](https://spark.apache.org/docs/latest/)
- [Azure Data Lake Storage](https://learn.microsoft.com/en-us/azure/storage/blobs/)
- [Medallion Architecture](https://www.databricks.com/glossary/medallion-architecture)

---

## ⭐️ Support This Project

If you found this project helpful:
- ⭐ Star the repository on GitHub
- 🔗 Share it with your network
- 💬 Provide feedback or suggestions

---

## 📄 License

This project is for educational purposes.

---

## 👨‍💻 Author

**Ige Ogunlade**  
Data Engineering Bootcamp Student  
[GitHub](https://github.com/lanreogunlade1998)

---

**Built with ❤️ during the Databricks Data Engineering Bootcamp** 🚀

---

*Last Updated: June 2026*
