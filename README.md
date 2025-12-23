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


## Execution Steps
1. Upload the dataset to HDFS.
2. Compile the Java MapReduce program.
3. Package the compiled classes into a JAR file.
4. Execute the MapReduce job using the Hadoop command-line interface.
5. Retrieve and verify the output from HDFS.

## Output
The final output is stored in HDFS and contains the average billing amount for each admission type. The results are generated successfully after the MapReduce job completes.

Sample Output:
