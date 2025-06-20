# 🔧 Data Engineer Intern Challenge

## 🎯 Objective
Build a complete ETL pipeline that ingests, processes, and serves data via API. Demonstrate your skills in data engineering, pipeline design, and API development.

## 📋 Task Overview
1. **Ingest** a publicly available CSV dataset using PySpark
2. **Process** data with cleaning, deduplication, and feature engineering
3. **Store** cleaned data to local/mock S3 bucket
4. **Serve** data through a FastAPI endpoint
5. **Bonus**: Add Airflow orchestration (mock setup acceptable)

## 📁 Project Structure

### `/data/`
- **`raw_data.csv`** - Your chosen public dataset (download and place here)
- **`processed_data.csv`** - Cleaned output from ETL pipeline
- **`.gitkeep`** - Maintains empty directory in git

### `/src/`
- **`etl_pipeline.py`** - Main PySpark ETL logic with data transformations
- **`data_processor.py`** - Data cleaning functions (null handling, deduplication)
- **`s3_utils.py`** - Mock S3 operations or local storage utilities
- **`config.py`** - Configuration settings (file paths, S3 buckets, etc.)

### `/api/`
- **`main.py`** - FastAPI application entry point
- **`models.py`** - Pydantic models for API request/response schemas
- **`endpoints.py`** - API route definitions and business logic

### `/tests/`
- **`test_etl.py`** - Unit tests for ETL pipeline functions
- **`test_api.py`** - API endpoint testing
- **`test_data_processor.py`** - Data processing function tests
- **`conftest.py`** - Pytest configuration and fixtures

## 🚀 Getting Started

1. **Setup Environment**
   ```bash
   python -m venv venv
   source venv/bin/activate  # Windows: venv\Scripts\activate
   pip install -r requirements.txt
   ```

2. **Run ETL Pipeline**
   ```bash
   python src/etl_pipeline.py
   ```

3. **Start API Server**
   ```bash
   uvicorn api.main:app --reload
   ```

4. **Run Tests**
   ```bash
   pytest tests/
   ```

## 📊 Dataset Requirements
Choose a CSV dataset with:
- 1000+ records
- Multiple columns (numerical + categorical)
- Some data quality issues (nulls, duplicates)

**Suggested sources**: Kaggle, UCI ML Repository, government open data

## ✅ Expected Deliverables

1. **Working ETL pipeline** that processes your chosen dataset
2. **FastAPI endpoint** returning sample records: `GET /data/sample?limit=10`
3. **Clean, documented code** with proper error handling
4. **Test coverage** for key functions
5. **Updated `submission.md`** explaining your approach and decisions

## 🎯 Evaluation Focus
- **Data pipeline design** and PySpark usage
- **API development** best practices
- **Code quality** and testing
- **Documentation** and clarity

## 💡 Bonus Points
- Airflow DAG setup (even mock configuration)
- Docker containerization
- Data validation checks
- Performance optimizations

---

**Time Estimate**: 4-6 hours | **Due**: June 26, 2025, 11:59 PM IST
