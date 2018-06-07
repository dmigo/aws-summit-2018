# Data Challenges in an acquisition based world
**(or how to click a Data Lake together with AWS)**
*Daniel Manzke* Delivery Hero


## Hyperlocal approach
Situation: Accuised companies come with their tech stacks. Only the local teams know how to do business in their location.  

Nature of the data: Which data can we collect?  
    Order itself  
    Order delivery  
    SAP  
    Excel files  
    Surveys  


Solution: Build central DWH  
    Airflow, Redshift, S3  
    ETL all over the place  
    Standard Data Structures  

## Architecture

*Getting data:* API Gateway + bunch of Lambdas push data to Kinesis  
    Gateway - versioning, auth  
    Lambdas - scalability, validation  
*Processing & Consuming:* 
Kinesis -> Kinesis Streams -> Kinesis Firehose -> S3 (Glue + Athena on S3)  
                           -> Kinesis Analytics  
                           -> Amazon SNS -> Internet  
    Glue - detects schemas  
    SNS - Fanout Events  

*Plans:*
    APIs for Single & Batch jobs  
    Subscriptions  
    Replay of the data ???  



## Requirements

250k orderss per day  
5-10 Events per order  
*Gives ~1Gb/Day*
Consumption under 5secs  

## Resources

4 People  
3 Months  
500$ monthly  


## Visualisation
Live map looks great  
Customer ratings show up in live

## Conclusion
You can click DL together, you don't need to manage Kafka on your own. Delegate the hell out of it.  
Be aware of the limits.  
Push back for requirements in the beginning. Start small.  
**STEP 1: Start small, build only the generic stuff. STEP 2: Observe your consumers down the stream, learn patterns, automate**
