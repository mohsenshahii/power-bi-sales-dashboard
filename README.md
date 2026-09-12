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

<img width="1346" height="757" alt="Image" src="https://github.com/user-attachments/assets/c216bf29-3aaa-4a7c-8ab1-4f11fb7685bf" />


### Sales Persons Detailes

<img width="1345" height="760" alt="Image" src="https://github.com/user-attachments/assets/984133a9-c695-4b32-9cc0-41505518bdda" />


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

> Sales performance in the United States and East Asia is particularly strong, making these regions some of the best-performing markets.
> Although the conversion rate from the Proposal stage to the next stage is relatively low at 27%, the overall win rate is considerably high at 80%, indicating that opportunities reaching the final stage have a strong likelihood of being won.
> Among the top five salespersons, Angela Chen has handled considerably fewer opportunities than her peers. However, in terms of total opportunity value, she has outperformed them, highlighting her strong performance in managing high-value opportunities.

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

<html xmlns:o="urn:schemas-microsoft-com:office:office"
xmlns:x="urn:schemas-microsoft-com:office:excel"
xmlns="http://www.w3.org/TR/REC-html40">

<head>

<meta name=ProgId content=Excel.Sheet>
<meta name=Generator content="Microsoft Excel 15">
<link id=Main-File rel=Main-File
href="file:///C:/Users/Utente/AppData/Local/Temp/msohtmlclip1/01/clip.htm">
<link rel=File-List
href="file:///C:/Users/Utente/AppData/Local/Temp/msohtmlclip1/01/clip_filelist.xml">
<style>
<!--table
	{mso-displayed-decimal-separator:"\.";
	mso-displayed-thousand-separator:"\,";}
@page
	{margin:.75in .7in .75in .7in;
	mso-header-margin:.3in;
	mso-footer-margin:.3in;}
tr
	{mso-height-source:auto;}
col
	{mso-width-source:auto;}
br
	{mso-data-placement:same-cell;}
td
	{padding-top:1px;
	padding-right:1px;
	padding-left:1px;
	mso-ignore:padding;
	color:black;
	font-size:11.0pt;
	font-weight:400;
	font-style:normal;
	text-decoration:none;
	font-family:"Aptos Narrow", sans-serif;
	mso-font-charset:0;
	mso-number-format:General;
	text-align:general;
	vertical-align:bottom;
	border:none;
	mso-background-source:auto;
	mso-pattern:auto;
	mso-protection:locked visible;
	white-space:nowrap;
	mso-rotate:0;}
.xl66
	{mso-number-format:"Short Date";}
-->
</style>
</head>

<body link="#467886" vlink="#96607D">

Opportunity Sales fact table:

