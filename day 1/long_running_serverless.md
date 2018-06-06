# Long Running Serverless Apps
*Marcos Rebelo & Abdullah Odibat* from home24

## Overview
**Why not L?**
 > 5 mins 
 Small tmp directory size
 JAR size is a problem with Spark standalone

**Why not EMR?**
 No distinct jobs for different jobs
 Expensive


**Limits for the Batch Serivce**
 Single machine
 Hardware

**AWS Batch Service**
 Built on ECS
 *Concepts:*
  Queue
  Environment
   AMI
   EC2 Instance
   Pricing
   Network
  Job
   Command to run
   Queue
   Dependencies between jobs

## home24 implementation
Recommendation Engine

**Step 2**:
 1 small machine
 1 hour to finish
 
**Step 2**:
 40 jobs
 4x machine
 20 hours to finish

 challenges:
    sync
    alarms
    parallelize

## Techs
 Lambda
 AWS Batch
 AWS Step-Function
 SQS Notify
 CloudWatch
 Resource Groups Tagging API

## References


## Resumee
 Good presentation from people having their hands dirty in serverless.
 