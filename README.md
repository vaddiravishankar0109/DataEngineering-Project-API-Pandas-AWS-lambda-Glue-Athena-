# **DataEngineering_Project_Pandas_AWSGlue_Athena**

## **Overview**
This project demonstrates approach for processing API response of TOLLYWOOD Songs Playlist and analyzing semi-structured JSON data and finally storing in relational table like format for Athena to Query. 

The workflow involves transforming JSON data into structured format using **Pandas**(locally) followed up by implemting similar functionality in **AWS Lambda** which can work on various Triggers mechanism , and then building data catalog tables with **AWS Glue**, analyzing the data with **Amazon Athena** for a relational table-like experience. Initially, the project is developed locally and later deployed to the **cloud** using **AWS Lambda**.

---

## **Workflow Architecture**

### **Data Retrieval**
- Semi-structured **JSON data** is retrieved from an **API source**.

### **Data Transformation**
- The JSON data is transformed into **structured format** using the **Pandas library**.

### **Data Catalog Creation**
- Transformed data is processed using **AWS Glue** to create **data catalog tables** for efficient querying.

### **Data Querying and Analysis**
- **Amazon Athena** is employed to query the **data catalog tables**, enabling a relational table-like experience for streamlined data analysis.

### **Cloud Deployment**
- The functionality built locally is migrated to the **cloud** using **AWS Lambda**, ensuring scalability and automation.

---

## **Architecture Flow Description**
Here’s the outline for a flow diagram based on the project's architecture:

1. **API Source → (Data Retrieval)**  
   - Fetch semi-structured JSON data.

2. **Local Processing → (Data Transformation)**  
   - Transform JSON into structured data using Pandas Locally.

3. **AWS Lambda → (Cloud Deployment)**  
   - Deploy locally developed functionality to the AWS Lamda , there will be two functions
     1. ***data extract*** - which will capture the raw JSON response from API and load to S3.
     2. ***data transform*** - this will basically transform the raw JSON data to CSV and load it into various S3 buckets.

4. **AWS Glue → (Data Catalog Creation)**  
   - Build data catalog tables from structured data.

5. **Amazon Athena → (Data Querying)**  
   - Query and analyze data catalogs.



---

