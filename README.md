# Uber-ETL-pipeline-using-GCP
A Data Analytics Project applying ETL logic on Uber data using Google Cloud Platform

### Introduction:
In this project, i have built an ETL Pipeline using Uber data. The pipeline will retrieve the data from the .csv file stored in Google Cloud Storage  which is then loaded to Mage and several transofrmations are applied on the raw data ultimately loading into the Google BigQuery for analytics.

### Dataset:
This Dataset contains the information related to Uber like trip_distance, passenger_count, pickup_location, dropoff_location, payment_type, fare_amount etc.. -- [Uber_data.csv](https://github.com/SameerPathaan/Uber-ETL-pipeline-using-GCP/tree/main/data)

### Architecture:
***Description:*** Firstly the raw data is uploaded to Google Cloud Storage collected from Uber website and coded using the python code and stored in Jupyter Notebook. Here starts the real process, The entire ETL part of the project is run of Google VM Compute Engine. i have created a data instance, where the Mage application is run on this machine to transform and load the data to BigQuery for further Analytics. When talking about the Mage, the pipeline has three main portions (ETL) - data is extracted from the file in Google Clous Storage using loader function, then transformed using Transformer function, finally loaded back Google BigQuery using Eporter function. The code for each of the functions is available at [Mage_Code](https://github.com/SameerPathaan/Uber-ETL-pipeline-using-GCP/tree/main/Mage_Code). After loading it to BigQuery, I have generated a table using a SQL query for further analytics using Looker Studio to build a Dashboard. 

### Architecture Diagrams: - [Pipeline_Architecture](https://github.com/SameerPathaan/Uber-ETL-pipeline-using-GCP/blob/main/Architecture_Diagrams/Uber_Pipeline_architecture.jpg), [Mage_Tree](https://github.com/SameerPathaan/Uber-ETL-pipeline-using-GCP/blob/main/Architecture_Diagrams/Mage_Architecture.png)

### Utilized Services:
**Google Cloud Storage:** It is a cloud-based object storage service provided by Google Cloud Platform. Google Cloud Storage provides a scalable, durable, and highly available solution for storing and retrieving data. It allows users to store and retrieve data in various formats such as images, videos, audio files, documents, and other binary or text data.

**Mage:** It is an open-source e-commerce platform used for building and managing online stores. It provides a flexible and customizable platform for creating a feature-rich online store. Mage supports various payment gateways and shipping methods, and it also provides advanced features such as product management, order management, and customer management.

**Google VM Compute Engine:** It is a virtual machine (VM) hosting service provided by Google Cloud Platform. It allows users to create and run virtual machines on Google's infrastructure. Users can choose from a variety of pre-configured virtual machine images or create their custom images. Compute Engine provides users with control over their virtual machines, including the ability to start, stop, and configure the machines.

**Google BigQuery:** It is a serverless, cloud-based data warehousing and analytics service provided by Google Cloud Platform. BigQuery allows users to store and analyze massive amounts of data quickly and easily. It provides users with a SQL-like query language for data analysis, and it also supports real-time data streaming and batch data processing.

**Google Looker Studio:** It is a cloud-based business intelligence and analytics platform provided by Google Cloud Platform. Looker Studio allows users to create and share data visualizations, reports, and dashboards using a drag-and-drop interface. It provides advanced analytics features such as predictive modeling and machine learning integration. Looker Studio also supports collaboration and sharing of data and reports among team members.

### Project Execution Flow:
Raw Data(Uber_data.csv) --> Google CLoud Storage --> ETL ( Mage [uber_data_load -- uber_transform_load -- uber_bigquery_load] ) --> Google BigQuery (Data Warehouse)  --> Looker Studio (Analytics)


