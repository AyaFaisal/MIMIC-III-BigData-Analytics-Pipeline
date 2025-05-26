# MIMIC-III-BigData-Analytics-Pipeline
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

## Notes  
- Make sure Docker is running before uploading files.  
- Use appropriate Git Bash commands (such as `docker cp`) to transfer files into the container.

---

Good luck with your project!

ر
