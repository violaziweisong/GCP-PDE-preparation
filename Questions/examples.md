

Subject: Farewell and Thank You

Dear Team,

Today is my last day here, and I wanted to take a moment to express my heartfelt gratitude to each of you. 

Working alongside each of you has been an enriching journey filled with laughter, challenges, and growth. Your support, kindness, and guidance have made this experience truly unforgettable, and I appreciate everything I've learned from you through our collaboration on various audit projects.

Before I depart, I have prepared a special treat for all of you - pastries made of roses and jasmine from my hometown. I have placed them on the snack table and I hope you enjoy these unique flavors.

While I move forward on my path, I will truly miss these days. Please stay in touch! You can reach me at songzwviola@gmail.com, +852 56031042, or connect with me on LinkedIn ([your LinkedIn profile link]).

Thank you once again for everything. Wishing you all continued success and happiness!

Warmest regards,

[Your Name]

---
Subject: Farewell and Thank You

Dear Team,

As I wrap up my last day here, I wanted to take a moment to express my heartfelt gratitude to each of you. 

Working alongside each of you has been an enriching journey filled with laughter, challenges, and growth. Your support, kindness, and guidance have made this experience truly unforgettable, and I appreciate everything I've learned from you through our collaboration on various audit projects.

While I move forward on my path, I will truly miss these days. Please stay in touch! You can reach me at songzwviola@gmail.com, WeChat account zwsongjy7, or connect with me on LinkedIn ([your LinkedIn profile link]).

Thank you once again for everything. Wishing you all continued success and happiness!

Warmest regards,

[Your Name]
---


## Question 22

Your financial services company is moving to cloud technology and wants to store 50 TB of financial time-series data in the cloud. This data is updated frequently and new data will be streaming in all the time. Your company also wants to move their existing Apache Hadoop jobs to the cloud to get insights into this data.

Which product should they use to store the data?
Cloud Bigtable
Google BigQuery
Google Cloud Storage
Google Cloud Datastore
Explain the above produects on their functions

---
For storing 50 TB of frequently updated financial time-series data and supporting Apache Hadoop jobs for insights, **Cloud Bigtable** is the most appropriate choice. Here’s an overview of each of the mentioned products and why Cloud Bigtable stands out for this use case:

### 1. **Cloud Bigtable**

- **Function**: Cloud Bigtable is a fully managed, scalable NoSQL database service designed for large analytical and operational workloads. It is optimized for time-series data, real-time analytics, and large-scale data storage.
- **Use Case**: It is ideal for storing large amounts of time-series data, such as financial data, because it efficiently handles high write throughput and large read volumes. Cloud Bigtable is well-suited for applications that require low-latency access to data and can scale horizontally to handle high data ingestion rates.
- **Features**: 
  - Handles large volumes of data and high request rates.
  - Suitable for time-series data, where data is continuously updated and needs to be queried efficiently.
  - Integrates with Apache Hadoop and other data processing frameworks.
  - Provides high availability and reliability.

### 2. **Google BigQuery**

- **Function**: Google BigQuery is a fully managed, serverless data warehouse designed for large-scale data analytics. It enables fast SQL queries using the processing power of Google's infrastructure.
- **Use Case**: BigQuery is excellent for running complex queries and performing analytics on large datasets. However, it is more suited for analytical workloads rather than real-time, frequently updated data ingestion.
- **Features**: 
  - Designed for interactive analysis and querying of large datasets.
  - Supports SQL queries and integrates well with data visualization tools.
  - Best for running analytical queries rather than serving as a primary store for continuously streaming data.

### 3. **Google Cloud Storage**

- **Function**: Google Cloud Storage is a scalable object storage service for storing and accessing any amount of data. It is designed for high durability and availability.
- **Use Case**: Ideal for storing large volumes of unstructured data, such as backups, data archives, and media. It is not optimized for high-frequency updates or low-latency access for time-series data.
- **Features**: 
  - Provides high durability and availability.
  - Suitable for archiving and backup rather than real-time data ingestion and analytics.
  - Data retrieval can be slower compared to specialized databases for real-time use cases.

### 4. **Google Cloud Datastore**

- **Function**: Google Cloud Datastore is a fully managed NoSQL document database designed for web and mobile applications. It provides a hierarchical data model and is suitable for applications requiring flexible schema and high availability.
- **Use Case**: Datastore is ideal for applications with flexible schema requirements and those needing automatic scaling. However, it is not optimized for handling large volumes of time-series data or high-throughput scenarios.
- **Features**: 
  - Supports hierarchical data and flexible schema.
  - Better suited for transactional data rather than large-scale time-series data.