Opportunity   ID | Reporting Date | Salesperson | Customer | Country | Sales stage | Opportunity Value (USD) | Sales Channel | Close Date/Expected Close Date | Next Steps
-- | -- | -- | -- | -- | -- | -- | -- | -- | --
N00000001 | 1/1/2015 | Angela Chen | Customer 1 | China | Identified | 2910 | Telesales | 4/7/2015 | No   Response
N00000002 | 1/1/2015 | Denny Walker | Customer 2 | Australia | Validated | 1680 | Telesales | 4/2/2015 | Follow up on call
N00000003 | 1/1/2015 | Angela Chen | Customer 3 | France | Validated | 1840 | Partners | 6/6/2015 | Follow   up on call
N00000004 | 1/1/2015 | Charlie Brooks | Customer 4 | US | Proposal | 1380 | Telesales | 5/4/2015 | Follow up on call
N00000005 | 1/1/2015 | Greg Mitchell | Customer 5 | US | Proposal | 4350 | Telesales | 4/17/2015 | Send   Email
N00000006 | 1/1/2015 | Bob Harrison | Customer 6 | India | Qualified | 2740 | Telesales | 4/6/2015 | Follow up on call
N00000007 | 1/1/2015 | Angela Chen | Customer 7 | US | Validated | 3040 | Telesales | 6/17/2015 | Schedule   a Meeting
N00000008 | 1/1/2015 | Tim Parker | Customer 8 | Malaysia | Identified | 1510 | Telesales | 6/26/2015 | Schedule a Meeting
N00000009 | 1/1/2015 | Edwin Foster | Customer 9 | Canada | Identified | 1960 | Partners | 4/21/2015 | Follow   up on call
N00000010 | 1/1/2015 | Lynda Morales | Customer 10 | France | Won | 3990 | F2F | 3/27/2015 |  
N00000011 | 1/1/2015 | Paul Bennett | Customer 11 | France | Identified | 300 | Partners | 6/21/2015 | Follow   up on call
N00000012 | 1/2/2015 | Angela Chen | Customer 12 | Malaysia | Proposal | 3030 | Telesales | 6/22/2015 | Send Email
N00000013 | 1/2/2015 | Edwin Foster | Customer 13 | UK | Proposal | 380 | Website | 4/9/2015 | Follow   up on call
N00000014 | 1/2/2015 | Rachael Simmons | Customer 14 | Germany | Validated | 4430 | Telesales | 5/10/2015 | No Response
N00000015 | 1/2/2015 | Paul Bennett | Customer 15 | China | Validated | 3390 | F2F | 4/21/2015 | Schedule   a Meeting
N00000016 | 1/2/2015 | Martha Reynolds | Customer 16 | Indonesia | Validated | 4680 | F2F | 6/26/2015 | Follow up on call
N00000017 | 1/2/2015 | Joe Thompson | Customer 17 | Canada | Identified | 2510 | F2F | 5/10/2015 | Schedule   a Meeting
N00000018 | 1/2/2015 | Paul Bennett | Customer 18 | Germany | Identified | 4900 | F2F | 5/21/2015 | Schedule a Meeting
N00000019 | 1/2/2015 | John Carter | Customer 19 | Australia | Identified | 4270 | F2F | 5/15/2015 | Follow   up on call
N00000020 | 1/2/2015 | Paul Bennett | Customer 20 | Australia | Identified | 2920 | F2F | 4/25/2015 | Send Email
N00000021 | 1/2/2015 | Arnold Hayes | Customer 21 | Australia | Validated | 1570 | F2F | 5/12/2015 | Schedule   a Meeting
N00000022 | 1/2/2015 | Piere Laurent | Customer 22 | India | Identified | 980 | F2F | 5/13/2015 | No Response
N00000023 | 1/2/2015 | Charlie Brooks | Customer 23 | China | Lost | 2230 | F2F | 5/14/2015 |  
N00000024 | 1/3/2015 | Mike Daniels | Customer 24 | Malaysia | Validated | 1390 | Partners | 4/2/2015 | Schedule a Meeting
N00000025 | 1/3/2015 | Angela Chen | Customer 25 | UK | Won | 3960 | Telesales | 2/4/2015 |  
N00000026 | 1/3/2015 | Denny Walker | Customer 26 | Malaysia | Identified | 4800 | F2F | 4/21/2015 | No Response
N00000027 | 1/3/2015 | Charlie Brooks | Customer 27 | UK | Won | 1990 | F2F | 2/4/2015 |  
N00000028 | 1/3/2015 | Lynda Morales | Customer 28 | China | Validated | 210 | Website | 4/4/2015 | No Response
N00000029 | 1/3/2015 | Bob Harrison | Customer 29 | India | Identified | 1200 | Partners | 4/21/2015 | No   Response
N00000030 | 1/3/2015 | Greg Mitchell | Customer 30 | Indonesia | Proposal | 2760 | F2F | 4/2/2015 |  
N00000031 | 1/3/2015 | Tim Parker | Customer 31 | India | Identified | 4210 | F2F | 6/4/2015 | Send   Email
N00000032 | 1/3/2015 | Cameron Blake | Customer 32 | US | Identified | 2690 | F2F | 6/29/2015 | Send Email
N00000033 | 1/3/2015 | John Carter | Customer 33 | UK | Qualified | 290 | Website | 5/31/2015 | Send   Email
N00000034 | 1/3/2015 | Bob Harrison | Customer 34 | France | Validated | 4690 | F2F | 5/5/2015 | Follow up on call
N00000035 | 1/3/2015 | Adrian Scott | Customer 35 | Canada | Identified | 980 | Telesales | 5/19/2015 | Follow   up on call
N00000036 | 1/4/2015 | Edwin Foster | Customer 36 | Canada | Identified | 1670 | F2F | 6/7/2015 |  
N00000037 | 1/4/2015 | Angela Chen | Customer 37 | Malaysia | Identified | 1030 | F2F | 6/8/2015 | Follow   up on call
N00000038 | 1/4/2015 | Rose Delgado | Customer 38 | Indonesia | Validated | 3180 | Partners | 6/2/2015 | Schedule a Meeting
N00000039 | 1/4/2015 | Chang Liu | Customer 39 | Australia | Proposal | 2360 | Partners | 6/28/2015 | Follow   up on call
N00000040 | 1/4/2015 | Martha Reynolds | Customer 40 | Germany | Proposal | 550 | Telesales | 4/5/2015 | Follow up on call
N00000041 | 1/4/2015 | Greg Mitchell | Customer 41 | India | Validated | 2900 | F2F | 4/11/2015 | Send   Email
N00000042 | 1/4/2015 | Lynda Morales | Customer 42 | Indonesia | Qualified | 3700 | F2F | 4/22/2015 | Schedule a Meeting
N00000043 | 1/4/2015 | Piere Laurent | Customer 43 | US | Validated | 1890 | F2F | 4/3/2015 | Follow   up on call
N00000044 | 1/4/2015 | Rose Delgado | Customer 44 | Australia | Identified | 880 | Telesales | 6/24/2015 | Follow up on call
N00000045 | 1/4/2015 | Arnold Hayes | Customer 45 | China | Identified | 3820 | F2F | 4/6/2015 | Follow   up on call
N00000046 | 1/4/2015 | Chang Liu | Customer 46 | India | Identified | 780 | Telesales | 4/8/2015 | No Response
N00000047 | 1/4/2015 | Greg Mitchell | Customer 47 | US | Identified | 4400 | F2F | 5/17/2015 | Follow   up on call
N00000048 | 1/4/2015 | Paul Bennett | Customer 48 | UK | Validated | 2040 | F2F | 6/28/2015 | Schedule a Meeting
N00000049 | 1/5/2015 | Chang Liu | Customer 49 | Australia | Proposal | 2130 | F2F | 4/11/2015 | Follow   up on call
N00000050 | 1/5/2015 | Rachael Simmons | Customer 50 | Malaysia | Identified | 4910 | F2F | 5/18/2015 |  
N00000051 | 1/5/2015 | Adrian Scott | Customer 51 | Germany | Qualified | 3720 | F2F | 5/20/2015 |  
N00000052 | 1/5/2015 | Paul Bennett | Customer 52 | Germany | Validated | 2140 | F2F | 6/15/2015 | Schedule a Meeting
N00000053 | 1/5/2015 | Denny Walker | Customer 53 | Canada | Identified | 3420 | F2F | 5/27/2015 | Schedule   a Meeting
N00000054 | 1/5/2015 | Arnold Hayes | Customer 54 | Germany | Identified | 620 | Telesales | 5/8/2015 | Follow up on call
N00000055 | 1/5/2015 | Greg Mitchell | Customer 55 | France | Qualified | 3980 | Partners | 5/15/2015 | No   Response
N00000056 | 1/5/2015 | Bob Harrison | Customer 56 | Canada | Proposal | 1940 | F2F | 6/17/2015 | Follow up on call
... | ... | ... | ... | ... | ... | ... | ... | ... | ... 




