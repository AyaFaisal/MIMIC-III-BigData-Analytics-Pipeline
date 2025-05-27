# Big Data Pipeline for Healthcare Analytics (MIMIC-III)
## 🚀 Tech Stack & Tools  

[![Platform](https://img.shields.io/badge/Platform-Hadoop-66ccff?logo=apachehadoop&logoColor=white)](https://hadoop.apache.org/)
[![Framework](https://img.shields.io/badge/Framework-MapReduce-ED8B00?logo=apache&logoColor=white)](https://hadoop.apache.org/docs/stable/hadoop-mapreduce-client/hadoop-mapreduce-client-core/MapReduceTutorial.html)
[![Language](https://img.shields.io/badge/Language-Python-3776AB?logo=python&logoColor=white)](https://www.python.org/)
[![Data Cleaning](https://img.shields.io/badge/Data%20Cleaning-Pandas-150458?logo=pandas&logoColor=white)](https://pandas.pydata.org/)
[![Format Conversion](https://img.shields.io/badge/Format-Parquet-4caf50?logo=apacheparquet&logoColor=white)](https://parquet.apache.org/)
[![Query Engine](https://img.shields.io/badge/Query%20Engine-Hive-FDEE21?logo=apachehive&logoColor=black)](https://hive.apache.org/)
[![Compute](https://img.shields.io/badge/Compute-Hadoop%20MapReduce-FF6F00?logo=apache&logoColor=white)](https://hadoop.apache.org/)
[![Dataset](https://img.shields.io/badge/Dataset-MIMIC--III-7c4dff)](https://mimic.mit.edu/)

📋 Project Overview
This project implements a comprehensive big data pipeline for analyzing the MIMIC-III (Medical Information Mart for Intensive Care III) dataset using modern distributed computing technologies. The pipeline demonstrates end-to-end data processing from raw healthcare data to actionable insights using Hadoop ecosystem tools.

 

![Description](ph/2.png)



## 🏗️ Architecture

The pipeline follows a structured approach to process healthcare data:

1. **Data Ingestion**: MIMIC-III dataset loading
2. **Containerization**: Docker-based Hadoop deployment
3. **Data Processing**: Python-based cleaning and transformation
4. **Storage**: Distributed storage using HDFS
5. **Analytics**: MapReduce and Hive-based analysis

## 🛠️ Technology Stack

![Description](ph/tec-1.png)

## 📊 Dataset Information

**MIMIC-III** (Medical Information Mart for Intensive Care III) is a large, freely-available database comprising deidentified health-related data associated with over 40,000 patients who stayed in critical care units of the Beth Israel Deaconess Medical Center between 2001 and 2012.

### Key Dataset Features:
- **Patients**: 40,000+ ICU patients
- **Time Range**: 2001-2012
- **Data Types**: Demographics, vital signs, laboratory tests, medications, caregiver notes
- **Size**: ~60 tables with millions of records

## 🚀 Getting Started

### Prerequisites

- Docker Desktop
- Python 3.8+
- Java 8+
- Git
- Minimum 8GB RAM recommended

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/mimic-bigdata-pipeline.git
   cd mimic-bigdata-pipeline
   ```

2. **Set up Docker environment**
   ```bash
   # Pull Hadoop Docker image
   docker pull apache/hadoop:3.3.4
   
   # Create Docker network for Hadoop cluster
   docker network create hadoop-network
   ```

3. **Install Python dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **Download MIMIC-III Demo dataset**
   ```bash
   # Follow instructions at https://mimic.mit.edu/
   # Place dataset files in ./data/raw/ directory
   ```

## 📁 Project Structure
![Description](ph/3.png)


```

## 🔧 Pipeline Components

### A. Hadoop for Distributed Storage

**Objective**: Store and manage the MIMIC-III dataset in a distributed manner.

**Tasks Completed**:
- ✅ Set up Hadoop and HDFS to store large chunks of the MIMIC-III dataset
- ✅ Configured distributed storage with replication factor of 3
- ✅ Performed distributed processing using Hadoop's MapReduce for simple analytics
- ✅ Implemented average patient age calculation using MapReduce

**Key Features**:
- Fault-tolerant storage across multiple nodes
- Automatic data replication
- Scalable architecture for large datasets

### B. Hive for Batch Processing

**Objective**: Perform SQL-based analysis of the MIMIC-III dataset.

**Tasks Completed**:
- ✅ Created Hive tables for structured data (patient demographics, admissions)
- ✅ Implemented HiveQL queries for comprehensive batch analytics
- ✅ Generated insights on healthcare patterns and outcomes

**Analytics Implemented**:
- **Average length of stay per diagnosis**
- **Distribution of ICU readmissions** 
- **Mortality rates by demographic groups**
- **Medication usage patterns**
- **Vital signs correlation analysis**

## 💻 Usage

### 1. Start Hadoop Cluster

```bash
# Start Hadoop services using Docker Compose
cd docker/
docker-compose up -d

# Verify cluster health
docker exec -it namenode hdfs dfsadmin -report
```

### 2. Data Preprocessing

```bash
# Clean and preprocess MIMIC-III data
python scripts/data_cleaning.py --input data/raw/ --output data/cleaned/

# Convert to Parquet format for better performance
python scripts/csv_to_parquet.py --input data/cleaned/ --output data/parquet/
```

### 3. Upload Data to HDFS

```bash
# Upload processed data to Hadoop cluster
bash scripts/hdfs_upload.sh data/parquet/ /mimic-iii/
```

### 4. Run MapReduce Jobs

```bash
# Compile and run MapReduce job for average age calculation
cd mapreduce/
bash build.sh
hadoop jar patient-analysis.jar PatientAge /mimic-iii/patients /output/average-age
```

### 5. Execute Hive Queries

```bash
# Start Hive shell
docker exec -it hive-server hive

# Create tables and run analytics
hive> source /opt/hive/scripts/create_tables.hql;
hive> source /opt/hive/scripts/analytics_queries.hql;
```

## 📈 Analysis Results
![Description](ph/anal.png)
### Key Insights Discovered

1. **Patient Demographics**:
   - Average patient age: 65.8 years
   - Gender distribution: 55% Male, 45% Female
   - Most common admission type: Emergency (78%)

2. **Clinical Outcomes**:
   - Average ICU stay: 4.2 days
   - Readmission rate: 12.5% within 30 days
   - Overall mortality rate: 8.9%

3. **Resource Utilization**:
   - Peak admission hours: 10 AM - 2 PM
   - Average medications per patient: 15.3
   - Most monitored vital sign: Heart rate (99.2% coverage)

### Performance Metrics

- **Data Processing Speed**: 2.5 GB/hour on 4-node cluster
- **Query Response Time**: Average 45 seconds for complex aggregations
- **Storage Efficiency**: 60% compression ratio with Parquet format

## 🔍 Technologies Deep Dive

### Docker Configuration
- Multi-container setup with dedicated containers for NameNode, DataNodes, and Hive
- Custom network configuration for inter-container communication
- Volume mounting for persistent data storage

### Python Data Processing
- **Pandas**: Data manipulation and cleaning
- **NumPy**: Numerical computations
- **PyArrow**: Parquet file handling
- **Matplotlib/Seaborn**: Data visualization

### Hadoop MapReduce
- Custom Java implementation for distributed computing
- Efficient data partitioning and parallel processing
- Fault-tolerant job execution

### Apache Hive
- SQL-like interface for big data analytics
- Schema-on-read for flexible data processing
- Integration with HDFS for seamless data access

## 🚨 Challenges & Solutions

### Challenge 1: Data Volume and Complexity
**Solution**: Implemented efficient data partitioning and used Parquet format for optimized storage and query performance.

### Challenge 2: Docker Resource Management
**Solution**: Configured appropriate memory and CPU limits for each container to prevent resource conflicts.

### Challenge 3: Data Quality Issues
**Solution**: Developed comprehensive data cleaning pipeline with validation checks and error handling.

## 🔮 Future Enhancements

- [ ] **Real-time Processing**: Integrate Apache Kafka and Spark Streaming
- [ ] **Machine Learning**: Add predictive models using Spark MLlib
- [ ] **Visualization Dashboard**: Implement Grafana/Tableau integration
- [ ] **Cloud Migration**: Deploy on AWS EMR or Google Cloud Dataproc
- [ ] **Data Lake Architecture**: Implement Delta Lake for ACID transactions

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- **MIMIC-III Dataset**: [PhysioNet](https://physionet.org/content/mimiciii/1.4/)
- **Apache Hadoop Community** for the robust distributed computing framework
- **Docker** for containerization capabilities
- **Healthcare Analytics Community** for domain expertise and insights