### Recommendation

**Cloud Bigtable** is the best fit for your requirements because:

- It efficiently handles large volumes of time-series data with high write throughput and low-latency read access.
- It scales horizontally to accommodate increasing data volumes and ingestion rates.
- It integrates well with Apache Hadoop for running analytical jobs and gaining insights from your data.

While **Google BigQuery** and **Google Cloud Storage** are powerful tools for data analytics and storage, respectively, they are not as optimized for real-time data ingestion and frequent updates as Cloud Bigtable. **Google Cloud Datastore** is more suited for applications requiring flexible schema and hierarchical data rather than high-frequency time-series data.


---
## Question 33

You decided to use Cloud Datastore to ingest vehicle telemetry data in real time. You want to build a storage system that will account for the long-term data growth, while keeping the costs low. You also want to create snapshots of the data periodically, so that you can make a point-in-time (PIT) recovery, or clone a copy of the data for Cloud Datastore in a different environment. You want to archive these snapshots for a long time.

Which two methods can accomplish this?
(Choose two.)
Use managed export, and store the data in a Cloud Storage bucket using Nearline or Coldline class.
Use managed export, and then import to Cloud Datastore in a separate project under a unique namespace reserved for that export.
Use managed export, and then import the data into a BigQuery table created just for that export, and delete temporary export files.
Write an application that uses Cloud Datastore client libraries to read all the entities. Treat each entity as a BigQuery table row via BigQuery streaming insert. Assign an export timestamp for each export, and attach it as an extra column for each row. Make sure that the BigQuery table is partitioned using the export timestamp column.
Write an application that uses Cloud Datastore client libraries to read all the entities. Format the exported data into a JSON file. Apply compression before storing the data in Cloud Source Repositories.

---
Question 35

Your United States-based company has created an application for assessing and responding to user actions. The primary table's data volume grows by 250,000 records per second. Many third parties use your application's APIs to build the functionality into their own frontend applications. Your application's APIs should comply with the following requirements:
- Single global endpoint
- ANSI SQL support
- Consistent access to the most up-to-date data

What should you do?
Implement BigQuery with no region selected for storage or processing.
Implement Cloud Spanner with the leader in North America and read-only replicas in Asia and Europe.
Implement Cloud SQL for PostgreSQL with the master in Norht America and read replicas in Asia and Europe.
Implement Cloud Bigtable with the primary cluster in North America and secondary clusters in Asia and Europe.




Answer is Implement Cloud Spanner with the leader in North America and read-only replicas in Asia and Europe.

Cloud Spanner has three types of replicas: read-write replicas, read-only replicas, and witness replicas. Bigquery cannot support 250K data ingestion/second , as ANSI SQL support is required , no other options left except Spanner.

---

Question 77

You need to give new website users a globally unique identifier (GUID) using a service that takes in data points and returns a GUID. This data is sourced from both internal and external systems via HTTP calls that you will make via microservices within your pipeline.
There will be tens of thousands of messages per second and that can be multi-threaded. and you worry about the backpressure on the system.

How should you design your pipeline to minimize that backpressure?
Call out to the service via HTTP.
Create the pipeline statically in the class definition.
Create a new object in the startBundle method of DoFn.
Batch the job into ten-second increments.


Answer is Batch the job into ten-second increments.

Option D is the best approach to minimize backpressure in this scenario. By batching the jobs into 10-second increments, you can throttle the rate at which requests are made to the external GUID service. This prevents too many simultaneous requests from overloading the service.

Option A would not help with backpressure since it just makes synchronous HTTP requests as messages arrive. Similarly, options B and C don't provide any inherent batching or throttling mechanism.

Batching into time windows is a common strategy in stream processing to deal with high velocity data. The 10-second windows allow some buffering to happen, rather than making a call immediately for each message. This provides a natural throttling that can be tuned based on the external service's capacity.

To design a pipeline that minimizes backpressure, especially when dealing with tens of thousands of messages per second in a multi-threaded environment, it's important to consider how each option affects system performance and scalability. Let's examine each of your options:

A. Call out to the service via HTTP: Making HTTP calls to an external service for each message can introduce significant latency and backpressure, especially at high throughput. This is due to the overhead of establishing a connection, waiting for the response, and handling potential network delays or failures.

