# MIMIC-III-BigData-Analytics-Pipeline
# Big Data Project Pipeline

## Overview
This project builds a **batch analytics pipeline** on the **MIMIC-III Clinical Database (Demo v1.4)** using a **Docker-based big data environment**.  
It supports structured querying via **Hive** and parallel analytics using **MapReduce**.

---

## Tech Stack

- ![Docker](https://img.shields.io/badge/Platform-Docker-blue)  ![Hadoop](https://img.shields.io/badge/Framework-Hadoop-orange) ![Hive](https://img.shields.io/badge/Query_Engine-Hive-yellow) ![MapReduce](https://img.shields.io/badge/Compute-MapReduce-red) ![MIMIC-III](https://img.shields.io/badge/Dataset-MIMIC--III-green) 

## Steps

### 1️⃣ Pull Docker Image  
Pulled the required **Docker** image to the local machine.

### 2️⃣ Upload Docker Image  
Uploaded the **Docker** image successfully to the registry.

### 3️⃣ Download Dataset  
Downloaded the dataset for the project from the official source.

### 4️⃣ Select and Clean Data  
Selected 4 main tables from the dataset:
- `ADMISSIONS`
- `diagnoses_icd`
- `icustays`
- `PATIENTS`

Performed data cleaning operations to ensure quality.

### 5️⃣ Save as Parquet Files  
Saved the cleaned tables as **Parquet** files for optimized storage and processing.

### 6️⃣ Upload Parquet Files to Docker  
Uploaded the **Parquet** files to the Docker container using **Git Bash**.

##---------------------------------------------------------------------

<h1 align="center" style="color:#1976D2;">🚀 Big Data Healthcare Analytics Project</h1>

---

## 📊 Project Scope

This project focuses on the **batch processing and analytics of ICU patient data** from the **MIMIC-III Clinical Database** using a **Dockerized big data stack**.  
It is designed for **educational and research purposes**, demonstrating the use of **Hadoop**, **Hive**, and **MapReduce** in healthcare data analytics.

---

## 📌 Tech Stack

| Type          | Tool/Platform |
|:--------------|:---------------|
| ![Docker](https://img.shields.io/badge/Platform-Docker-blue) | Docker |
| ![Hadoop](https://img.shields.io/badge/Framework-Hadoop-orange) | Hadoop |
| ![Hive](https://img.shields.io/badge/Query_Engine-Hive-yellow) | Hive |
| ![MapReduce](https://img.shields.io/badge/Compute-MapReduce-red) | MapReduce |
| ![MIMIC-III](https://img.shields.io/badge/Dataset-MIMIC--III-green) | MIMIC-III |

---

## 🗺️ Project Architecture Overview

| Component  | Description                                      |
|:------------|:------------------------------------------------|
| Docker       | Container orchestration for Hadoop, Hive, and supporting services |
| HDFS         | Distributed storage system                    |
| Hive         | SQL-like querying interface                    |
| MapReduce    | Java-based batch analytics engine               |
| MIMIC-III    | Public ICU dataset for healthcare analytics     |

---

## 📂 Project Directory Structure


---

## ⚙️ Setup Instructions

### 📑 Prerequisites
- **Git Bash** (Windows)
- **Python 3.x** with pip
- **Docker & Docker Compose**
- **Git CLI**
- **MIMIC-III Demo CSV files** in `data/mimiciii/csv/`

---

## 🚀 Step-by-Step Execution

### 📌 Step 1: Install Python Dependencies
```bash
pip install pandas pyarrow



ر
