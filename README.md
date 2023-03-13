
# Predictive Modeling using Azure Machine Learning 

## Introduction 
In this project, I used various Azure services/resources to predict the likelihood of readmissions in diabetic patients. I was able to create visualizations of data to analyze correlation between values in a dataset 

## The Data 
I used a [dataset](https://archive.ics.uci.edu/ml/datasets/diabetes+130-us+hospitals+for+years+1999-2008#) of the medical history of diabetic patients compiled by a medical research team at VCU. This dataset was then uploaded to my Azure Blob storage account in csv format. The storage account was then mounted to my databricks notebook for analysis. This took a little bit of troubleshooting because my storage account needed to be a Data Lake Gen 2 enabled with specific settings in order to be mounted and used in Databricks. So, I ended up making a new storage account specifically for this project. 

## Databricks and Apache Spark 
Once my dataset was imported into my Databricks notebooks, I created a dataframe and cleansed my data by dropping unneeded columns and removing rows that met certain conditions. 

For example, I  
* Removed patients that were no longer with us using their discharge id 
* created additional columns to make age and number of previous readmissions integar values instead of strings

I then created tables for my analysis to find possible indicators using Pyspark SQL functions with basic SQL syntax. Once my tables were created I was able to create visualizations to identify trends. 

## Analysis
Before creating my tables, I need to find what factors might influence readmission. The factors were:
* race  

* gender 

* age 

* number of diagnoses 

* number of medications