B. Create the pipeline statically in the class definition: While this approach can improve initialization time and reduce overhead during execution, it doesn't directly address the issue of backpressure caused by high message throughput.

C. Create a new object in the startBundle method of DoFn: This approach is typically used in Apache Beam to initialize resources before processing a bundle of elements. While it can optimize resource usage and performance within each bundle, it doesn't inherently solve the backpressure issue caused by high message rates.

D. Batch the job into ten-second increments: Batching messages can be an effective way to reduce backpressure. By grouping multiple messages into larger batches, you can reduce the frequency of external calls and distribute the processing load more evenly over time. This can lead to more efficient use of resources and potentially lower latency, as the system spends less time waiting on external services.

Given these considerations, option D (Batch the job into ten-second increments) seems to be the most effective strategy for minimizing backpressure in your scenario. By batching messages, you can reduce the strain on your pipeline and external services, making the system more resilient and scalable under high load. However, the exact batch size and interval should be fine-tuned based on the specific characteristics of your workload and the capabilities of the external systems you are interacting with.

Additionally, it's important to consider other strategies in conjunction with batching, such as implementing efficient error handling, load balancing, and potentially using asynchronous I/O for external HTTP calls to further optimize performance and minimize backpressure.

---
Question 100

You launched a new gaming app almost three years ago. You have been uploading log files from the previous day to a separate Google BigQuery table with the table name format LOGS_yyyymmdd. You have been using table wildcard functions to generate daily and monthly reports for all time ranges. Recently, you discovered that some queries that cover long date ranges are exceeding the limit of 1,000 tables and failing.

How can you resolve this issue?
Convert all daily log tables into date-partitioned tables
Convert the sharded tables into a single partitioned table
Enable query caching so you can cache data from previous months
Create separate views to cover each month, and query from these views


Google says that when you have multiple wildcard tables, best option is to shard it into single partitioned table. Time and cost efficient
To address the issue of exceeding the limit of 1,000 tables due to your current sharded table structure in Google BigQuery, the most effective solution is to **convert the sharded tables into a single partitioned table**. Here’s why this approach works best and how it compares to the other options:

### 1. **Convert the Sharded Tables into a Single Partitioned Table**

**Description:**
- **Partitioned Tables**: In BigQuery, partitioned tables allow you to store large amounts of data in a single table while still being able to query efficiently across specific date ranges. You can partition tables by date, which will let you query data efficiently without hitting the 1,000-table limit.

**Advantages:**
- **Efficiency**: Queries on a partitioned table are often more efficient than those using table wildcards, especially for large date ranges.
- **Cost-Effective**: Reduces the need to scan multiple tables and simplifies the query logic, potentially lowering costs.
- **Scalability**: Avoids the issue of hitting table limits and scales better with large datasets over time.

**Implementation Steps:**
1. **Create a Partitioned Table**:
   ```sql
   CREATE TABLE `your_project.your_dataset.logs_partitioned` (
     log_date DATE,
     -- other columns
   )
   PARTITION BY log_date;
   ```

2. **Migrate Data**:
   - Load your existing sharded data into this new partitioned table. You can use a Data Transfer Service or write a script to handle the migration.

3. **Update Queries**:
   - Modify your queries to work with the new partitioned table. You can use date filters to specify the desired range.

   ```sql
   SELECT *
   FROM `your_project.your_dataset.logs_partitioned`
   WHERE log_date BETWEEN '2023-01-01' AND '2023-01-31';
   ```

### 2. **Convert All Daily Log Tables into Date-Partitioned Tables**

**Description:**
- This would involve creating multiple partitioned tables, each corresponding to a specific date range or period.

**Disadvantages:**
- **Over-Complexity**: Managing multiple partitioned tables can become cumbersome and does not solve the fundamental issue of exceeding the table limit.

### 3. **Enable Query Caching**

**Description:**
- Query caching in BigQuery is used to speed up query execution by reusing the results of previously run queries.

**Disadvantages:**
- **Not a Solution for Table Limits**: Caching helps with performance but does not address the issue of exceeding the table limit or manage large datasets effectively.

### 4. **Create Separate Views for Each Month**

**Description:**
- This involves creating views that aggregate data by month from the existing sharded tables.

**Disadvantages:**
- **Still Exceeds Table Limits**: Although views can simplify querying, you are still dealing with the original sharded tables and will eventually hit the 1,000-table limit.

### **Summary**

**Converting the sharded tables into a single partitioned table** is the best solution because it efficiently manages large datasets, avoids the 1,000-table limit, and improves query performance. It provides a scalable and manageable way to handle historical and ongoing data without running into limitations imposed by the sharded table approach.

