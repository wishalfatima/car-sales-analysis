
# Car Sales Analysis

Business Intelligence analysis of car sales and vehicle attributes using Python, Pandas, Jupyter Notebook, data modelling, and Tableau.

## Project Overview

This project explores the **Retail / Automotive Sales domain** by combining two car-related datasets to investigate vehicle sales, pricing, fuel efficiency, engine characteristics, and resale value.

The project follows a Business Intelligence workflow covering:

- Business question definition
- Data understanding
- Data transformation
- Data integration
- Data cleaning
- Data modelling
- Analytical exploration
- Business intelligence visualization
- Business-oriented interpretation of results

The analysis was developed as part of a **Business Intelligence** academic project.

## Business Questions

The analysis focuses on five main questions:

1. **How do car sales vary across different brands or models?**

2. **How does fuel efficiency relate to different car models?**

3. **Which car features have the greatest relationship with car sales?**

4. **How does engine power relate to car price and mileage?**

5. **Which vehicle types are associated with higher resale values?**

These questions were selected to support business decisions around pricing, sales strategy, customer preferences, manufacturing, marketing, inventory, and resale value. :contentReference[oaicite:4]{index=4} :contentReference[oaicite:5]{index=5}

---

## Datasets

Two datasets were used in the analysis.

### 1. German Car Insights

The German Car Insights dataset contains approximately **100,000 records and 15 columns**.

It includes information such as:

- Brand
- Model
- Color
- Registration date
- Year
- Price
- Power
- Transmission type
- Fuel consumption
- Mileage
- Offer description

### 2. Car Sales

The Car Sales dataset contains approximately **153 records and 16 columns**.

It includes information such as:

- Manufacturer
- Model
- Sales
- Year resale value
- Vehicle type
- Price
- Engine size
- Horsepower
- Wheelbase
- Vehicle dimensions
- Fuel information
- Launch date

The datasets were selected to provide complementary information about vehicle characteristics, sales, pricing, and resale value. :contentReference[oaicite:6]{index=6}

---

## Data Processing

Data preparation was performed using **Python, Pandas, and Jupyter Notebook**.

The processing workflow consisted of three main stages:

### Data Transformation

- Loaded the datasets from CSV files
- Identified primary keys
- Established relationships using foreign keys
- Loaded the datasets into Pandas DataFrames
- Inspected the structure and initial records
- Removed irrelevant attributes
- Removed unnecessary columns such as `Unnamed: 0`
- Removed attributes such as `Latest Launch` and `Simplified Model` where appropriate

### Data Integration

The datasets were integrated to support the BI data model.

Key steps included:

- Comparing manufacturer and model values across datasets
- Standardizing model naming where necessary
- Using inner joins to reduce non-matching records
- Recreating dimension data from the merged dataset
- Creating additional dimension tables
- Preparing data for Tableau analysis

The resulting model included dimensions such as:

- `Dimension_Car`
- `Dimension_Date`
- `Dimension_Fuel`

### Data Cleaning

The datasets contained missing values and inconsistent data types.

Cleaning included:

- Identifying missing values
- Filling missing numerical values using the median
- Filling missing categorical values such as color using the mode
- Converting `power_kw` and `power_ps` into numeric values
- Cleaning and converting `price_in_euro` into numeric format
- Handling values affected by conversion errors

These steps prepared the datasets for analysis and visualization. :contentReference[oaicite:7]{index=7} :contentReference[oaicite:8]{index=8}

---

## Data Modelling

Two modelling approaches were used.

### Entity Relationship Diagram

An ERD was developed to represent relationships within the source data.

The model considers entities and attributes related to:

- Cars
- Manufacturers
- Models
- Colors
- Fuel

The ERD was used as the foundation for understanding relationships before developing the BI model.

![Entity Relationship Diagram](ERD.jpg)

### Star Schema

A dimensional model was designed for Business Intelligence analysis.

The central fact table is:

**Fact Table**

- `Car_Sales_Fact`

The model includes dimensions such as:

- `Dimension_Car`
- `Dimension_Date`
- `Dimension_Fuel`
- `Dimension_Mileage`
- `Dimension_Yearly_Resale_Value`

