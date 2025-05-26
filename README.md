# MIMIC-III-BigData-Analytics-Pipeline
# Big Data Project Pipeline

## Overview
This project builds a **batch analytics pipeline** on the **MIMIC-III Clinical Database (Demo v1.4)** using a **Docker-based big data environment**.  
It supports structured querying via **Hive** and parallel analytics using **MapReduce**.

---

## Tech Stack

- ![Docker](https://img.shields.io/badge/Platform-Docker-blue)-- ![Hadoop](https://img.shields.io/badge/Framework-Hadoop-orange)-- ![Hive](https://img.shields.io/badge/Query_Engine-Hive-yellow)--![MapReduce](https://img.shields.io/badge/Compute-MapReduce-red)--![MIMIC-III](https://img.shields.io/badge/Dataset-MIMIC--III-green)--

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

---

## Notes  
- Ensure **Docker** is running before transferring files.
- Use commands like `docker cp` to copy files into the container.

---

## Final Note  
Best of luck with your analytics pipeline! 🚀

# Big Data Project Pipeline

## Overview
This project focuses on processing and analyzing large-scale medical datasets using Docker and efficient data storage formats like Parquet.

---

## Steps

### 1. Pull Docker Image  
First, the required Docker image was pulled to the local machine.

### 2. Upload Docker Image  
The Docker image was uploaded successfully to the registry.

### 3. Download Dataset  
The dataset for the project was downloaded from the specified source.

### 4. Select and Clean Data  
Four main tables were selected from the dataset:  
- `ADMISSIONS`  
- `diagnoses_icd`  
- `icustays`  
- `PATIENTS`  

These tables underwent a thorough cleaning process to ensure data quality and usability.

### 5. Save as Parquet Files  
After cleaning, the tables were saved in **Parquet** format to optimize loading and processing performance.

### 6. Upload Parquet Files to Docker  
Using Git Bash, the cleaned Parquet files were uploaded into the Docker container, making them ready for further processing and analysis.

---




ر