Question 110

Your company needs to upload their historic data to Cloud Storage. The security rules don't allow access from external IPs to their on-premises resources. After an initial upload, they will add new data from existing on-premises applications every day.

What should they do?
Execute gsutil rsync from the on-premises servers.
Use Cloud Dataflow and write the data to Cloud Storage.
Write a job template in Cloud Dataproc to perform the data transfer.
Install an FTP server on a Compute Engine VM to receive the files and move them to Cloud Storage.

---
Question 108

You're using Bigtable for a real-time application, and you have a heavy load that is a mix of read and writes. You've recently identified an additional use case and need to perform hourly an analytical job to calculate certain statistics across the whole database. You need to ensure both the reliability of your production application as well as the analytical workload.

What should you do?
Export Bigtable dump to GCS and run your analytical job on top of the exported files.
Add a second cluster to an existing instance with a multi-cluster routing, use live-traffic app profile for your regular workload and batch-analytics profile for the analytics workload.
Add a second cluster to an existing instance with a single-cluster routing, use live-traffic app profile for your regular workload and batch-analytics profile for the analytics workload.
Increase the size of your existing cluster twice and execute your analytics workload on your new resized cluster.

Answer is Add a second cluster to an existing instance with a single-cluster routing, use live-traffic app profile for your regular workload and batch-analytics profile for the analytics workload.

You need to perform an hourly batch job on the cluster that already has high workload. in such cases, the best option is to replicate the cluster with single cluster routing. The original cluster can continue its read and writes. the replicated cluster can be used for analytical workload without impacting original cluster. Multi cluster routing is beneficial in cases where high availability is needed but requirement is only to isolate analytical workload from existing cluster.

---
Question 107

Your team is responsible for developing and maintaining ETLs in your company. One of your Dataflow jobs is failing because of some errors in the input data, and you need to improve reliability of the pipeline (incl. being able to reprocess all failing data).

What should you do?
Add a filtering step to skip these types of errors in the future, extract erroneous rows from logs.
Add a try... catch block to your DoFn that transforms the data, extract erroneous rows from logs.
Add a try... catch block to your DoFn that transforms the data, write erroneous rows to PubSub directly from the DoFn.
Add a try... catch block to your DoFn that transforms the data, use a sideOutput to create a PCollection that can be stored to PubSub later.


When dealing with data pipeline failures in Google Cloud Dataflow due to errors in input data, it’s important to ensure that your pipeline is resilient and can handle and reprocess errors effectively. Here's a breakdown of the options:

### 1. **Add a Filtering Step to Skip These Types of Errors in the Future, Extract Erroneous Rows from Logs**

**Description:**
- This approach involves modifying the pipeline to filter out problematic records that cause errors, and then extracting these errors from logs for further analysis.

**Advantages:**
- **Prevention**: Prevents the pipeline from failing on future errors of the same type.

**Disadvantages:**
- **Limited Reprocessing**: This does not directly address reprocessing or managing the erroneous data. It focuses on preventing failures but does not handle the errors that have already occurred.

### 2. **Add a Try... Catch Block to Your `DoFn` That Transforms the Data, Extract Erroneous Rows from Logs**

**Description:**
- This involves adding error handling within your `DoFn` to catch exceptions and then extract erroneous rows from logs.

**Advantages:**
- **Error Handling**: Catches and logs errors within the `DoFn`.

**Disadvantages:**
- **Reactive Approach**: This approach focuses on extracting errors after the fact, and it does not provide a mechanism for reprocessing or handling erroneous rows dynamically.

### 3. **Add a Try... Catch Block to Your `DoFn` That Transforms the Data, Write Erroneous Rows to Pub/Sub Directly from the `DoFn`**

**Description:**
- This approach involves handling errors in your `DoFn` and sending erroneous rows to Pub/Sub for further analysis or reprocessing.

**Advantages:**
- **Immediate Action**: Allows you to handle errors in real-time and forward erroneous rows for further processing or monitoring.

**Disadvantages:**
- **Potential Overhead**: Directly writing to Pub/Sub from `DoFn` can introduce overhead and complexity. The handling of erroneous rows needs to be carefully managed.

### 4. **Add a Try... Catch Block to Your `DoFn` That Transforms the Data, Use a SideOutput to Create a PCollection That Can Be Stored to Pub/Sub Later**

