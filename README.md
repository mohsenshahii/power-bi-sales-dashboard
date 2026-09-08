# 📊 Sales Opportunities Dashboard — Power BI

## Overview

**Sales Opportunities** is an interactive Business Intelligence dashboard developed with **Microsoft Power BI** to analyze and monitor sales opportunities throughout the sales process.

The project transforms sales opportunity data into interactive visualizations and KPIs that help users understand sales performance, opportunity distribution, pipeline development, and business trends.

The project is built using the **Power BI Project (`.pbip`)** format, making it suitable for version control and portfolio development.

---

## 🎯 Project Objectives

The main objectives of this project are to:

* Analyze sales opportunities and their distribution
* Monitor the sales pipeline
* Identify Salespersons and their Lost opportunities or Won ones in opportunity data
* Compare performance across relevant business dimensions
* Provide an interactive interface for exploring sales data
* Support data-driven sales and business decisions

---

## 📌 Key Business Questions

The dashboard is designed to help answer questions such as:

* How many sales opportunities are currently in the pipeline?
* What is the total opportunities value?
* How are opportunities distributed across different stages?
* How are opportunities distributed across different countries?
* Which categories, regions, products, or sales representatives generate the most opportunities?
* How does opportunity performance change over time?
* Which opportunities or segments require the most attention?

---

## 🛠️ Tools & Technologies

| Technology        | Purpose                                          |
| ----------------- | ------------------------------------------------ |
| **Power BI**      | Dashboard development and data visualization     |
| **Power Query**   | Data cleaning and transformation                 |
| **DAX**           | Measures and analytical calculations             |
| **Data Modeling** | Creating relationships and analytical structures |
| **Git / GitHub**  | Version control and project documentation        |

---

## 📊 Dashboard

### Sales Opportunities Overview

[page1.bmp](https://github.com/user-attachments/files/31966192/page1.bmp)


### Sales Persons Detailes

[page2.bmp](https://github.com/user-attachments/files/31966903/page2.bmp)


---

## 🔍 Analysis

The dashboard provides an interactive view of the sales opportunity pipeline.

Users can explore the data through filters and visualizations to investigate differences across dimensions such as:

* Opportunity stage
* Sales persons
* Countries
* Product/category
* Customer
* Time period
* Opportunity status

The interactive design allows users to move from high-level KPIs to more detailed views of individual segments.

---

## 🧮 Data & DAX

The project uses **DAX measures** to calculate business metrics and support interactive analysis.

Some examples of measures that can be documented here include:

```DAX
Opportunities Won = CALCULATE([Total Oportunities],'Sales Opportunities'[Deal Status] = "Won")
```

```DAX
Win Rate = 
DIVIDE(
[Opportunities Won],
CALCULATE([Total Oportunities], 'Sales Opportunities'[Deal Status] IN {"Won","Lost"})
)
```

```DAX
Conversion Rate = 
VAR ProposalCount = CALCULATE([Total Oportunities],'Sales Opportunities'[Sales stage] = "Proposal")
VAR WonCount = [Opportunities Won]
RETURN
DIVIDE(WonCount,ProposalCount+WonCount)
```

---

## 🗂️ Project Structure

```text
SalesOpportunities/
│
├── SalesOpportunities.pbip
│
├── SalesOpportunities.Report/
│   └── ...
│
├── Screenshots/
│   ├── dashboard-overview.png
│   ├── sales-analysis.png
│   └── opportunity-analysis.png
│
├── Documentation/
│   ├── data-dictionary.md
│   └── dax-measures.md
│
└── README.md
```

---

## 📈 Key Insights

The dashboard can be used to identify important patterns in the sales pipeline, including:

* High-value sales opportunities
* Distribution of opportunities across pipeline stages
* Strong and weak-performing salespersons
* Changes in opportunity volume over time
* Countries where sales teams may need additional attention

> Add **3–5 specific findings from your actual dashboard** here. This section is especially important for demonstrating that you can interpret data, not just build visualizations.

---

## 💡 Skills Demonstrated

This project demonstrates practical experience with:

* Business Intelligence
* Data Analysis
* Data Visualization
* Power BI
* Power Query
* DAX
* Data Modeling
* KPI Development
* Interactive Dashboard Design
* Business-oriented Data Storytelling
* GitHub / Version Control

---

## 🚀 How to Use

1. Clone this repository:

```bash
git clone https://github.com/mohsenshahii/SalesOpportunities.git
```

2. Open the project folder.

3. Open:

```text
SalesOpportunities.pbip
```

with **Power BI Desktop**.

4. Explore the dashboard using the available filters and interactive visualizations.

---

## 📁 Data

The project uses sales opportunity data for analytical and visualization purposes.



**Power BI • Data Analytics • Business Intelligence • DAX • Data Visualization**
