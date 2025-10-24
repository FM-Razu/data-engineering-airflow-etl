# 🚀 Supermarket Sales ETL with Apache Airflow

This project builds an **ETL pipeline** to extract, transform, and load supermarket sales data into a **PostgreSQL database** using **Apache Airflow** running in Docker.

---

## 🧩 Project Overview

- **Extract**: Pulls CSV data from Plotly’s public dataset.  
- **Transform**: Cleans and standardizes the data.  
- **Load**: Inserts into PostgreSQL staging and star-schema (fact/dim) tables.

---

## ⚙️ Setup Instructions

### 1. Clone this repository
```bash
git clone https://github.com/<FM-Razu>/airflow-supermarket-etl.git
cd airflow-supermarket-etl
```

### 2. Build Airflow image
```bash
docker build -t airflow:2.8.2 .
```

### 3. Start the containers
```bash
docker compose up
```

### 4. Access Airflow UI
Go to 👉 **http://localhost:8080**  
(Default login: `airflow` / `airflow`)

---

## 🧠 DAG Details

The DAG file is located at `airflow/dags/etl_supermarket_sales_Final-Assignment_by_fahim.py`.

Tasks:
1. **Extract Data**
2. **Transform Data**
3. **Load Clean Data to Staging**
4. **Create Dimension and Fact Tables**
5. **Load Fact and Dimension Tables**

---

## 🛢️ Database

- Host: `postgres`
- Port: `5432`
- DB: `airflow`
- User/Pass: `airflow`

---

## 🧾 Requirements

- Docker
- Docker Compose

---

## 📸 Preview
- Airflow Web UI running at port 8080
- PostgreSQL container for warehouse