**Description:**
- This involves adding error handling within the `DoFn` and using a `SideOutput` to capture erroneous rows into a separate `PCollection`, which can then be written to Pub/Sub or another sink for later processing.

**Advantages:**
- **Structured Error Handling**: This method allows you to separately handle and reprocess erroneous data without affecting the main pipeline. 
- **Flexibility**: Enables reprocessing of erroneous data later, and keeps the main pipeline clean and focused on processing valid data.

**Disadvantages:**
- **Complexity**: Introduces additional steps and complexity in managing side outputs and ensuring that the erroneous data is properly handled and reprocessed.

### **Recommendation**

**Add a Try... Catch Block to Your `DoFn` That Transforms the Data, Use a SideOutput to Create a PCollection That Can Be Stored to Pub/Sub Later**

**Rationale:**
- This approach provides a robust way to handle errors and ensures that erroneous data can be captured, stored, and reprocessed separately from the main data pipeline. Using `SideOutput` allows for a clean separation of error handling and main data processing, which improves reliability and maintainability.

**Implementation Steps:**
1. **Add Error Handling**: Implement a `try... catch` block within your `DoFn` to handle and catch exceptions that occur during data transformation.
   
2. **Use SideOutput**: Create a `PCollection` for erroneous rows using `SideOutput`.

   ```python
   class MyDoFn(DoFn):
       def process(self, element, context):
           try:
               # Transformation logic
               yield transformed_element
           except Exception as e:
               # Capture erroneous rows in a side output
               context.side_output(erroneous_rows, element)
   
   p = Pipeline()
   main_data = p | 'Read' >> ReadFromSource()
   erroneous_data = main_data | 'Transform' >> ParDo(MyDoFn()).with_outputs('erroneous_rows', main='main_data')
   erroneous_data.erroneous_rows | 'WriteErrorsToPubSub' >> WriteToPubSub(...)
   main_data.main | 'WriteToBigQuery' >> WriteToBigQuery(...)
   ```
---
Question 104

You are a head of BI at a large enterprise company with multiple business units that each have different priorities and budgets. You use on-demand pricing for BigQuery with a quota of 2K concurrent on-demand slots per project. Users at your organization sometimes don't get slots to execute their query and you need to correct this. You'd like to avoid introducing new projects to your account.

What should you do?
Convert your batch BQ queries into interactive BQ queries.
Create an additional project to overcome the 2K on-demand per-project quota.
Switch to flat-rate pricing and establish a hierarchical priority model for your projects.
Increase the amount of concurrent slots per project at the Quotas page at the Cloud Console.

3. **Process SideOutput Data**: Set up a separate process or pipeline to handle and reprocess the erroneous data stored in Pub/Sub or another sink.

This approach ensures that your pipeline remains reliable and that errors are effectively managed and reprocessed, enhancing the overall robustness of your data processing workflows.


You might simply prefer a fixed monthly bill, or encounter workloads that are extremely sensitive to query latency, and thus have predictability and control requirements that cannot be met by the on-demand service. For such situations, you can use the flat-rate service. In this model, a certain number of slots are dedicated to your project(s), and you can establish a hierarchical priority model amongst the projects. The flat-rate model is especially suitable for large enterprises with multiple business units and workloads with varying priorities and budgets. For instance, the arrangement illustrated below gives priority to queries that are issued from the “Dashboarding” project over the queries from the other two projects. But even with prioritization, slots won’t be wasted. If the prioritized “Dashboarding” project does not use all its dedicated slots, they’ll be distributed among the remaining projects. Even data stored in the “Data Science” project can be queried from the “Dashboarding” project with a higher priority than when it’s queried from within the “Data Science” project itself.

---


Question 106

Your team is responsible for developing and maintaining ETLs in your company. One of your Dataflow jobs is failing because of some errors in the input data, and you need to improve reliability of the pipeline (incl. being able to reprocess all failing data).

What should you do?
Add a filtering step to skip these types of errors in the future, extract erroneous rows from logs.
Add a try... catch block to your DoFn that transforms the data, extract erroneous rows from logs.
Add a try... catch block to your DoFn that transforms the data, write erroneous rows to PubSub directly from the DoFn.
Add a try... catch block to your DoFn that transforms the data, use a sideOutput to create a PCollection that can be stored to PubSub later.



---
Question 107

You're using Bigtable for a real-time application, and you have a heavy load that is a mix of read and writes. You've recently identified an additional use case and need to perform hourly an analytical job to calculate certain statistics across the whole database. You need to ensure both the reliability of your production application as well as the analytical workload.