![Star Schema](Star%20Schema-Final.png)

---

## Analytics & Visualization

The prepared data was analysed using **Tableau**.

The analysis focused on the five business questions defined at the beginning of the project.

Visual analysis included:

- Car sales by brand/model
- Car price and fuel efficiency relationships
- Relationships between vehicle features and sales
- Engine power compared with price and mileage
- Vehicle type compared with yearly resale value

The Tableau analysis was used to transform the prepared datasets into business-oriented insights.

---

## Key Findings

The analysis identified several important patterns:

- **Ford F-Series** showed the highest sales volume among the models examined.
- Higher-priced vehicles generally showed lower fuel efficiency.
- Vehicle characteristics such as engine size and horsepower showed relationships with sales across manufacturers.
- Passenger vehicle types showed higher resale values in the analysed data.

These findings can support discussions around:

- Pricing strategy
- Marketing strategy
- Manufacturing decisions
- Inventory management
- Customer preferences
- Sales planning
- Resale value analysis

The project report specifically identifies manufacturing, marketing, pricing, inventory management, and sales forecasting as potential areas where the analysis could support decision-making. :contentReference[oaicite:9]{index=9}

---

## Challenges

Several data quality and integration challenges were encountered:

- A large number of missing values
- Inconsistent data organization
- Numeric values stored as strings
- Difficulties establishing relationships between primary and foreign keys
- Differences in manufacturer and model naming across datasets

These challenges required additional data cleaning, transformation, and integration before the data could be used effectively for BI analysis. :contentReference[oaicite:10]{index=10}

---

## Business & Process Analysis Perspective

Although this is a Business Intelligence project, it demonstrates several skills relevant to **Process Analyst, Business Analyst, and Data/BI Analyst roles**.

The project demonstrates experience with:

- Translating business questions into analytical requirements
- Understanding a business domain
- Identifying relevant business entities and relationships
- Working with structured and semi-structured data
- Data quality assessment
- Data cleaning and transformation
- Data integration
- Entity Relationship modelling
- Dimensional modelling
- Designing a BI-oriented star schema
- Turning data into business insights
- Communicating findings to support decision-making

The project therefore demonstrates not only technical data skills, but also the ability to move from **business questions → data → analysis → actionable insights**.

---

## Tools & Technologies

| Tool / Technology | Purpose |
|---|---|
| Python | Data processing and transformation |
| Pandas | Data manipulation and cleaning |
| Jupyter Notebook | Data preparation and analysis |
| Tableau | Business intelligence visualization |
| CSV | Source and processed datasets |
| ERD | Source data modelling |
| Star Schema | BI dimensional modelling |

---

## Repository Structure


car-sales-analysis/
│
├── Data Processing for Tableau Using Python.ipynb
│   └── Data transformation, integration, and cleaning workflow
│
├── car_sales_df.csv
│   └── Car sales dataset
│
├── gcar_data_df.csv
│   └── German car dataset
│
├── ERD.jpg
│   └── Entity Relationship Diagram
│
├── Star Schema-Final.png
│   └── BI star schema
│
└── README.md
    └── Project documentation

---

## Reproducibility

The main data preparation workflow is available in:

`Data Processing for Tableau Using Python.ipynb`

The notebook documents the major data transformation, integration, and cleaning steps performed before the BI analysis.

The CSV files included in the repository provide the datasets used during the project workflow.

---

## Future Improvements

Possible improvements include:

* Use larger and more recent datasets
* Improve the consistency of relationships between datasets
* Perform additional statistical analysis
* Investigate predictive modelling for sales forecasting
* Add more interactive Tableau dashboards
* Validate findings with automotive domain experts
* Incorporate additional business and market variables
* Extend the analysis to support more detailed forecasting and decision-making

The project report also identifies larger datasets and domain-expert validation as areas for future improvement. 

---

## Project Context

This project was completed as part of an academic **Business Intelligence** assignment.

The work covered data research, analytical question development, data modelling, Jupyter/Pandas processing, Tableau analysis, and reporting. 




