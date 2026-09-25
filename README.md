# Canadian Labour Market Analysis — Power BI

## Overview

This project is an interactive Power BI dashboard analysing the Canadian labour market from **2021 to 2025**.

The dashboard brings together information on employment, unemployment, wages, industries, age groups, gender, provinces, and Census Metropolitan Areas (CMAs).

The goal of the project was to transform publicly available Statistics Canada data into an interactive report that allows users to explore labour-market trends at the national, provincial, and CMA levels.

---

## Key Insights

- Canada's unemployment rate decreased from **7.50% in 2021 to 6.42% in 2025**, a decrease of **1.08 percentage points**.
- The average hourly wage increased from 2021 to 2025 by **$4.83**, reaching **$29.46 in 2025**.
- Provincial unemployment trends varied considerably, with some provinces experiencing increases while others experienced decreases.
- Differences in unemployment can be explored by **age group, gender, industry, province, and CMA**.
- Wage analysis shows differences across age and gender groups, with older age groups and men generally having higher average hourly wages.
- In 2025, **Brantford had the highest unemployment rate among the top five CMAs analysed, at 14.10%**.
- The dashboard allows users to move from a national overview to detailed provincial and CMA-level analysis.

---

## Dashboard Pages

### 1. Summary

The Summary page provides an overview of the Canadian labour market using the most recent year available in the dataset, 2025.

It includes:

- National unemployment rate
- Unemployment trend from 2021–2025
- Total employment
- Average hourly wage
- Wage change since 2021
- Industries with high unemployment
- Provinces with the largest unemployment changes
- Navigation to detailed report pages

### 2. Provinces

The Provinces page focuses on employment and labour-force characteristics across Canada.

Users can:

- Select a year
- Compare total employment and labour force
- Analyse employment by industry
- Select provinces using an interactive map
- Drill through to detailed provincial analysis

### 3. Province Details

The Province Details page provides a deeper analysis of a selected province.

It includes:

- Annual unemployment trends
- Population change
- Employment change
- Unemployment by age and gender
- Industry filtering
- Unemployment changes by demographic group

### 4. Wages

The Wages page analyses average hourly wages at the provincial level.

It includes:

- Average hourly wage
- Wage trends over time
- Wage comparisons by age group
- Male and female wage comparisons
- Top five earning industries
- Highest and lowest earning demographic groups

### 5. Census Metropolitan Areas

The CMA page provides a more detailed geographic analysis.

CMA stands for **Census Metropolitan Area**, a geographic area centred around a population centre and including surrounding municipalities that are closely integrated with it.

The page includes:

- CMA population
- CMA unemployment rates
- Geographic visualization
- Top CMAs by unemployment rate
- Annual unemployment trends
- Age and gender analysis
- City-level unemployment information

---

## Data Sources

The data used in this project was obtained from **Statistics Canada** and covers the period from 2021 to 2025.

Statistics Canada:
https://www.statcan.gc.ca/

The original datasets should be consulted for the complete definitions, methodology, and data limitations.

The project uses information related to:

- Labour force and employment
- Unemployment
- Average hourly wages
- Industries
- Age and gender
- Provinces
- Census Metropolitan Areas

---

## Industry Classification

Industry information is based on the **North American Industry Classification System (NAICS)**.

NAICS is a standardized classification system used to organize businesses and economic activities into industries.

Statistics Canada — NAICS:
https://www.statcan.gc.ca/en/subjects-start/business-industry-and-trade/business-industry-and-trade

---

## Data Preparation

The data was prepared using **Power Query** in Power BI.

Data-cleaning steps included:

- Trimming values
- Standardizing fields
- Removing unwanted footnotes
- Replacing incorrect or inconsistent values
- Preparing tables for relationships
- Creating geographic information
- Preparing data for analysis

Power Query transformation steps were used to ensure that values matched correctly between fact and dimension tables.

---

## Data Model

The project uses a **star-schema approach** with two primary fact tables:

- `Fact Province`
- `Fact CMA`

The provincial fact table contains labour-market information such as employment, unemployment, labour force, unemployment rate, wages, age, gender, and industry.

The CMA fact table contains information such as employment rate, unemployment rate, population, age, gender, and geographic information.

Dimension tables provide additional information about provinces, cities, and other analytical categories.

The City dimension also contains province information, allowing geographic analysis between provinces and their associated cities or CMAs.

---

## Calculated Columns and Measures

The project uses both **calculated columns and DAX measures**.

A calculated unemployment-rate percentage column was created in the provincial fact table.

DAX measures were used extensively for dynamic calculations, including:

- Employment changes
- Unemployment changes
- Wage changes
- Highest and lowest values
- Demographic comparisons
- Province comparisons
- CMA comparisons

Measures were preferred for many calculations because they respond dynamically to slicers, filters, and drill-through selections.

---

## Power BI Features Used

The dashboard demonstrates several Power BI features, including:

- Power Query
- Star-schema data modelling
- Relationships
- DAX measures
- Calculated columns
- Slicers
- Drill-through pages
- Interactive maps
- Tooltips
- Decomposition tree
- Cards
- Matrix visualizations
- Charts
- Conditional formatting
- Interactive filtering

---

## Tools

- **Microsoft Power BI**
- **Power Query**
- **DAX**
- **Statistics Canada open data**
- **OpenAI / AI-assisted data preparation**

---

## Project Purpose

This project was created as a data analytics project to demonstrate the process of transforming publicly available data into an interactive business-intelligence dashboard.

The focus was not only on presenting individual statistics, but also on allowing users to interact with the data and investigate how labour-market characteristics vary across **time, geography, industry, age, and gender**.

---

## Dashboard Preview

### Summary
![Summary Dashboard](Screenshots/Summary.png)

### Provincial Analysis
![Provincial Analysis](Screenshots/Provinces1.png)
![Provincial Analysis](Screenshots/Provinces3.png)

### Wage Analysis
![Wage Analysis](Screenshots/AgeGender.png)

### CMA Analysis
![CMA Analysis](Screenshots/CMA1.png)
![CMA Analysis](Screenshots/CMA2.png)

## Disclaimer

This project is an independent data-analysis project using publicly available Statistics Canada data.

The visualizations and analysis represent the author's interpretation of the available data and are not intended to replace Statistics Canada's official publications or methodology.
