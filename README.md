# E-commerce Database Management Project

This project focuses on managing an E-commerce dataset using MongoDB for storage, Python for UI, Apache Spark for analysis, and PowerBI for data visualization.

## Prerequisites

- Spark (scala)
- MongoDB
- PowerBi desktop
- Pymongo

## Overview

- **Dataset**: E-commerce dataset containing 17 attributes, including order details, customer information, product details, and sales information.
- **Database Name**: ecommerce
- **Collection Name**: project

## Setup Instructions

### 1. Loading Dataset into MongoDB

- Use MongoDB and create a database named `ecommerce` and a collection named `project`.
- Data types for attributes:
    - `order_id`: string
    - `customer_id`: string
    - `timestamp`: string
    - `customer_city`: string
    - `customer_state`: string
    - `quantity`: int32
    - `price_MRP`: double
    - `payment`: double
    - `payment_type`: string
    - `payment_installments`: int32
    - `product_id`: string
    - `product_category`: string
    - `rating`: int32
    - `seller_id`: string
    - `seller_city`: string
    - `seller_state`: string
    - `order_status`: string

### 2. Connecting Python UI to MongoDB

- Install `pymongo`.
  ```python
  pip install pymongo
- UI consists of `index.html` and `dashboard.html`.
- Ensure attribute data types in `index.html` match MongoDB specifications to avoid errors.

### 3. Adding Data to MongoDB

- Run `data.py` to add data to the database.

### 4. Setting up Apache Spark for Analysis

- Download the Apache Spark connector for Spark and MongoDB from [MongoDB Spark Connector Documentation](https://www.mongodb.com/docs/spark-connector/current/).
- Add required dependencies in `build.sbt` for IntelliJ integration:

```scala
libraryDependencies ++= Seq(
  "org.apache.spark" %% "spark-core" % "3.2.0",
  "org.apache.spark" %% "spark-sql" % "3.2.0",
  "org.mongodb.spark" %% "mongo-spark-connector" % "3.0.1"
)
```

- Run `Spark_analysis.scala` to perform analysis after following all preceding steps.
- You can also check on some of the analysis i performed in MongoDB in `mongoDB-analysis.txt`

### 5. Data Visualization in PowerBI

- Download the MongoDB ODBC connector and BI connector from [MongoDB PowerBI Connector Documentation](https://www.mongodb.com/docs/bi-connector/current/connect/powerbi/).
- Load the database into PowerBI following instructions in the provided [YouTube link](https://www.youtube.com/watch?v=mGYB2u3okDk&t=105s).
- Refer to `datavisual.pbix` for visualization of analysis results.

## Note

Ensure to follow each step meticulously to set up the database, perform analysis, and visualize data accurately.

Feel free to reach out to me via [LinkedIn](https://www.linkedin.com/in/a-venkata-sai-krishna-varun-060304247/) for any clarifications or collaboration.


---

