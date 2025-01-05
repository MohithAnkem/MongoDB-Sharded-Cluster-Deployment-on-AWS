# MongoDB-Sharded-Cluster-Deployment-on-AWS
Project Developed for CS 157C No SQL Class

Project Overview

This project demonstrates the setup of a MongoDB sharded cluster with high availability and scalability using AWS EC2 instances. The cluster consists of three shards, one mongos router, and a replica set of three config servers. Each shard is configured with three-member replica sets to ensure fault tolerance and data redundancy.

Tasks Completed

# 1. Node Setup in AWS

Launched 9 AWS EC2 instances to host the MongoDB cluster components.

Configured security groups with appropriate inbound and outbound rules.

# 2. SSH Access to Instance

Accessed each EC2 instance securely using SSH and the provided .pem key file.

# 3. MongoDB Installation 

Installed MongoDB on all EC2 instances by configuring the MongoDB repository and using package managers.

# 4. Database Directory Setup

Created dedicated directories on each node to store MongoDB database files.

# 5. IP Address Configuration

Documented public and private IP addresses of all AWS instances used in the cluster.

# 6. Config Server Replica Set

Set up three config servers in a replica set.

Verified replica set configuration using rs.status().

# 7. Mongos Configuration

Connected the mongos router to the config server replica set.

Verified the mongos connection to all config servers.

# 8. Shard Setup 

Configured three shards, each consisting of a three-member replica set.

Verified shard replica sets using rs.status().

# 9. Adding Shards 

Added all three shards to the cluster using the mongos router.

Verified the cluster configuration using sh.status().

# 10. Shard Key and Sharding Strategy 

Enabled sharding with a hash-based shard key for data distribution.

Explained the rationale for using hash-based sharding to ensure even data distribution across shards.

# 11. Data Population 

Populated the cluster with data using a public dataset.

Dataset: https://www.kaggle.com/datasets/shrashtisinghal/mongo-db-datsets?select=grades.json

Included code and scripts for data import.

Verified data distribution across shards using sh.status().

# 12. Query Execution

Executed the following queries and recorded results, execution times, and the shard serving the query:

Range Query: Querying documents within a specified range.

$elemMatch Query: Filtering documents based on multiple conditions.

$in/$nin/$all Query: Searching documents with specified values.

Aggregate Query: Performing data aggregation using MongoDB pipelines.

Update Query: Modifying documents in the collection.

Delete Query: Removing documents from the collection.

# 13. Replica Set Verification

Verified shard replication status using rs.status().

# 14. Host Configuration Summary

Listed all hosts along with the services deployed on each instance, including primary and secondary roles.

# Documentation and Proof of Completion

The detailed process and results, including screenshots, are provided in the project documentation file (MongoDB_Cluster_Setup_Report.docx). The document includes:

Step-by-step setup procedures

Configuration details

Query results and execution times

Verification commands output

Tools and Technologies Used

AWS EC2: For deploying MongoDB instances.

MongoDB: Database platform for sharded cluster deployment.

SSH: Secure remote access to instances.

Ubuntu OS: Operating system for EC2 instances.

Public Dataset: Used to populate the database for testing queries.

# Instructions to Run

Clone the repository.

Review the MongoDB_Cluster_Setup_Report.docx for setup instructions and details.

Follow the steps mentioned in the document to recreate the cluster or analyze the commands used.
