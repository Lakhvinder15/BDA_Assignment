# Big Data Analytics Assignment: Cloud-Based Big Data Analytics with Apache Spark and Hadoop Ecosystem

## Overview
This repository contains the implementation and documentation for a Big Data Analytics assignment focused on processing and analyzing Amazon customer reviews using Apache Spark and Hadoop in a cloud environment. The project demonstrates data ingestion, processing, advanced analytics, and machine learning to derive business insights.

## Introduction
The project explores the practical implementation of Apache Spark and Hadoop in a cloud environment (AWS EMR, Google Dataproc, or Azure HDInsight) to process and analyze large-scale Amazon customer reviews (>10 GB). The study highlights the role of Big Data in decision-making, compares MapReduce and Spark performance, and extracts business insights through sentiment analysis, customer behavior analysis, and predictive modeling.

## Problem Definition and Business Context
With the rise of e-commerce, customer feedback has become crucial for improving products and services. This project addresses the challenge of analyzing large volumes of unstructured Amazon reviews to derive actionable insights, such as sentiment trends, fraudulent review detection, and product recommendations.

## Cloud Environment Setup and Data Ingestion
- **Cluster Configuration**: A Dataproc cluster was set up with a master node (`n1-standard-2`) and worker nodes (`n1-standard-1`).
- **Data Ingestion**: The dataset was copied from Google Cloud Storage to the master node and uploaded to HDFS for distributed processing.

## Data Processing with Spark and Hadoop
### Hadoop MapReduce
- **Functionality**: Tokenized reviews, counted word frequencies, and flagged anomalies (e.g., missing/short reviews).
- **Output**: Identified 20 most common words (e.g., "the," "I", and "and") and 7,459 anomalies.

### Apache Spark
- **Exploratory Data Analysis (EDA)**: Analyzed schema, filtered null/short reviews, and performed word frequency analysis.
- **Key Findings**:
  - Top-rated products had perfect 5.0 ratings.
  - Verified reviews (627,809) significantly outnumbered unverified ones (66,260).
  - Most helpful reviews had high engagement (e.g., 646 helpful votes).

### Performance Comparison
| Criteria          | MapReduce                          | Spark                              |
|-------------------|------------------------------------|------------------------------------|
| Speed             | Slower (disk-based processing)     | Faster (in-memory processing)      |
| Scalability       | High disk overhead                 | Efficient scaling                  |
| Ease of Use       | Complex (Java-based APIs)          | User-friendly (Python/Scala APIs)  |
| Fault Tolerance   | High recovery times                | Efficient (RDD lineage tracking)   |
| Use Case          | Batch processing (e.g., ETL)       | Real-time analytics, ML            |

## Advanced Analytics and Machine Learning
### Sentiment Analysis
- **Preprocessing**: Converted ratings to binary sentiment (1 for positive, 0 for negative).
- **Feature Engineering**: Tokenized text and removed stop words.
- **Model Training**: Logistic Regression achieved 83% accuracy.

### Business Insights
1. **Sentiment Trends**: Identified frequently praised/complained features for product improvement.
2. **Fraud Detection**: Flagged fake reviews to maintain platform credibility.
3. **Market Trends**: Analyzed consumer preferences for inventory and marketing optimization.
4. **Verified Reviews**: Highlighted authentic customer experiences for trust-building.
5. **Recommendations**: Improved personalized suggestions using ML models.

## Concluding Remarks
The project demonstrates the effectiveness of Big Data analytics in extracting actionable insights from customer reviews. By leveraging Apache Spark and Hadoop, businesses can enhance decision-making, improve customer satisfaction, and drive revenue growth in competitive markets.

## Dataset**: [Amazon Reviews Data 2023](https://www.kaggle.com/datasets/wajahat1064/amazon-reviews-data-2023)
