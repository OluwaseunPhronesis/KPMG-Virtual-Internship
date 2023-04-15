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
1. **Data quality assessment:** Assessment of data quality and completeness in preparation for analysis.
The task is to take a look at datasets provided by Sprocket Central Pty Ltd and identify all data quality issues. And draft an email to the client identifying all data quality issues.

2. **Data Insights:** Targeting high value customers based on customer demographics and attributes.
This task is to create a PowerPoint presentation which outlines the approach that will be taking to identify which of the 1000 customers Sprocket Central Pty Ltd should target, based on this dataset. That explain the three phases:  Data Exploration; Model Development and Interpretation.

3. **Data Insights and Presentation:** Using Visualisations to present insights.
The task is to develop a dashboard that can be present to the client at the next meeting. Displaying the data summary and results of the analysis in a dashboard. Specifically, the presentation specifies who Sprocket Central Pty Ltd' should be targeting out of the new 1000 customer list.	

### Finding’s Presentation 
- What are the trends in the underlying data?
- Which customer segment has the Sprocket central Pty Ltd’s marketing and growth strategy?
- What additional external datasets maybe useful to obtain greater insights into customer preferences and propensity to purchase the products?
- Specifically, your presentation should specify who Sprocket central Pty Ltd’s marketing teams should be targeting out of the new 1000customer list as well as the broader market segment to reach out to.

### Data Gathering and Transformation
The Organisation provided 3 datasets **(Customer demographic, Customer address and Transactions in the past month)**

- **The Customer demographic data** has 92000 records: 13Columns and 4000Rows.  The data includes Customer ID, First Name, Last Name, Gender, Past 3years bike related purchase, DOB, Job title, Job Industry Category, Wealth segment, Deceased indicator, Default, Own car, Tenure which will allow me to properly visualize and dimension the data.

- **The Customer address Data** has 27993 data records: 6Columns and 3999 Rows. The data includes customer ID, Address, postcode, State, Country and Property Valuation.

