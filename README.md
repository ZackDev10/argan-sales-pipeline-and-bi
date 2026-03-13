# 🌿 Argan Cooperative Sales Analytics: End-to-End Data Pipeline & Dashboard

### 📊 Project Overview

This project transforms raw, unstructured sales data from a Moroccan Argan oil cooperative into an interactive, executive-level Power BI dashboard. As a Database Developer and SQL Specialist, my goal with this analysis is to demonstrate rigorous data integrity, programmatic data modeling, and the ability to surface actionable business intelligence regarding revenue streams, customer purchasing behavior, and regional sales distribution across the Souss-Massa region.

### 🛠️ Tech Stack & Tools

* **Data Cleaning & Preprocessing:** Python (Pandas, NumPy)
* **Exploratory Data Analysis (EDA):** Python (Matplotlib, Seaborn)
* **Data Visualization & BI:** Power BI, DAX (Data Analysis Expressions)

### 🧹 The 8-Step Data Cleaning Pipeline

Real-world data is messy. To ensure accurate reporting and prepare the data for downstream database ingestion, I engineered a robust Python pipeline to preprocess the raw CSV before importing it into Power BI. The pipeline includes:

1. **Header Standardization:** Normalizing column names for programmatic access.
2. **Currency & Type Conversion:** Stripping text/symbols from MAD financials and casting to floats.
3. **Categorical Cleaning:** Standardizing text casing and converting to memory-efficient `category` dtypes.
4. **Boolean Mapping:** Creating clean logical flags for B2B vs. B2C sales.
5. **Date Parsing:** Coercing varied date strings into standard `datetime` objects.
6. **Logical Integrity Checks:** Validating physical possibilities (e.g., dropping negative quantities and verifying `Price * Quantity = Revenue`).
7. **Outlier Handling:** Applying the IQR (Interquartile Range) method to cap extreme wholesale anomalies via Winsorization.
8. **String Parsing:** Extracting volumetric data (e.g., pulling "250" out of "Argan Oil 250ml") using Regex for granular product analysis.

### 📈 Key Business Insights

Based on the executive dashboard, the cooperative exhibits strong financial health and clear market trends:

* **High-Volume Profitability:** The cooperative processed **50,000 total orders**, generating **211M MAD** in total revenue with a highly healthy **33.48% overall profit margin** (yielding **70.65M MAD** in total profit).
* **Brick-and-Mortar Dominance:** Physical shop sales massively outperform the online channel across all customer segments (Tourist, Retailer, and Local).
* **Regional Concentration:** Geographic mapping confirms that the bulk of revenue remains heavily concentrated around the Agadir and Marrakesh distribution hubs.
* **Seasonal Volatility:** Time-series analysis reveals distinct peaks and valleys in monthly revenue, indicating strong seasonal purchasing behaviors that should dictate future inventory and supply chain planning.

### 🖼️ Executive Dashboard

![Dashboard Preview](../dashboard/dashboard.png)
