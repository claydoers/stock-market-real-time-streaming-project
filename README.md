# Overview
The purpose of this project is develop and end to end solution using various tools that can stream stock market data in real time that can be used for reporting and analysis

# Technology
<li>Python - Functions for Producer and Consumer</li>
<li>Apache Kafka - Used to stream stock market data</li>
<li>AWS S3 - Data Lake/Object Storage</li>
<li>Amazon EC2 - Computing instance to run scripts</li>
<li>AWS Glue - Crawler to fetch new data as its added to S3</li>
<li>Amazon Athena - Serverless analytics service to run SQL</li>

# Architecture
![image](https://github.com/claydoers/stock-market-real-time-streaming-project/assets/109707159/6b38852f-e1a5-46fb-ae43-f0f8c425c387)

# Design/Development Process
<ol type="1">
  <li>Create a new EC2 instance to install Java & Kafka on</li>
  <li>Create new Kafka Topic, and start Producer & Consumer</li>
  <li>Develop Python scripts to pass data for each stock ticker to a data frame using pandas and upload to S3 in JSON format</li>
  <li>Design AWS Glue Crawler to crawl the bucket in the data lake to check for new data in real time</li>
  <li>Utilize Athena to confirm data counts are increasing on tables as data streams in real time to AWS S3 & gets ingested from the Glue Crawler</li>
</ol>
