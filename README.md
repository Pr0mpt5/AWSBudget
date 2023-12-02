## AWS Budget
Tutorial of the using of AWS Pricing Calculator 

# Project Budget: **Evaluate cloud software for analytics.**

**AWS Pricing Calculator**

AWS Pricing Calculator is a free web-based planning tool that you can use to create cost estimates for using AWS services. You can use AWS Pricing Calculator for the following use cases:

-   Model your solutions before building them.
-   Explore AWS service price points.
-   Review the calculations behind your estimates.
-   Plan your AWS spend.
-   Find cost saving opportunities.

**Starting our budget**

Please go this link to start using AWS Pricing Calculator: [https://calculator.aws/\#/](https://calculator.aws/#/)

The information below is a tutorial according to the use of the services indicated in the AWS Architecture Diagram.

![A diagram of a diagram Description automatically generated](media/cf35c2144f61a0f9e98aac7b82d5a54f.png)

-   In AWS Pricing Calculator main screen do click in **create estimate** option.

**![A screenshot of a calculator Description automatically generated](media/1c10f80edc1f9aa9188290820e17c80c.png)**

-   In **Add service** window we will choose the location type and region where the services are located.

![A screenshot of a computer Description automatically generated](media/a606c825a92db8e5977094b04fed5ed8.png)

-   In the **Find service** option we will look for the services we want to add to the budget.
1.  **Elastic Load Balancer**
-   In **find service** type **Elastic Load Balancing** and choose the **configure** button.

    **![A screenshot of a computer Description automatically generated](media/ffe5fdedb7d0352558ec0d740d4fa684.png)**

-   In the **Configure Elastic Load Balancer** window, in the **Description** option named the service for example: “Budget ELB”, then **Choose the location type** to **Region**, and **Choose the region** in this case is US East (Ohio)
-   In **Elastic Load Balancing** choose **Application Load Balancer** and the **Application Load Balancer feature** as **Load Balancer in AWS Region**

    **![A screenshot of a computer Description automatically generated](media/c08d4fcc584844a213435bbdfa94b507.png)**

-   In **Service Settings**, in the **Number of Application Load Balancers** option put the number of Application Load Balancers.
-   Show calculations will show us the current cost per hour, in a month.

    ![A screenshot of a calculator Description automatically generated](media/d8859bb6ea86a7b7e2f68852709134bf.png)

-   Load Balancer Capacity Units (LCUs) measures the dimensions on which the Application Load Balancer processes your traffic (averaged over an hour). The four dimensions are: new connections, active connections, processed bytes, and rule evaluations. You are charged only on the dimension with the highest usage.

    ![A screenshot of a computer Description automatically generated](media/26b848e639a8d675957851030b919909.png)

    ![A close-up of a white sheet Description automatically generated](media/54375de9db986a2b09a9f15a3cebe9d5.png)

1.  **Amazon API Gateway**
-   In **find service** type **Amazon API Gateway** and choose the **configure** button.

    ![A screenshot of a computer Description automatically generated](media/59bd2928fbbc926ba0f48565a46b2c85.png)

-   In the **Configure Amazon API Gateway** window, in the **Description** option named the service for example: “Budget Amazon API Gateway”, then **Choose the location type** to **Region**, and **Choose the region** in this case is US East (Ohio)

    ![A screenshot of a computer Description automatically generated](media/0117d1780eb77737c5c58ec9f3f9ce1c.png)

-   HTTP APIs, you only pay when your APIs are in use. There are no minimum fees or upfront commitments. You pay for the API calls you receive, and the amount of data transferred out. Requests are metered in 512 KB increments of data. So, a request with 513 KB of data is metered as two requests.

![A screenshot of a computer Description automatically generated](media/8d4023f5965dfa1b10113047355ffa0a.png)

**![A black text on a white background Description automatically generated](media/4b4a5c603d94d660801b3378523a10f7.png)**

-   There are also options to use REST APIs and WebSocket APIs for both you only pay when the APIs are in use. There are no minimum fees or upfront commitments. You pay for the API calls you receive, and the amount of data transferred out. There are no data transfer out charges for Private APIs. However, AWS PrivateLink charges apply when using Private APIs in API Gateway. API Gateway also provides optional data caching charged at an hourly rate that varies based on the cache size you select. For WebSocket APIs, you pay for messages sent and received and the total number of connection minutes. You may send and receive messages up to 128 kilobytes (KB) in size. Messages are metered in 32 KB increments. So, a 33 KB message is metered as two messages.
1.  **Amazon Kinesis Data Firehose**
-   In **find service** type **Amazon Kinesis Data Firehose** and choose the **configure** button.

**![A screenshot of a computer Description automatically generated](media/8a61fe4ff2133c6e55f566f555520132.png)**

-   In the **Configure Amazon Kinesis Firehose** window, in the **Description** option name the service for example: “Budget Amazon Kinesis Firehose”, then **Choose the location type** to **Region**, and **Choose the region** in this case is US East (Ohio)

    ![A screenshot of a login box Description automatically generated](media/b66574af76544461352c9359453fb972.png)

-   **Data Ingestion** pricing is based on the volume of data ingested into Amazon Kinesis Data Firehose, which is calculated as the number of data records you send to the service, times the size of each record rounded up to the nearest 5KB. For example, if your data records are 42KB each, Kinesis Data Firehose will count each record as 45KB of data ingested. Usage charges associated with Amazon S3, Amazon Redshift, Amazon Elasticsearch Service, and Splunk are billed separately. Data transfer usage charges for cross-region and to the internet are billed separately.

    ![A screenshot of a computer Description automatically generated](media/b67decc8bd967edc8b515ade221b77f6.png)

    ![A screenshot of a computer Description automatically generated](media/015684f5a274503b156aed5b0e3cb56d.png)

-   **Data Format Conversion** pricing is based on the volume of incoming data. It works only if delivery stream to convert the incoming data into Apache Parquet or Apache ORC format is configured before the data is delivered to destinations.
-   **Dynamic Partitioning** is used to continuously group data by keys in your records (such as “customer_id”), and have data delivered to S3 prefixes mapped to each key. With Dynamic Partitioning, you pay per GB delivered to S3, per object, and optionally per JQ processing hour for data parsing.
-   **Data Processed to VPC** pricing is based on the volume of data ingested into Amazon Kinesis Firehose. If you configure your delivery stream to deliver to a destination that resides in a VPC, you will be charged based on the volume of data processed via the VPC and for the number of hours that your delivery stream is active in each subnet.
1.  **Amazon Simple Storage Service (S3) (Object Lambda)**
-   In **find service** type **Amazon Simple Storage Service** and choose the **configure** button.

![A screenshot of a computer Description automatically generated](media/1cc31d592afb78d00ec300fd1013eca1.png)

-   In the **Configure Amazon Simple Storage Service** window, in the **Description** option name the service for example: “Budget S3 Object Lambda”, then **Choose the location type** to **Region**, and **Choose the region** in this case is US East (Ohio)

![A screenshot of a computer Description automatically generated](media/cb9f450d9e77afcc398ac754e1663b98.png)

-   In **Select S3 Storage classes and other features** choose **S3 Object Lambda** and **Data transfer**.

**![A screenshot of a computer Description automatically generated](media/3d142cfbc0d1a0532ab6df94fcfca855.png)**

-   In **S3 Object Lambda** add your own code to S3 GET requests to modify and process data as it is returned to an application. For the first time, you can use custom code to modify the data returned by standard S3 GET requests to filter rows, dynamically resize images, redact confidential data, and much more. Powered by AWS Lambda functions, your code runs on infrastructure that is fully managed by AWS, eliminating the need to create and store derivative copies of your data or to run expensive proxies, all with no changes required to applications.

    ![A screenshot of a computer Description automatically generated](media/6f9490877e830e535a4ad07898d339a0.png)

-   In **Data Transfer** enter the amount of inbound data transfer by TB or GB per month, same for outbound data transfer.

    ![A screenshot of a computer screen Description automatically generated](media/63b5ea7912c182a81db59f1b9c1dd2ec.png)

1.  **AWS Lambda**
-   In **find service** type **AWS Lambda** and choose the **configure** button.

    ![A screenshot of a computer Description automatically generated](media/e9d9781c04c21a904bbb9ab7f3151cca.png)

-   In the **Configure AWS Lambda** window, in the **Description** option name the service for example: “Budget S3 Object Lambda”, then **Choose the location type** to **Region**, **Choose the region** in this case is US East (Ohio), and Choose **Lambda Function – Include Free Tier.**

    **![A screenshot of a computer Description automatically generated](media/dfab61b8608c35b49ebbc9747682bce5.png)**

-   In **Service settings**, set the type of architecture, number of requests, duration of each request, the amount of memory of each request and the amount of ephemeral storage allocated.

    ![A screenshot of a computer Description automatically generated](media/e0594c70d9fb4addb076ceddd37b93f2.png)

-   **Provision Concurrency** also can be enabled for Lambda functions for greater control over the performance of your serverless applications. When enabled, Provisioned Concurrency keeps functions initialized and hyper-ready to respond in double-digit milliseconds. You pay for the amount of concurrency that you configure and for the period of time that you configure it.
-   **Lambda@Edge** currently is not free tier. You are charged for the total number of requests across all your functions. Lambda@Edge counts a request each time it starts executing in response to a CloudFront event globally.
-   **Lambda HTTP Response Streaming**, AWS Lambda functions can return an HTTP response stream when invoked via the InvokeWithResponseStream API or through a function URL using the ResponseStream invoke mode. When using HTTP response streaming, you are charged for each GB written to the response stream by your function. You can stream the first 6MB per request at no cost.
1.  **Amazon DynamoDB**
-   In **find service** type **AWS DynamoDB** and choose the **configure** button.

![A screenshot of a computer Description automatically generated](media/f9dc9a9b02194753a3a880970948abb3.png)

-   In the **Configure AWS DynamoDB** window, in the **Description** option name the service for example: “Budget Amazon DynamoDB”, then **Choose the location type** to **Region**, **Choose the region** in this case is US East (Ohio) and **Choose DynamoDB features** in this case **DynamoDB on-demand capacity**.

![A screenshot of a computer Description automatically generated](media/71078a3f3096dffab4e12453ca1f1295.png)

-   In **DynamoDB on-demand capacity feature**, DynamoDB offers two table classes designed to help you optimize for cost. The DynamoDB **Standard** table class is the default and recommended for the vast majority of workloads. The DynamoDB Standard-Infrequent Access (DynamoDB Standard-IA) table class is optimized for tables that store data that is accessed infrequently, where storage is the dominant cost. Each table class offers different pricing for data storage as well as read and write requests. You can select the most cost-effective table class based on your table’s storage requirements and data access patterns. Learn more about DynamoDB table classes in the DynamoDB Developer Guide.
-   
-   There are also options to specify **Data Storage** size, **On-demand write settings**, and **On-demand read settings**.

![A screenshot of a computer Description automatically generated](media/a06a8c72572e3e96fdf65cfbb5218149.png)

1.  **Amazon Simple Storage Service (S3) Standard**
-   In **find service** type **Amazon Simple Storage Service** and choose the **configure** button.

![A screenshot of a computer Description automatically generated](media/1cc31d592afb78d00ec300fd1013eca1.png)

-   In the **Configure Amazon Simple Storage Service** window, in the **Description** option name the service for example: “Budget Amazon S3”, then **Choose the location type** to **Region**, **Choose the region** in this case is US East (Ohio) and Choose in **Select S3 Storage Classes and other features** the **S3 Standard option.**

    ![A screenshot of a computer Description automatically generated](media/b1d2b84ff1e64b8372263ffeab6aeb1b.png)

-   In **S3 Standard feature** set the **S3 Standard** storage size and the unit to use per month. **S3 Standard** is best used for general-purpose of frequently accessed data.

    ![A screenshot of a computer Description automatically generated](media/a375ddc15b1187ee3f5122c5dafe5a31.png)

-   Calculations for 50GB storage

    ![A black text on a white background Description automatically generated](media/6b268f69ef3f80cae1061e75f6151c1f.png)

1.  **Amazon Athena**
-   In **find service** type **Amazon Athena** and choose the **configure** button.

    ![A screenshot of a computer Description automatically generated](media/a61581ba1944959999432f80487a6ba4.png)

-   In the **Configure Amazon Athena** window, in the **Description** option name the service for example: “Budget Amazon Athena”, then **Choose the location type** to **Region**, **Choose the region** in this case is US East (Ohio).

    ![A screenshot of a computer Description automatically generated](media/2a618e8f85c65ab816a09d02b000dd25.png)

-   Amazon Athena is a serverless, interactive analytics service built on open-source frameworks. Athena provides a simplified, flexible way to analyze petabytes of data where it lives. With Athena, you pay only for what you use. There are no upfront fees and no long-term commitments.
-   In SQL Queries windows, in SQL queries with per query pricing type the number of queries, the amount of data scanned per query and the unit of each option.

    **![A screenshot of a computer Description automatically generated](media/57025c1579567714da4f0e1a83e5b059.png)**

    **![A screenshot of a computer screen Description automatically generated](media/46f2b6353b14f0419ca096b9bab1fbb1.png)**

-   In Spark for Amazon Athena, you only pay for the time that your Apache Spark application takes to run. You are charged an hourly rate based on the number of data Processing Units (DPUs) used to run your Apache Spark application. A single DPU provides 4 vCPU and 16GB of memory.

    **![A screenshot of a computer Description automatically generated](media/8774ad4706252bbf422d57d582867a38.png)**

    **Conclusion**

    Here you will find a sample of a Budget using **AWS Pricing Calculator,** including the pricing of all the services we were using for this project. Please feel free to use it and update the content of this budget.

    [https://calculator.aws/\#/estimate?id=ef2bcb54bd9782531d5345a4cb1f2c1f21f19950](https://calculator.aws/#/estimate?id=ef2bcb54bd9782531d5345a4cb1f2c1f21f19950)

    ![A screenshot of a computer Description automatically generated](media/2b0926722effc59be57b00e98eb9950d.jpeg)
