# Marketing Campaign Analysis  - Fashion Brand

## About the Data
The dataset is a Microsoft Excel file that contains one table, consisting of **9,900 rows and 18 columns**, of the Daily performance metrics, of a Marketing Campaign data for a **UK Fashion brand**, carried out during 3 seasons in 2023 - Spring (March to May), Summer (June to August), and Fall (October to November). The dataset was gotten from [Onyx Data](https://onyxdata.ck.page/datadna-jun-2024).  

## Business Need 
A comprehensive Power BI report that:
-	Analyzes the Marketing Campaign performance metrics
-	Provides insights into the effectiveness of each campaign, and 
-	Identifies opportunities for optimization.
## Target Audience
-	Technical and Non-technical Business Users
## Skills/Concepts applied
-	Defining & Computing KPIs
-	Cleaning/Validation in Power Query
-	Power BI DAX Concepts: Calculated Measures
-	Data Visualization in Power BI
-	Power BI Dashboard building
-	Filters and Slicers
- Bookmarks and Tooltips 
-	Microsoft PowerPoint (to enhance UI design & commentary)
-	
## Defining Key Performance Indicators (KPIs)
The following metrics were identified as essential Key Performance Indicators (KPIs) to provide the business user with insights into the effectiveness of each campaign, and  Identify opportunities for optimization:

**Provided KPIs (Within the dataset)**
- _Impressions_ – Daily impressions (times ad was shown to a viewer) for each ad
- _CTR (%)_ - Daily average click-through rate for each ad
- _Clicks_ - Daily clicks for each ad
- _Daily Average CPC_ - Daily average cost-per-click for each ad
- _Spend, GBP_ - Total daily amount of advertising spending for each ad, in Great Britain Pounds(GBP)
- _Conversions_ - Total daily purchases attributed to a specific ad
- _Total Conversion Value, GBP_ - Total amount received from purchases attributed to a specific ad (Revenue)
- _Likes_ - Total daily likes (or other reactions) per ad
- _Shares_ - Total daily shares per ad (For the simplicities sake, each Pin on Pinterest was counted as a share)
- _Comments_  - Total daily comments per ad


**Additional(computed) KPIs.**
- Total Engagement - _What is the overall level of user interaction or engagement with our Ads across different metrics (likes, shares, and comments)?_
- Conversion rate (%) - _What percentage of ad viewers are converting into Paying customers?_
- Cost per Acquisition - _How much does it cost to acquire a single customer?_
- Return on Ad-spend (ROAS) - _How much revenue is generated for every dollar spent on advertising?_
- Return on Investment (ROI) (%) - _How much profit or loss is generated from our investment relative to its cost?_
- Monetary ROI (£) - _What is the net financial return (in monetary terms) on our investment after accounting for all costs and revenues?_

## Data Transformation/Preprocessing
The dataset was imported into Power BI’s Power Query for data validation and cleaning.  The column profiling was changed from ‘based on Top 1000 rows’ to ‘based on entire dataset’. ‘Column quality’ and ‘Column distribution’ checkboxes were selected to get a summary information about each column for effective cleaning/Preprocessing. The data table was fairly clean and required minimal transformation, which was carried out as follows:
- Column datatypes were validated appropriately - the data types of Impressions, Clicks and comments columns were changed from decimal to whole number. The data type of Click-through rate (CTR) column was changed from decimal to percentage.
- Columns that contain financial data such as the daily “Average CPC (cost-per-click) & Spend (GBP) Columns were rounded off to 2 decimal places, for consistency.
- There were no missing values, empty cells or duplicates
To enable flexibility of time-based analysis, a **Calendar Table** was then created in power query using the 


## Data Modelling
The Model from the cleaned data is a **basic Star Schema** comprising of:
one fact table (the data table) and two, dimension tables (Calendar & Image). The `date` column from the Marketing data table was connected to the `date` column in the calendar table, via a Many-to-one relationship while the `channel` column from the Marketing data table was connected to the `Channel` column in the image table, via a Many-to-one relationship. This is shown in the image below:

## Data Exploration (EDA)
With the data now transformed and modelled, it’s time to explore the data to analyze the Marketing Campaign performance metrics, in order to provide insights into the effectiveness of each campaign, and Identify opportunities for optimization, in response to the Business need. 

I approached the analysis by segmenting it into 3 Levels – **Campaign, Channel and Ad performance**, with filters, slicers and tooltips to enable interactivity and drill-down into other categories such as Cities, device, and Month.

The metrics were then analyzed & summarized within 3 areas – **Engagement, Revenue generated and Cost Analysis**. To analyze **Engagement performance** of the campaign, the following DAX Measures were created:

## KPI Visualization/Presentation (WIP)
Our Fashion brand needed to increase its revenue while staying above the competition. We thought, in our current digital global village, what other way than a digital marketing campaign - **3 Seasons, Endless Style**😉.  Every weather season has an attire for it, and so we launched into the deep. 


_**What should be done?**_    

- The **highest engagement was observed in London**
→ This indicates a strong interest that can be leveraged to drive more clicks and conversions by refining ad content with compelling calls to action.     
- **Birmingham showed the highest clicks and conversion rate**, suggesting it is highly effective at turning interest into purchases.    
→ Allocating more budget to Birmingham could maximize conversions.
- **Manchester**, despite lower engagement and click, **generated the highest revenue**, indicating effective campaigns.     
→ Analyzing successful strategies in Manchester and replicating them in other locations could further enhance performance.
 
**For the Devices:**
- **Desktop ads** outperformed mobile in terms of click-to-conversion rate and revenue. This suggests maintaining a strong focus on desktop-targeted campaigns, with high-quality, detailed ad content optimized for larger screens.

- Mobile performance can be improved by ensuring ads are mobile-optimized, with responsive design and faster load times. Introducing mobile-specific promotions and enhancing the mobile user experience could boost engagement and conversions, helping to capture a broader audience effectively.
  

**So, what about other 2 channels - _Instagram and Pinterest_.**

Well, Our **Instagram** Users showed higher interest in the campaign offer than Facebook, having recorded the **highest number of conversions (15 thousand+) and highest revenue of over £684,000**. Wow! that’s great. 😀

**Now, where is Pinterest in all of this?** 🤔

Interestingly, despite having the lowest engagement and Click-through rate (CTR), **Pinterest had the highest conversation rate(26.83%) and highest Return on Ad-Spend (ROAS) (22.47)** among the channels. 

Additionally, I carried out cost analysis to evaluate how efficient our investment in the 3 channels were.

From the above visual, the average Cost-per-Click (CPC) for _Facebook_ is £1.04, and the cost per acquisition (CPA) is £5.45, which is relatively high; and despite having the largest Ad-spend, it had the lowest Profit/Return-On investment (ROI). 

_Instagram_, on the other hand, had the highest Revenue & Profit/Return-On investment (ROI). With a CPC of £1.00, CPA is £4.07, and an Ad-Spend slightly lower than Facebook's, it generated a ROI of £621.37K. 

_Pinterest_ is seen to be the most cost-effective across the channels - despite having the lowest Ad-spend of £28.24K , it was the next best in terms of revenue and ROI, having generated a Profit/Return-On investment (ROI) of £606.47K

**For Facebook**: 
-	Improve conversion rate and ROAS by refining ad targeting and testing new creatives. 
-	Consider segmenting audiences further to identify high-intent users. 
  
**For Instagram**: 
-	Scale up Instagram campaigns by increasing the ad spend on high-performing ads. 
-	Leverage the high engagement rates by creating more interactive and visually appealing content. 
-	Additionally, use Instagram Stories and Reels to tap into a wider audience and boost conversions.
  
**For Pinterest**: Pinterest's strong conversion performance indicates a high potential for scalable growth with increased investment, thus:
-	Significantly increase the ad spend on Pinterest campaigns. 
-	Focus on scaling successful ad formats and targeting strategies. 
-	Consider expanding to new audience segments and utilizing promoted pins to enhance visibility

It’s now time to evaluate the 2 Ad categories – _**Discount and Latest collection**_

Among the 2 Ads used for the campaign, we see from the visual above that Discount ads lead in overall engagement metrics, including likes and Comments. However, Collection ads have more clicks despite having fewer conversions and lower Return on Ad-Spend. Discount ads have a lower CTR but a significantly higher conversion rate and ROAS compared to Collection ads.

In terms of Cost analysis,  the visual above shows that Collection ads are slightly more cost-effective in terms of Cost Per Acquisition (CPA) and Cost-Per-Click (CPC) compared to Discount ads. Although Discount ads have a higher ad spend, they yield a significantly higher return on investment (ROI) in terms of monetary value compared to Collection ads.

_**How do we Improve on the Ads?**_

There are opportunities for optimization/Scaling based on the Ads performance:

**For Discount Ads:**

_Strength_: **High conversion rate and ROAS** indicate strong performance in converting clicks to revenue.

**Opportunity**:
-	 Increase the ad spend for Discount ads to capitalize on the high conversion efficiency. 
-	Enhance targeting strategies to further improve CTR and engagement, especially leveraging the high like and share rates.
  
**For Collection Ads:**

_Strength_: **Higher CTR** indicates effective ad appeal and relevance to the audience.

**Opportunity**: 
-	Focus on improving the conversion rate by refining landing pages and checkout processes. 
-	Consider optimizing ad creatives to maintain high engagement while driving more conversions. 
-	Test variations in ad copy and visuals to determine the best-performing combinations.

## Conclusion
In Summary, Consideration should be given to _shifting budget from underperforming areas to high perfoming areas_ to optimize overall campaign performance. 
One way to do this will be by **reallocating budget to top-performing ads like discounts, and channels like Pinterest & Instagram.**

