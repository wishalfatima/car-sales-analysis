Car Sales Analysis
Project Overview
This project is a Business Intelligence (BI) analysis in the Retail (Sales) Domain.
It explores two real-world car datasets to uncover insights about pricing, fuel efficiency,
engine power, sales trends, and vehicle resale values using Python and Tableau.

📂 Datasets Used
Dataset                  Source          Size
German Car Insights   Kaggle~       100,000 entries, 15 columns
Car Sales              Kaggle~        153 entries, 16 columns

❓ Analytical Questions

How do car sales vary across different brands or models?
How does fuel efficiency relate among different car models?
Which features of the car have more impact on car sales?
How does engine power relate to car price and mileage?
Which vehicle types are associated with higher resale values?


🛠️ Data Processing
Data Transformation

Downloaded datasets as CSV files
Identified Primary Keys and created relationships using Foreign Keys
Loaded datasets into Jupyter Notebook using Pandas
Removed irrelevant attributes (e.g., Unnamed: 0, Latest Launch, Simplified Model)

Data Integration

Merged datasets using inner joins to eliminate non-matching entries
Created Dimension tables: Dimension_Car, Dimension_Date, Dimension_Fuel
Standardized manufacturer and model names across both datasets

Data Cleaning

Identified and handled missing values
Filled missing numerical values using median
Filled missing categorical values (e.g., color) using mode
Converted power_kw and power_ps to numeric by removing non-numeric characters
Converted price_in_euro to numeric format


🗃️ Data Modeling

ERD Model — Source data relationships with entities: Car, Manufacturer, Color, Fuel
Star Schema — BI data model with:

Fact Table: Car_Sales_Fact
Dimensions: Dimension_Car, Dimension_Date, Dimension_Fuel, Dimension_Mileage, Dimension_Yearly_Resale_Value


📊 Data Analytics & Visualizations
All visualizations were created in Tableau:

Q1 — Bar chart: Car Sales vs Brand/Model
Q2 — Scatter plot: Car Price vs Fuel Efficiency
Q3 — Multi-panel scatter: Car features (Curb weight, Engine size, Horsepower) vs Sales
Q4 — Scatter plot: Engine Power vs Price and Mileage
Q5 — Bar chart: Vehicle Type vs Year Resale Value


🔧 Tools & Technologies
ToolUsagePythonData processing & cleaningPandasData manipulationJupyter NotebookDevelopment environmentTableauData visualization & analytics

📁 Project Structure
car-sales-analysis/
├── data/               # Raw and processed CSV files
├── images/             # Tableau visualization screenshots
├── notebook/           # Jupyter Notebook (.ipynb) with full code
└── report/             # Project presentation/report

💡 Key Findings

Ford F-Series had the highest sales volume among all models
Higher-priced cars generally show lower fuel efficiency
Engine size and horsepower have notable impact on sales across manufacturers
Passenger vehicle types tend to have higher resale values than regular cars


⚠️ Difficulties Encountered

Large number of missing values in both datasets
Data was not consistently organized
Some numeric values were stored as strings and required conversion
Limited relationships between primary and foreign keys across datasets


🔮 Future Improvements

Use larger datasets for more accurate and reliable results
Conduct domain expert validation for real-world applicability
Further refine the analysis for better business decision-making
