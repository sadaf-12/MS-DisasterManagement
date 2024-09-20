# MS-DisasterManagement
My MS Final Project for Cloud based Disaster Management (SaaS) through Tweets Sentiment Analysis

This repository includes Azure resource group information with all the necessary resources, such as 'Infrastructure as a Code (IaaC)' in the ExportedTemplate-TweetsIngestion.zip.
This zip folder contains parameters and templates that are used as JSON files.

The project uses Azure Databricks to perform Sentiment Analysis.
Scala (code) notebook is saved as Sentiment Analysis.dbc (Databrick Archive).

Below are the steps to deploy this project back to Azure:

1. Upload the ExportedTemplate-TweetsIngestion.zip to Azure portal
2. Test run the EventsHub _(TweetsIng)_, StreamAnalytics Job _(tweets-stream-cosmos)_ (_note: this project uses Cosmos DB_)
3. Run the StreamAnalytics Job **_tweets-stream-cosmos_**
4. Open the Azure Databricks workspace and setup _**compute**_ instance with _**Apache Spark 3.5.0, Scala 2.12**_
5. The libraries required are detailed later
6.   
7. Upload the Sentiment Analysis.dbc file which will open the Scala Notebook for tweets ingestion and sentiment analysis

The following libraries are required for this project:

_1. Azure Cosmos DB Connector for Spark_
    Maven: com.azure.cosmos.spark:azure-cosmos-spark_3_5_2:4.33.1
_2. Azure Messaging Event Hubs_
    Maven: com.azure:azure-messaging-eventhubs:5.18.6
_3. John Snow Labs NLP (GPU version)_
    Maven: com.johnsnowlabs.nlp:spark-nlp-gpu_2.12:3.0.1
_4. Azure Event Hubs Connector for Spark_
    Maven: com.microsoft.azure:azure-eventhubs-spark_2.12:2.3.18
_5. Play JSON Library_
    Maven: com.typesafe.play:play-json_2.12:2.10.6
_6. JSON4S Core_
    JAR: json4s-core_2.12-4.0.3.jar

