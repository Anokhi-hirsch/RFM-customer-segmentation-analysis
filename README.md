# Customer Segmentation Analysis Using RFM  
## Objective  
The purpose of this project is to conduct a Customer Segmentation Analysis for an Automobile bike Company. Customer segmentation is performed by developing an RFM Model. RFM analysis is a behavior-based approach to segment customers based on their purchasing behavior using Recency, Frequency, and Monetary (RFM) analysis. This segmentation will help identify different customer groups and provide actionable insights for targeted marketing strategies.
Customer segmentation can help businesses in many ways, including targeted marketing, customer retention, efficiency and improved customer satisfaction. By organizing customers into distinct groups based upon shared characteristics, we can gauge and respond to their needs in strategic ways that help them get the most out of the product and best meet their needs.
## Tools and Libraries Used
Programming Languages: Python  
Libraries: pandas, numpy, matplotlib, seaborn, etc.  
Visualization Tools: Tableau
## Data Overview
The raw data is collected from Kaggle, which can be found <code>[here.](https://www.kaggle.com/datasets/tforsyth/99bikes-sales-data/data)</code>  
This dataset contains sales and customer data of one of Australia's largest retailers of bicycles named 99 Bikes. They sell everything bicycle-related, from accessories to clothing to helmets to even e-bikes.  
The datasets used include:  
<code>[Raw_data_99bikes.xlsx:](https://github.com/Anokhi-hirsch/RFM-customer-segmentation-analysis/blob/main/raw_data_99bikes.xlsx)</code> This Excel file dataset included the following sheets of data:  
- Transactions_data.xlsx: Transactions data of the customers across all the different states in Australia.  
- NewCustomerList.xlsx: The list of the new customers who visited the automobile bike company recently.  
- CustomerDemographic.xlsx: Includes the entire details of the Customer Demographics.  
- CustomerAddress.xlsx: Address of the Customers.  
## Analysis Approach  
### 1. Data Cleaning and Preprocessing  
Key Data Quality Issues Addressed:  
- CustomerDemographics.xlsx:  
Dropped unnecessary columns, addressed missing data in five columns by either dropping records or imputing appropriate values, standardized inconsistent data in the gender column, created 'Age' and 'Age Group' columns from the Date of Birth, an outlier was identified and removed.

- NewCustomerList.xlsx:  
Removed five unnecessary columns, managed missing data across four columns using deletion or imputation as appropriate, created 'Age' and 'Age Group' columns from the Date of Birth.

- Transaction_data.xlsx:  
Converted the 'product_first_sold_date' column from int64 to datetime format, managed missing data in seven columns using deletion or imputation as necessary, added a 'Profit' column, calculated as the difference between list price and standard price.

- CustomerAddress.xlsx:  
Standardized inconsistent data in the states column, identified and addressed customer IDs from the Customer Demographics table that were missing in the Address table.

For a more detailed analysis and the complete code, please visit the Jupyter Notebook[ data cleaning & assessment](https://github.com/Anokhi-hirsch/RFM-customer-segmentation-analysis/blob/main/data_cleaning_%26_assessment.ipynb).

### 2. Exploratory Data Analysis (EDA)

The following insights were derived from the exploratory analysis of customer segments after data cleaning:

- **Age Distribution (New vs. Old Customers)**: The majority of both New and Old customers fall within the 40-49 age group. The fewest customers are under 20 and over 80 years old. Notably, there’s a sharp decline in New customers in the 30-39 age group.
  ![Age Distribution](https://github.com/Anokhi-hirsch/sales-data-analysis/blob/main/dashboard-images//initial-sales-analysis.jpg)

- **Bike Purchases by Gender (Last 3 Years)**: Female customers dominate bike purchases, making up 51% of total purchases, surpassing males by 10,000 bikes.
  ![Bike Purchases by Gender](images/bike_purchases_by_gender.png)

- **Job Industry Distribution (New vs. Old Customers)**: Most New customers work in Manufacturing and Financial Services (~20%), while the least are in Agriculture and Telecom (~3%). Old customers follow a similar pattern.
  ![Job Industry Distribution](path/to/job_industry_distribution.png)

- **Wealth Segmentation by Age**: Across all age groups, the 'Mass Customer' segment has the highest representation, followed by 'High Net Worth' customers. However, in the 40-49 age group, the Affluent segment exceeds High Net Worth customers.
  ![Wealth Segmentation by Age](path/to/wealth_segmentation_by_age.png)

- **Cars Owned by State**: New South Wales has the most customers without cars, while Queensland has more car owners than non-owners. Victoria shows an even split.
  ![Cars Owned by State](path/to/cars_owned_by_state.png)