- **The Transactions in the past month Data** has 26000 data records: 13Columns and 2000 Rows. The data includes Transaction ID, Product ID, Customer ID, Transaction Date, Online Order, Order Status, Brand, Product line, Product class, Product Size, List Price, Standard Cost and Product first sold date. It is a table that has a primary key (Customer ID) that I used to connect to the Order Data. [https://github.com/OluwaseunPhronesis/KPMG-Virtual-Internship/blob/main/KPMG_VI_New_raw_data_update_final%20-%20Copy.xlsx](url)

The raw data fields were cleaned and transformed into other calculated fields for modelling purposes (i.e converting D.O.B to age or age groups), been pre-processed with Excel, I had to remove blank data, create some additional columns, and connect the Transaction table with Customer Demographic tables.
After the cleaning and transformation, an email was drafted to identify the data quality issues and strategies to mitigate these issues. Then, how it may impact our analysis forward in phase 2.

Summary of Transformation Carried as can be seen in the email [https://github.com/OluwaseunPhronesis/KPMG-Virtual-Internship/blob/main/Data%20Quality%20Email.docx](url)

### Data Modelling in Excel
After data was transformed into the Pivot table, new measures such as RFM Segmentation were created in other to build a relationship with data set that was available. After creating a relationship, proceed into creating a PowerPoint presentation which outlines the approach that identify which of the 1000 customers Sprocket Central Pty Ltd should target, based on the dataset. 

### RFM Segmentation/Analysis
**RFM Analysis** is a marketing technique used to quantitatively rank and group customers based on the recency, frequency and monetary total of their recent transactions to identity the best customers and perform targeted marketing campaigns. To predict how a new customer is likely to act in the future.

RFM stand for Recency, Frequency and Monetary.
- **Recency** is simply the amount of time since the customer’s most recent transaction (most businesses use days, though for others it might make sense to use months, weeks or even hours. How recently did the customer purchase? On a Scale of 4 - 1
- **Frequency** is the total number of transactions made by the customer (during a defined period). How often do the customer purchase? On a Scale of 4 - 1
- **Monetary** is the total amount that the customer has spent across all transactions (during a defined period). How much do they spend in total? On a Scale of 4 - 1

**RFM Analysis**

This was done by using Recency, Product ID and Sum of Profit column from the dataset received in PivotTable Field to create R_Score, F_Score and M_Score to formed RFM Value.

444, 434, 424, 414, 441, 442, 443

344, 334, 324, 314, 341, 342, 343

244, 234, 224, 214, 243, 242, 241

144, 134, 124, 114, 141, 142, 143

A Bar chart was plotted to represent the RFM Segmentation. The Segmentation represent the performance of the customer: -

•	Platinum customer = 444 (most recent transaction, high transacted and most spent) Your best customers, they buy and spend a lot and made their last purchase recently

•	Very Loyal >444, >=433 Very good customers – they spend a lot. X5X

[] 	The above customer segment: they love you and they represent your ideal customer

•	Becoming Loyal >433, >=421 Recent customers, who made only a few purchases. 52X

•	Recent customer >421, >=344 customers who buy frequently and spent a lot, but made their last purchase some time ago. X53 and X52

•	Potential Customer >344, >=323 Recent customers, but who have already spent a lot. Added (registered) in less than 3 months but they spent more than ATM (Average Monetary Value)

•	Late bloomer >323, > = 311 customers with recency and above-average spending. Customers whose new level < last level

•	Losing Customer >311, >= 224 Customer who have spent a lot, but have been inactive for long time 22X

•	High Risk Customer >224, >= 212 customer who bought frequently, but haven’t made any purchases in a long time. Customer whose new level< last level (3 times)

•	Almost Lost Customer >121, >= 124 Customer who have spent a lot, but have been inactive for long time 22X

[] 	The above customer segment: They have sympathy from you and they represent your average customer

•	Evasive Customer >124, >= 112 Low frequency, low spender customers who haven’t bought in a longtime. (6months)

•	Lost customer = 111 Your worst customers. They haven’t bought in a long time, they only bought once (or very few times) and they spent very little

[] 	The Customer segment: They are indifferent to you and they represent problematic customer.

**Tip** The QUARTILE.INC return the quartile of a given data set based on percentile value from 0.1, inclusive	
=IFS(H5=444,"Platinum Customer",AND(H5>444,H5>=433),"Very Loyal",AND(H5>433,H5>=421),"Becoming Loyal",AND(H5>421,H5>=344),"Recent Customer",AND(H5>344,H5>=323),"Potential Customer",AND(H5>323,H5>=311),"Late Bloomer",AND(H5>311,H5>=224),"Losing Customer",AND(H5>224,H5>=212),"High Risk Customer",AND(H5>212,H5>=124),"Almost Lost Customer",AND(H5>124,H5>=112),"Evasive Customer",H5=111,"Lost Customer") 

### Data Analysis 
Building the recommended, I started with a PowerPoint presentation which outlines the approach that we will be taking with the following 3 phrases as – Data Exploration: Model Development and Interpretation.	[https://github.com/OluwaseunPhronesis/KPMG-Virtual-Internship/blob/main/PowerPoint%20Presentation.pptx](url)

#### The result of the analysis

![Screenshot of a comment on a GitHub issue showing an image, added in the Markdown, of an Octocat smiling and raising a tentacle.](https://github.com/OluwaseunPhronesis/KPMG-Virtual-Internship/blob/main/Dashboard.png)

[https://github.com/OluwaseunPhronesis/KPMG-Virtual-Internship/blob/main/Dynamic%20Dashboard.pbix](url)

- A visualization showing the number of customers that purchased based on their wealth segmentation was “Mass customer” with 50.89%, followed by “High net worth” with 27.01% and “Affluent Customer” with 22.1% of customers. 

- Also, a visual on visualization showing the past 3 years Purchase shows that Solex brand have the highest percentage of 21% while Trek Bicycle brand was the least percentage with 13%. 

![Screenshot of a comment on a GitHub issue showing an image, added in the Markdown, of an Octocat smiling and raising a tentacle.](https://github.com/OluwaseunPhronesis/KPMG-Virtual-Internship/blob/main/Wealth%20segment.png)

- Order status: From 36,940 Transactions, 99.28% order was Approved while 0.72% order was Cancelled.

- Recent customer segment has the highest Sprocket central Pty Ltd’s marketing and growth strategy for all the brands.

![Screenshot of a comment on a GitHub issue showing an image, added in the Markdown, of an Octocat smiling and raising a tentacle.](https://github.com/OluwaseunPhronesis/KPMG-Virtual-Internship/blob/main/RFm%20analysis.png)


### Recommendation
Based on the result from the customer segmentation analysis, Sprocket central Pty Ltd’s are encouraged to have more Solex Brand in stock as it is of high demand, they should see it as a brand that are bringing more profit to the business as it was showed in the visulisation for past 3 years purchase while Trek Bicycle Brand Marketing Team should do more advert on their brand for it to be well known to people.
For continuing growth of the business, Sprocket central Pty Ltd’s should always target Recent customer for marketing and strategy growth.

### Conclusion 
This Internship shows the impact of RFM analysis in businesses to determine customer segment based on their review thereby letting the business owner know how their business grow and perceived by the customer’s patronage. Using the right tool to analyze segment is also as important as getting the intended result and you can’t miss it when you combine Excel with Power BI to accomplish it.

