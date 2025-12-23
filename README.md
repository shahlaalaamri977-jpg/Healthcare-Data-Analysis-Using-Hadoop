# Healthcare Data Analysis Using Hadoop

## Project Overview
This project demonstrates the use of the Apache Hadoop ecosystem to perform large-scale data analysis on a healthcare dataset. The primary objective is to process and analyze patient billing information using the MapReduce programming model. Hadoop Distributed File System (HDFS) is used for data storage, while custom Java-based Mapper and Reducer classes are implemented to compute analytical insights efficiently.

## Dataset Description
The dataset used in this project is a structured healthcare dataset obtained from Kaggle. It contains patient-related information such as admission type, medical condition, billing amount, insurance provider, and hospital details. Due to the dataset size and structure, Hadoop MapReduce was selected as an appropriate framework for distributed data processing.

Dataset Source:  
https://www.kaggle.com/code/manarmohamed24/analysis-healthcare-dataset

## Technologies Used
- Apache Hadoop 2.6.0 (CDH 5.13.0)
- Hadoop Distributed File System (HDFS)
- MapReduce Framework
- Java (JDK 1.7)
- Eclipse IDE
- Cloudera QuickStart VM
- Oracle VirtualBox

## System Architecture
The project follows a distributed processing architecture where the dataset is first uploaded to HDFS. The MapReduce job reads the input data from HDFS, processes it in parallel using the Mapper and Reducer, and writes the final output back to HDFS.

## Project Objective
The main objective of this project is to calculate the **average billing amount per admission type** (e.g., Emergency, Urgent, Elective) using Hadoop MapReduce. This analysis helps demonstrate how distributed systems can efficiently process and aggregate healthcare data.

## Implementation Details

### Data Ingestion
The healthcare dataset is uploaded into HDFS using Hadoop filesystem commands. A dedicated directory is created to store both input and output data.

### Mapper Implementation
The Mapper reads each line of the dataset, skips the header row, extracts the admission type and billing amount fields, and emits them as key-value pairs where:
- Key: Admission Type
- Value: Billing Amount

### Reducer Implementation
The Reducer receives grouped billing amounts for each admission type, calculates the sum and count, and outputs the average billing amount for each category.

### Driver Program
The Driver class configures the MapReduce job, sets the Mapper and Reducer classes, defines input and output paths, and submits the job to the Hadoop cluster for execution.

## Execution Steps
1. Upload the dataset to HDFS.
2. Compile the Java MapReduce program.
3. Package the compiled classes into a JAR file.
4. Execute the MapReduce job using the Hadoop command-line interface.
5. Retrieve and verify the output from HDFS.

## Output
The final output is stored in HDFS and contains the average billing amount for each admission type. The results are generated successfully after the MapReduce job completes.

Sample Output:
