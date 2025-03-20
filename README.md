# Weather and Sales Trend Pipeline
Weather and sales trend end-to-end pipeline using Snowflake

## Overview
This project demonstrates an end-to-end data pipeline that integrates weather data with sales trends using **Snowflake** for data storage and processing. The pipeline is structured into three main phases: **Ingestion, Transformation, and Delivery**. A **Streamlit** application is provided to visualize and analyze the processed data.

## Architecture

1. **Ingestion**
   - Create necessary databases, schemas, and tables in **Snowflake**.
   - Define external **stages** and **file formats** for structured data ingestion.
   - Load weather and sales data from an **S3 bucket** into Snowflake using `COPY INTO` commands.

2. **Transformation**
   - Process raw data into structured **harmonized** and **analytics** schemas.
   - Create **views** to integrate weather and sales data for city-based trend analysis.
   - Implement **User-Defined Functions (UDFs)** for data conversion, such as **Fahrenheit to Celsius** and **inches to millimeters**.
   - Aggregate and normalize weather and sales trends, focusing on **Hamburg, Germany**.

3. **Delivery**
   - Expose transformed data through Snowflake **views** for easy querying.
   - Develop a **Snowflake Streamlit app** to visualize weather and sales trends.
   - Use **Altair charts** in Streamlit to present interactive data insights.

## Folder Structure

```
📂 weather_sales_pipeline
│-- 📂 ingest               # SQL scripts for data ingestion
│   │-- copy_into.sql       # SQL script for loading data into Snowflake
│   │-- tasty_bytes.sql     # SQL script for database, schema, and table creation
│-- 📂 transform            # SQL scripts for data transformation
│   │-- hamburg_sales.sql   # SQL script for sales trends in Hamburg, Germany
│   │-- udf.sql             # SQL script for user-defined functions
│   │-- updated_hamburg.sql # SQL script for applying UDFs and advanced transformations
│-- 📂 delivery             # Streamlit app for data visualization
│   │-- streamlit.py        # Streamlit application code
│-- 📜 README.md            # Project documentation
```

## Streamlit App (Delivery)

The Streamlit app was created in **Snowflake** using Python to visualize daily sales and weather trends for Hamburg, Germany.

![Weather and Sales Trends for Hamburg, Germany](https://github.com/gloryodeyemi/Weather_and_Sales_Trend_Pipeline/blob/main/delivery/weather_sales_trend_chart.png)

## Setting up on Snowflake

1. Create a **Snowflake** account.
2. Run the SQL scripts in the following order:
   - `ingest/copy_into.sql` to create the database, schemas, and raw tables.
   - `ingest/tasty_bytes.sql` to create structured schemas and views.
   - `transform/hamburg_sales.sql`, `transform/udf.sql`, and `transform/updated_hamburg.sql` to process and aggregate data.
3. Create a Streamlit app and run the **streamlit.py** script.

## Usage

- Use the Streamlit dashboard to explore weather and sales trends.
- Modify SQL scripts to adapt the pipeline to new datasets or custom transformations.

## Future Improvements

- Automate data ingestion using **Snowflake Snowpipe**.
- Integrate **machine learning** to predict sales trends based on weather conditions.

## Connect With Me
Do you have an opportunity for me or want to collaborate? You can connect with me on [LinkedIn](https://www.linkedin.com/in/glory-odeyemi/).
