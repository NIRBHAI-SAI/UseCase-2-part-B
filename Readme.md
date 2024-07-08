# USE CASE 2

## Problem Statement

### 1. Logging Extension for FileScanner Application (UseCase 1)

The audit logs of a PostgreSQL database are essential for understanding database activity, user actions, and potential security events. However, directly monitoring these logs within the database can be time-consuming, inefficient, and lacking in advanced visualization features.

This project will address these issues by transferring shipping logs from a PostgreSQL database to Kibana, using Logstash as a data transport mechanism and Elasticsearch for indexing. The goal is to offer a more efficient, real-time, and visually appealing monitoring system.

### 2.Detect Change in Configuration Files

A configuration file for a Beats application controls the inputs and destinations of logs that it is capable of sending. Any changes in the config file can alter the outcome drastically. Working on a cluster with many active nodes makes it practically difficult to reach the node and check the status to config file.

In this use case, we aim to create a set of rules to detect changes in the configuration file of a beat application, such as Winlogbeat or Filebeat.


- Kibana : Monitoring the Logs.
- WinlogBeat - To monitor windows Log events.

# 1. Logging Extenstion

### Approach
![Flow chart of Approach](image.png)

As the logs of FileScanner are Stored in Audit Table of PostgreSQL Database they need to be ingested by Logstash on a scheduled basis and sent to Elastic Search for indexing.
These logs are collected at kibana for better visualisation. 

### Tech Stack

- Postgre SQL : Data Base for Audit Table.
- LogStash : To ship logs from Audit Table.
- ElasticSearch : To index the logs comming from Logstash.
### Set up

#### Elastic Search

- After [dowloading](https://www.elastic.co/downloads/elasticsearch) and unziping the ElasticSearch Application.
- Assign roles in roles.yml file present in config directory of elastic search.
- open command prompt as Admin and add
- Setup in built users like "elastic" and "kibana_systems" in the elastic.

