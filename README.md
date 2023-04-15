# Project Documentation of KPMG AU Data Analytics Virtual Internship BY Arowosola Oluwaseun

## Outline
- Introduction 
- The workflow
- Findings 
- Data Gathering and Transformation
- RFM segmentation /Analysis 
- Data Modelling in Power BI
- Data analysis
- Recommendation
- Conclusion

### Introduction
This is a real-world Project Hand-on by 2018 KPMG, an Australian partnership and a member firm of the KPMG network of independent member firms affiliated with KPMG International Cooperative (“KPMG International”), a Swiss entity.

It belongs to Sprocket Central Pty Ltd, a medium size bikes & cycling accessories organization, whose need help with its customer and transaction data. 
itis a long-standing KPMG client whom specializes in high-quality bikes and accessible cycling accessories to riders. Their marketing team is looking to boost business by analysing their existing customer trends and behaviour. It has a large dataset relating to customer, it their team is unsure how to effectively analyse it to help optimize its marketing strategy.

### The workflow
The Project contains of 3 Tasks which entails:
1	**Data quality assessment:** Assessment of data quality and completeness in preparation for analysis.
The task is to take a look at datasets provided by Sprocket Central Pty Ltd and identify all data quality issues. And draft an email to the client identifying all data quality issues.

2	**Data Insights:** Targeting high value customers based on customer demographics and attributes.
This task is to create a PowerPoint presentation which outlines the approach that will be taking to identify which of the 1000 customers Sprocket Central Pty Ltd should target, based on this dataset. That explain the three phases:  Data Exploration; Model Development and Interpretation.

3	 **Data Insights and Presentation:** Using Visualisations to present insights.
The task is to develop a dashboard that can be present to the client at the next meeting. Displaying the data summary and results of the analysis in a dashboard. Specifically, the presentation specifies who Sprocket Central Pty Ltd' should be targeting out of the new 1000 customer list.	

### Finding’s Presentation 
- What are the trends in the underlying data?
- Which customer segment has the Sprocket central Pty Ltd’s marketing and growth strategy?
- What additional external datasets maybe useful to obtain greater insights into customer preferences and propensity to purchase the products?
- Specifically, your presentation should specify who Sprocket central Pty Ltd’s marketing teams should be targeting out of the new 1000customer list as well as the broader market segment to reach out to.

### Data Gathering and Transformation
The Organisation provided 3 datasets **(Customer demographic, Customer address and Transactions in the past month)**

**The Customer demographic data** has 92000 records: 13Columns and 4000Rows.  The data includes Customer ID, First Name, Last Name, Gender, Past 3years bike related purchase, DOB, Job title, Job Industry Category, Wealth segment, Deceased indicator, Default, Own car, Tenure which will allow me to properly visualize and dimension the data.

**The Customer address Data** has 27993 data records: 6Columns and 3999 Rows. The data includes customer ID, Address, postcode, State, Country and Property Valuation.

**The Transactions in the past month Data** has 26000 data records: 13Columns and 2000 Rows. The data includes Transaction ID, Product ID, Customer ID, Transaction Date, Online Order, Order Status, Brand, Product line, Product class, Product Size, List Price, Standard Cost and Product first sold date. It is a table that has a primary key (Customer ID) that I used to connect to the Order Data. [](url)

The raw data fields were cleaned and transformed into other calculated fields for modelling purposes (i.e converting D.O.B to age or age groups), been pre-processed with Excel, I had to remove blank data, create some additional columns, and connect the Transaction table with Customer Demographic tables.
After the cleaning and transformation, an email was drafted to identify the data quality issues and strategies to mitigate these issues. Then, how it may impact our analysis forward in phase 2.  Data Quality Email.docx
Summary of Transformation Carried as can be seen in Data Quality Email.docx