What should you do?
Export Bigtable dump to GCS and run your analytical job on top of the exported files.
Add a second cluster to an existing instance with a multi-cluster routing, use live-traffic app profile for your regular workload and batch-analytics profile for the analytics workload.
Add a second cluster to an existing instance with a single-cluster routing, use live-traffic app profile for your regular workload and batch-analytics profile for the analytics workload.
Increase the size of your existing cluster twice and execute your analytics workload on your new resized cluster.

Answer is Add a second cluster to an existing instance with a single-cluster routing, use live-traffic app profile for your regular workload and batch-analytics profile for the analytics workload.

You need to perform an hourly batch job on the cluster that already has high workload. in such cases, the best option is to replicate the cluster with single cluster routing. The original cluster can continue its read and writes. the replicated cluster can be used for analytical workload without impacting original cluster. Multi cluster routing is beneficial in cases where high availability is needed but requirement is only to isolate analytical workload from existing cluster.

---
Question 109

Your company needs to upload their historic data to Cloud Storage. The security rules don't allow access from external IPs to their on-premises resources. After an initial upload, they will add new data from existing on-premises applications every day.

What should they do?
Execute gsutil rsync from the on-premises servers.
Use Cloud Dataflow and write the data to Cloud Storage.
Write a job template in Cloud Dataproc to perform the data transfer.
Install an FTP server on a Compute Engine VM to receive the files and move them to Cloud Storage.

Answer is Execute gsutil rsync from the on-premises servers.

Dataflow is on cloud is external; "don't allow access from external IPs to their on-premises resources" so no dataflow.
---
Question 113

You have Cloud Functions written in Node.js that pull messages from Cloud Pub/Sub and send the data to BigQuery. You observe that the message processing rate on the Pub/Sub topic is orders of magnitude higher than anticipated, but there is no error logged in Stackdriver Log Viewer.

What are the two most likely causes of this problem? (Choose two.)
Publisher throughput quota is too small.
Total outstanding messages exceed the 10-MB maximum.
Error handling in the subscriber code is not handling run-time errors properly.
The subscriber code cannot keep up with the messages.
The subscriber code does not acknowledge the messages that it pulls.

Answers are;
C. Error handling in the subscriber code is not handling run-time errors properly.
E. The subscriber code does not acknowledge the messages that it pulls.

By not acknowleding the pulled message, this result in it be putted back in Cloud Pub/Sub, meaning the messages accumulate instead of being consumed and removed from Pub/Sub. The same thing can happen ig the subscriber maintains the lease on the message it receives in case of an error. This reduces the overall rate of processing because messages get stuck on the first subscriber. Also, errors in Cloud Function do not show up in Stackdriver Log Viewer if they are not correctly handled.
A: No problem with publisher rate as the observed result is a higher number of messages and not a lower number.
B: if messages exceed the 10MB maximum, they cannot be published.
D: Cloud Functions automatically scales so they should be able to keep up.


---
Question 118

You currently have a single on-premises Kafka cluster in a data center in the us-east region that is responsible for ingesting messages from IoT devices globally. Because large parts of globe have poor internet connectivity, messages sometimes batch at the edge, come in all at once, and cause a spike in load on your Kafka cluster. This is becoming difficult to manage and prohibitively expensive.

What is the Google-recommended cloud native architecture for this scenario?
Edge TPUs as sensor devices for storing and transmitting the messages.
Cloud Dataflow connected to the Kafka cluster to scale the processing of incoming messages.
An IoT gateway connected to Cloud Pub/Sub, with Cloud Dataflow to read and process the messages from Cloud Pub/Sub.
A Kafka cluster virtualized on Compute Engine in us-east with Cloud Load Balancing to connect to the devices around the world.

Answer is An IoT gateway connected to Cloud Pub/Sub, with Cloud Dataflow to read and process the messages from Cloud Pub/Sub.

Alterative to Kafka in google cloud native service is Pub/Sub and Dataflow punched with Pub/Sub is the google recommended option

---
Question 119

You have a petabyte of analytics data and need to design a storage and processing platform for it. You must be able to perform data warehouse-style analytics on the data in Google Cloud and expose the dataset as files for batch analysis tools in other cloud providers.
What should you do?
Store and process the entire dataset in BigQuery.
Store and process the entire dataset in Cloud Bigtable.
Store the full dataset in BigQuery, and store a compressed copy of the data in a Cloud Storage bucket.
Store the warm data as files in Cloud Storage, and store the active data in BigQuery. Keep this ratio as 80% warm and 20% active.

