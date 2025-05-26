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




ر