Sales Persons Dimension table:

Salesperson | Images
-- | --
Angela Chen | https://i.ibb.co/zTb1n1X7/Angela.png
Denny Walker | https://i.ibb.co/GQVNznMt/Denny.png
Charlie Brooks | https://i.ibb.co/6JBg4QjR/Charlie.png
Greg Mitchell | https://i.ibb.co/mr1JTYk4/Greg.png
Bob Harrison | https://i.ibb.co/YFgVQjL1/Bob.png
Tim Parker | https://i.ibb.co/Qjq9Stj4/Tim.png
Edwin Foster | https://i.ibb.co/QqH2fZ3/Edwin.png
Lynda Morales | https://i.ibb.co/nqbYK54f/Lynda.png
Paul Bennett | https://i.ibb.co/fdNB06Pd/Paul.png
Rachael Simmons | https://i.ibb.co/LdX65drH/Rachael.png
Martha Reynolds | https://i.ibb.co/S7BtQnDh/Martha.png
Joe Thompson | https://i.ibb.co/wZCc0FnP/Joe.png
John Carter | https://i.ibb.co/qY1631D9/John.png
Arnold Hayes | https://i.ibb.co/5WssxkWw/Arnold.png
Piere Laurent | https://i.ibb.co/d3ZSzN4/Piere.png
Mike Daniels | https://i.ibb.co/8DDS1Pk3/Mike.png
Cameron Blake | https://i.ibb.co/BH7rf8xM/Cameron.png
Adrian Scott | https://i.ibb.co/Vc4qJ0R7/Adrian.png
Rose Delgado | https://i.ibb.co/cc2brFrw/Rose.png
Chang Liu | https://i.ibb.co/nNxr4VD6/Chang.png


</body>

</html>
