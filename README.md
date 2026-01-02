# FMCG Delta Medallion Pipeline

A scalable data pipeline implementing the medallion architecture (Bronze → Silver → Gold) using Databricks and Delta Lake for FMCG (Fast-Moving Consumer Goods) data processing, supporting both batch and incremental load patterns.

## 📋 Table of Contents

- [Overview](#overview)
- [Architecture](#architecture)
- [Features](#features)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Usage](#usage)
- [Pipeline Stages](#pipeline-stages)
- [Configuration](#configuration)
- [Project Structure](#project-structure)
- [Contributing](#contributing)
- [License](#license)

## 🎯 Overview

This project demonstrates a production-ready data pipeline built on the medallion architecture pattern, specifically designed for FMCG industry data processing. The pipeline ingests raw data, applies transformations, and produces analytics-ready datasets using Delta Lake's powerful capabilities.

## 🏗️ Architecture

The pipeline follows the medallion architecture with three distinct layers:

```
┌─────────────┐     ┌─────────────┐     ┌─────────────┐
│   Bronze    │ --> │   Silver    │ --> │    Gold     │
│   (Raw)     │     │ (Cleaned)   │     │ (Curated)   │
└─────────────┘     └─────────────┘     └─────────────┘
```

- **Bronze Layer**: Raw data ingestion with minimal transformation
- **Silver Layer**:  Cleaned, validated, and deduplicated data
- **Gold Layer**: Business-level aggregations and analytics-ready datasets

## Features

- **Dual Load Patterns**: Support for both batch and incremental data loading
- **Delta Lake Integration**:  ACID transactions and time travel capabilities
- **Scalable Processing**: Leverages Databricks for distributed computing
- **Data Quality**:  Built-in validation and data quality checks
- **Schema Evolution**: Automatic schema handling and evolution

## 🛠️ Prerequisites

- **Databricks Workspace**: Runtime 11.3 LTS or higher
- **Azure/AWS/GCP Account**: For cloud storage (ADLS Gen2, S3, or GCS)
- **Python**: 3.8 or higher
- **Apache Spark**: 3.3 or higher (included in Databricks)
- **Delta Lake**: 2.0 or higher (included in Databricks)

## 📦 Installation

1. **Clone the repository**:
   ```bash
   git clone https://github.com/vinaldsz/fmcg-delta-medallion-pipeline.git
   cd fmcg-delta-medallion-pipeline
   ```

2. **Set up Databricks workspace**:
   - Import notebooks to your Databricks workspace
   - Configure cluster with appropriate libraries

3. **Configure storage paths**:
   - Update configuration files with your storage account details
   - Set up access credentials (Service Principal, Access Keys, etc.)

   ```


## 🔄 Pipeline Stages

### Bronze Layer
- Ingests raw CSV/JSON/Parquet files from source systems
- Minimal schema enforcement
- Preserves original data format
- Adds metadata columns (ingestion timestamp, source file, etc.)

### Silver Layer
- Data cleansing and standardization
- Duplicate removal
- Data type conversions
- Business rule validations

### Gold Layer
- Business-level aggregations
- Dimensional models
- KPI calculations
- Pre-joined tables for reporting
- Optimized for query performance


## 🤝 Contributing

Contributions are welcome! Please follow these steps: 

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 📞 Contact

**Vinal Dsouza** - [@vinaldsz](https://github.com/vinaldsz)

Project Link: [https://github.com/vinaldsz/fmcg-delta-medallion-pipeline](https://github.com/vinaldsz/fmcg-delta-medallion-pipeline)

## 🙏 Acknowledgments

- [Databricks](https://databricks.com/) for the platform
- [Delta Lake](https://delta.io/) for the storage layer
- [Codebasics.io](https://www.youtube.com/watch?v=U6ZUKWdfSLY) for tutorial
- The data engineering community for best practices and patterns

---

⭐ Star this repository if you find it helpful! 
```