Explanation:
BigQuery: Ideal for data warehouse-style analytics due to its scalability, ease of use, and powerful querying capabilities.
Cloud Storage: Provides a way to store a compressed copy of the data, making it accessible for batch processing tools on other cloud providers.

BigQuery can read compressed files directly if they are in supported formats like GZIP for CSV and JSON files. However, it cannot query directly from compressed files in Cloud Storage. You would need to load or query the data into BigQuery, where it can handle compressed input during loading
---

Question 121

You are building a new application that you need to collect data from in a scalable way. Data arrives continuously from the application throughout the day, and you expect to generate approximately 150 GB of JSON data per day by the end of the year. Your requirements are:
- Decoupling producer from consumer
- Space and cost-efficient storage of the raw ingested data, which is to be stored indefinitely
- Near real-time SQL query
- Maintain at least 2 years of historical data, which will be queried with SQL

Which pipeline should you use to meet these requirements?
Create an application that provides an API. Write a tool to poll the API and write data to Cloud Storage as gzipped JSON files.
Create an application that writes to a Cloud SQL database to store the data. Set up periodic exports of the database to write to Cloud Storage and load into BigQuery.
Create an application that publishes events to Cloud Pub/Sub, and create Spark jobs on Cloud Dataproc to convert the JSON data to Avro format, stored on HDFS on Persistent Disk.
Create an application that publishes events to Cloud Pub/Sub, and create a Cloud Dataflow pipeline that transforms the JSON event payloads to Avro, writing the data to Cloud Storage and BigQuery.

D
Because we have to be able to query over historical 2 years data only BigQuery address this issue and because we have lots of input data we have to use Dataflow for processing.

Explanation:
- Decoupling Producer from Consumer: Cloud Pub/Sub acts as a messaging service, allowing you to decouple the application (producer) from the processing pipeline (consumer).
- Space and Cost-Efficient Storage: Transforming JSON to Avro reduces storage costs due to Avro's efficient binary format. Storing data in Cloud Storage is cost-effective.
- Near Real-Time SQL Query: Dataflow can write directly to BigQuery, enabling near real-time SQL querying capabilities.
Historical Data Storage: Cloud Storage can retain Avro files indefinitely, and BigQuery can maintain at least 2 years of historical data for querying.

This setup efficiently handles ingestion, transformation, and storage while meeting all specified requirements.
---
Question 123

Data Analysts in your company have the Cloud IAM Owner role assigned to them in their projects to allow them to work with multiple GCP products in their projects. Your organization requires that all BigQuery data access logs be retained for 6 months. You need to ensure that only audit personnel in your company can access the data access logs for all projects.

What should you do?
Enable data access logs in each Data Analyst's project. Restrict access to Stackdriver Logging via Cloud IAM roles.
Export the data access logs via a project-level export sink to a Cloud Storage bucket in the Data Analysts' projects. Restrict access to the Cloud Storage bucket.
Export the data access logs via a project-level export sink to a Cloud Storage bucket in a newly created projects for audit logs. Restrict access to the project with the exported logs.
Export the data access logs via an aggregated export sink to a Cloud Storage bucket in a newly created project for audit logs. Restrict access to the project that contains the exported logs.

Answer is Export the data access logs via an aggregated export sink to a Cloud Storage bucket in a newly created project for audit logs. Restrict access to the project that contains the exported logs.

Aggregated log sink will create a single sink for all projects, the destination can be a google cloud storage, pub/sub topic, bigquery table or a cloud logging bucket. without aggregated sink this will be required to be done for each project individually which will be cumbersome.

Reference:
https://cloud.google.com/logging/docs/export/aggregated_sinks

---
Question 127

You need to deploy additional dependencies to all of a Cloud Dataproc cluster at startup using an existing initialization action. Company security policies require that Cloud Dataproc nodes do not have access to the Internet so public initialization actions cannot fetch resources.

What should you do?
Deploy the Cloud SQL Proxy on the Cloud Dataproc master
Use an SSH tunnel to give the Cloud Dataproc cluster access to the Internet
Copy all dependencies to a Cloud Storage bucket within your VPC security perimeter
Use Resource Manager to add the service account used by the Cloud Dataproc cluster to the Network User role

Answer is Copy all dependencies to a Cloud Storage bucket within your VPC security perimeter

