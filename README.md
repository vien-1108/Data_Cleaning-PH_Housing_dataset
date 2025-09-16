# 🏡 PH Housing Dataset — Data Cleaning & Preparation

This repository contains the **data cleaning, transformation, and preparation steps** performed on the **Philippine Housing Dataset** to make it ready for analysis and visualization.

## 📑 Project Overview
The dataset contains various property listings across the Philippines, including details like price, location, number of bedrooms, floor area, lot area, and descriptions.  
The main objective of this project was to **clean, standardize, and enrich the data** so that it can be used for insights and visualizations such as **price trends, location-based comparisons, and property type analysis**.

## 🎯 Goals
- Remove duplicates and ensure data integrity  
- Handle missing values appropriately  
- Extract new features (Project, Property Type, Storeys) from description text  
- Standardize formats (price, city/province names, column ordering)  
- Prepare dataset for easy visualization in Tableau, Power BI, or Python  

## 🧹 Data Cleaning Steps
### 1️⃣ Handling Missing Values
- Identified missing values in `Price`, `Project`, `Latitude`, and `Longitude`
- Left missing prices blank (no imputation) to preserve accuracy
- Ensured `City/Province` and `Location` were consistently populated

### 2️⃣ Removing Duplicates
- Removed duplicate listings based on `Description + Location + Price`
- Kept first occurrence to prevent skewed counts
- Reduced noise and improved reliability of insights

### 3️⃣ Standardizing Formats
- Converted `Price` to float, formatted into `₱X,XXX,XXX.00` (Accounting Style)
- Removed decimals from number of bedrooms
- Cleaned and capitalized `City/Province` and `Project` names
- Removed leading "in", "at", "by" in project names
- Extracted `Property Type`, `Storeys`, `Project` from `Description`
- Reordered columns into a logical, analysis-friendly order: House ID → City/Province → Location → Latitude → Longitude →
Project → Property Type → Storeys → Bedrooms → Bathrooms →
Floor Area → Land Area → Price (PHP) → Description

### 4️⃣ Validating Data Integrity
- Checked for negative or zero prices (none found)
- Verified numeric columns are within realistic ranges
- Flagged rows with missing prices for future review

### 5️⃣ Additional Enhancements
- Created a separate numeric `Price_Value` column for computation
- Left `Price (PHP)` as formatted for readability
- Dataset now ready for direct import into visualization tools

## 📊 Insights from Cleaning
- Property prices vary widely by location, confirming location as a primary price driver
- Extracted `Project` and `Property Type` enable segmentation by developers and house types
- Missing price entries are likely preselling units or "contact for price" listings
- Dataset now supports advanced analysis such as price distribution, project-level comparisons, and city-based visualizations

## 🚀 Next Steps
- Build Tableau or Power BI dashboards for:
- Price heatmaps by city/province
- Property type distribution charts
- Project-level price comparison
- Potentially geocode missing Latitude/Longitude for more accurate mapping

## 🧑‍💻 Tech Used
- **Python** (pandas, regex) for data cleaning and transformations
- **Jupyter Notebook** for step-by-step processing and validation

## 👤 Author
**Group:** DataViz Group 9
- Vivienne Rose Rates
- Kate Iris Dataylo
- Kyle Gabriel Tubera
- Stephen Dave Campillanes

---

## 📌 Summary
This repository provides a **clean, well-structured, and analysis-ready** version of the PH Housing Dataset, making it suitable for academic projects, market research, and visualization dashboards.
