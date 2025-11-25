# Consumer Financial Complaints Analysis

### Overview
This project was created as part of my participation with **Onyx Data Challenge**, where I analyzed consumer complaints. The mission is to create an analytical report that identifies patterns in complaints, evaluates company responses, and highlights areas of concern for regulators and consumers. Using Power BI, I designed an interactive 6-page dashboard that provides a comprehensive view of consumer issues, product performance, and company responsiveness. 


### Data
Consumer Financial Protection Bureau (CFPB), a U.S. government agency ensuring fairness and accountability in the financial sector. The CFPB collects complaints from consumers across the United States regarding financial products and services. Each complaint is tracked from submission through company response.
#### Data Source
  - downloaded from onyx data dataDNA [website](https://datadna.onyxdata.co.uk/challenges/october-2025-datadna-consumer-financial-complaints-analytics-challenge).
#### Data Dictionary
  |         Column   Name        |                                   Description                                  |
  |:----------------------------:|:------------------------------------------------------------------------------:|
  |         Complaint ID         |                      Unique identifier for each complaint.                     |
  |         Submitted via        |         Submission channel used by the consumer (e.g., Web, Referral).         |
  |        Date submitted        |                   Date the consumer submitted the complaint.                   |
  |         Date received        |          Date the authority/company recorded receipt of the complaint.         |
  |             State            |                           U.S. state of the consumer.                          |
  |        State_Latitude        |  Latitude of the state centroid. REQUIRED for ZoomCharts Drill Down Map   PRO. |
  |        State_Longitude       | Longitude of the state centroid. REQUIRED for ZoomCharts Drill Down Map   PRO. |
  |            Product           |         Financial product category (e.g., Mortgage, Credit reporting).         |
  |          Sub-product         |            More specific product type (e.g., Conventional mortgage).           |
  |             Issue            |               General problem category reported by the consumer.               |
  |           Sub-issue          |                       More detailed problem description.                       |
  |    Company public response   |           Public statement from the company regarding the complaint.           |
  | Company response to consumer |      Outcome communicated to the consumer (e.g., Closed with explanation).     |
  |       Timely response?       |      Whether the company responded within the required timeframe (Yes/No).     |
  |         Census_Region        |       U.S. Census region for the state (Northeast, Midwest, South, West).      |
  |        Census_Division       |           U.S. Census division for the state (nine-division scheme).           |
  |     Company_Response_Date    |                             Company response date.                             |
  |        Company_ID_1081       |                   Company identifier (COMP-0001 … COMP-1081).                  |
  |      Response_Time_Days      |        Calculated days between Date submitted and Company_Response_Date.       |
  |        Company_ID_1081       |                   Company identifier (COMP-0001 … COMP-1081).                  |
  |     Market_Share_Percent     |          Market share percentage; sums to ~100% across all companies.          |
  |       Reputation_Score       |                           Reputation score (50–100).                           |
  |      Enforcement_History     |                   Flag for past regulatory actions (Yes/No).                   |
  |       Company_Size_Tier      |             Company size classification based on market share rank.            |
  |        Complaint_Count       |          Number of complaints linked to the company (from fact table).         |
  |     Timely_Response_Rate     |    Percentage of complaints marked 'Timely response?' = Yes for the company.   |
  |    Avg_Response_Time_Days    |         Average days from submission to response date for the company.         |
  |   Complaints_per_1pct_Share  |       Complaint_Count divided by Market_Share_Percent; normalization KPI.      |


### Purpose
The aim is to provide report that identifies patterns in complaints, evaluates company responses, and highlights areas of concern. The report should address the following questions:

- When do complaints rise or fall over time?
- Which states and regions are hotspots?
-	Which products and sub-products drive the most complaints?
-	Which issues and sub-issues are most common or most severe?
-	How fast, and how timely are company responses to complaints?
-	Which companies show the highest complaint rates relative to market share?
-	Do company traits (size tier, reputation, enforcement history) correlate with outcomes?
-	Do submission channels differ in response speed or outcomes?

### Analysis
- **62,516** total complaints was submitted in the span of 5 years.
- Complaints tend to rise in midyear and fall during start and end of the year which indicates a seasonal pattern.
- **1,081** companies received complaints and **93.8%** of them responded timely.
- Companies based in **South** and **West** region of the USA received the most complaints which is **69.1%** of the total.
- **California**, **Florida**, and **Texas** state-based companies are the main generator of complaints which is **40%** of the total.
- **Checking or savings account**(24,814), **Credit card or prepaid card**(16,197), and **Credit reporting, credit repair services or other personal consumer reports**(7,710) is the 3 most complained products which is approximately **80%** of the total complaints.
  - Within the products, **Checking Accounts**(20,768), **General-purpose credit card or charge card**(13,404), and **Credit Reporting (7,340)** sub-products received the most complaints.
- **Account Managemnt**, **Incorrect Report Data**, and **Statement Purchase Problem** are the main issue complained by consumers.
- Companies generally respond within **15 days** after complaints have been submitted.
- **COMP-0077** have the highest complaint count relative to the market share which is **63.93%**.
- Most complaints are submitted via **Web**.
- Difference in submission channel does not have a remarkable margin that indicates increase or decrease in response time.
- Small-sized companies receives the most complaints by a large margin.

### Reference
Refer to my LinkedIn [post](https://www.linkedin.com/posts/batchaaan22_datadna-powerbi-share-7387363758173675521-Grh8?utm_source=share&utm_medium=member_desktop&rcm=ACoAADU37-4BvZkdxoNILB6GhzRJGT7OoLWMMoY) to view my submission.