If you create a Dataproc cluster with internal IP addresses only, attempts to access the Internet in an initialization action will fail unless you have configured routes to direct the traffic through a NAT or a VPN gateway. Without access to the Internet, you can enable Private Google Access, and place job dependencies in Cloud Storage; cluster nodes can download the dependencies from Cloud Storage from internal IPs.

Reference:
https://cloud.google.com/dataproc/docs/concepts/configuring-clusters/init-actions

---
Question 128

You work for a mid-sized enterprise that needs to move its operational system transaction data from an on-premises database to GCP. The database is about 20 TB in size.

Which database should you choose?
Cloud SQL
Cloud Bigtable
Cloud Spanner
Cloud Datastore

Answer is Cloud SQL

Cloud SQL can store upto 30 TB.

---
Question 129

You have data pipelines running on BigQuery, Cloud Dataflow, and Cloud Dataproc. You need to perform health checks and monitor their behavior, and then notify the team managing the pipelines if they fail. You also need to be able to work across multiple projects. Your preference is to use managed products of features of the platform.

What should you do?
Export the information to Cloud Stackdriver, and set up an Alerting policy
Run a Virtual Machine in Compute Engine with Airflow, and export the information to Stackdriver
Export the logs to BigQuery, and set up App Engine to read that information and send emails if you find a failure in the logs
Develop an App Engine application to consume logs using GCP API calls, and send emails if you find a failure in the logs

Answer is Export the information to Cloud Stackdriver, and set up an Alerting policy

Monitoring does not only provide you with access to Dataflow-related metrics, but also lets you to create alerting policies and dashboards so you can chart time series of metrics and choose to be notified when these metrics reach specified values.

---

Question 130

Suppose you have a table that includes a nested column called "city" inside a column called "person", but when you try to submit the following query in BigQuery, it gives you an error. SELECT person FROM `project1.example.table1` WHERE city = "London"
How would you correct the error?
Add ", UNNEST(person)" before the WHERE clause.
Change "city" to "person.city".
Change "person" to "city.person".
Add ", UNNEST(city)" before the WHERE clause.

If you need to filter based on a nested column without unnesting, you can directly reference it using the dot notation as shown. However, if you need to work with repeated fields, you might need to use UNNEST. Here's how you would use it:
```
SELECT person
FROM `project1.example.table1`,
UNNEST(person) AS p
WHERE p.city = "London"
Use UNNEST when dealing with repeated fields to flatten the array and access individual elements.
```


---
Question 138

What are two methods that can be used to denormalize tables in BigQuery?
1) Split table into multiple tables; 2) Use a partitioned table
1) Join tables into one table; 2) Use nested repeated fields
1) Use a partitioned table; 2) Join tables into one table
1) Use nested repeated fields; 2) Use a partitioned table

   
Denormalization in BigQuery can improve query performance by reducing the number of joins needed between tables. Here are two common methods to denormalize tables in BigQuery:

### 1. **Nested and Repeated Fields**
BigQuery supports nested and repeated fields, which allow you to store related data in a single table instead of separate tables. This method is particularly useful for handling one-to-many relationships.

- **Nested Fields**: You can create a column that is itself a structured type (a record) containing multiple fields.
  
- **Repeated Fields**: You can create an array of records to store multiple values for a single field.

**Example**:
Instead of having separate tables for `users` and `orders`, you could have a single table where each user record contains an array of their orders.

```sql
CREATE TABLE users (
  user_id INT64,
  name STRING,
  orders ARRAY<STRUCT<order_id INT64, order_date DATE, total_amount FLOAT64>>
);
```

### 2. **Flattening Tables**
Flattening involves merging related tables into a single flat table, which can eliminate the need for joins and speed up query performance. This is often done through queries that combine multiple related tables into one.

**Example**:
You can use a `JOIN` operation to combine a `users` table and an `orders` table into a single denormalized table:

```sql
CREATE TABLE denormalized_users AS
SELECT
  u.user_id,
  u.name,
  o.order_id,
  o.order_date,
  o.total_amount
FROM
  users u
LEFT JOIN
  orders o ON u.user_id = o.user_id;
```

### Summary
- **Nested and Repeated Fields**: Use structured types to store related data within a single table.
- **Flattening Tables**: Merge multiple related tables into a single flat table to reduce the need for joins.

Both methods can help improve query performance in BigQuery by reducing complexity and the volume of data processed during queries. If you have more questions or need additional examples, feel free to ask!

---
Question 139

Once table is created, you cannot change it partitioned

---



