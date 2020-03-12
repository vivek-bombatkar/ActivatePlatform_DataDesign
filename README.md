# Activate Platform - Data Design

- ['S'ituation](#10) 
- ['T'asks](#20) 
- ['A'ction](#30) 
- ['R'esult](#40) 


# <a name="10"></a>Situation   
<img src="./pics/Activate Platform Spider diagram.jpeg"  />


# <a name="20"></a>Tasks

***1. Data Organization.***  
<img src="./pics/DataOrganization_DetailedFlowchart.jpeg"  />

  - 'Activate' have 2 types of data ingestion; Realtime and Batch
  - Realtime Ingestion will be for 1st party data, coming from the device every 5 seconds or on the event.
  - Further Data pre-process happen before data stored in persistent cloud storage. 
  - Data Partition and Bucketing are important strategies for 'Segmentation' queries and keys for theses needs to be decided after studying schema.
  - Tools for data discovery and metadata management service need to setup.

  
  
  

***2. Output KPIs and analytics.***  
<img src="./pics/kpi_table.png"  />

  - Generic KIP table to store KIP from all the segments. 
  - Partition strategy put in place to efficiently fetch KIP. 



***3. Lookalike Model***
   - A graph like structure could be though to achieve connections between segments.
   - Or perhaps a Recommendation algorithm could be developed to learn patterns in segment usage.
   
   

# <a name="30"></a>Action

***Activate Platform - Cloud Implementation ***
<img src="./pics/ActivatePlatform-CloudImplementation2.png"  />

  - Services from 'Google Cloud Platform' is considered while designing this solution, but this could be easily replaced by AWS services.
  - 'Apache Spark' will be the choice of the technology for data ingestion and processing for both batch and realtime.
  - File-based storage could be ideal for this solution, with storage formats like AVRO.
  - Most of the 'tricky' functionality could be achieved using Cloud Native services.
  - Ex. Storing the results of segments for some period of time, so that next time effort could be saved. This will be is achieved using Google BigQuery's persistent-query-result functionality.
 


# <a name="40"></a>Result
- We have developed a cloud-native solution with most of them out of the box and battle-tested technologies.
- Due to this provided solution is highly scalable and elastic. Adding more processing resources and slashing down clusters when not in use could be accomplished. 
- SaaS cloud products also offer a cost-effective pricing strategy.
- Apache Spark is ideal for batch and realtime needs for Bigdata application.


