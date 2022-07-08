# JP Morgan Chase & Co. Branch Optimization Project
This is a repository for my collaborative term project completed for BUS4022 Programming Fundamentals for Analytics during my post-graduate studies at George Brown College in Analytics for Business Decision-Making

## Project Background
JPMorgan Chase & Co. (NYSE: JPM) is a leading global financial services firm with assets of $1.2 trillion and operations in more than 50 countries. The firm is a leader in financial services for consumers and several other lines of business. JPM serves millions of consumers in the United States under its JPMorgan and Chase brands (Chase Bank).

Our goal was to develop branch optimization strategies in the United States that will:
1. **Optimize use of branch channels for retail customers.**
2. **Increase Primary Banking customer base by 9% by December 31, 2016.**
3. **Enhance use of existing branch channels to keep client retention and grow its customer base.**

We were provided with  Chase Bank data for retail deposits (i.e. mainly checking and savings accounts) at the branch level from 2010 to 2016. This includes information on locations across the United States, the date in which the branch was established, and acquired date if applicable. 

A sample of raw dataset can be viewed [here via ipynb](https://github.com/tlieva/JPM-branch-optimization-project/blob/668c0d877f76fda5bf05123ff825b0de9931a848/JPmorgan_chase_raw.ipynb).


Applications used: SAS, Tableau

## Methodology
**Summary of approach:** To develop appropriate optimization strategies, we looked to identify underperforming branches under JPMorgan Chase & Co by segmenting the deposit data provided by the firm by state, county, and city. Performance will be measured by analyzing the year-over-year, share of segments, total and average deposits at each segment level to identify the underperforming branches that require further evaluation to increase optimization. Appropriate recommendations are to be provided based on identification of underperforming branches at JPMorgan Chase & Co.

Data cleaning and processing was completed via Structured Query Language (SQL)-based queries in SAS analytical software whereby duplicate records and outliers were removed from the raw dataset. This was determined by identifying the upper outer limit of the interquartile range which excluded the extreme outliers from the dataset with deposits from 2010 to 2016 totalling to greater than $2,000,000. 

Furthermore, branches that have not been active over the last seven years from 2010 to 2016 with deposits totalling to less than $10 were also removed from the final analytical file. 

The final processed data was exported from SAS into an Excel file for further modeling and forecasting in Tableau. Data at the data source level was pivoted to accurately display time series calculations, and generate yearly growth rates, segment shares and average deposits using table calculations. 

**Applications used:** SAS, Tableau

**Copy of Cleaned CSV file:** [Downloaded from here](https://github.com/tlieva/JPM-branch-optimization-project/blob/668c0d877f76fda5bf05123ff825b0de9931a848/Analytical-file.xlsx)


## Summary Data Analysis & Findings
 - Analysis was conducted using a top-down approach which identified New York as the state of interest with the highest average deposits across the country. Furthermore, its average growth rate has reached 9.3% over the last 7 years. 
 - When assessing segmentation by counties, Suffolk and Westchester show indications of underperformance in comparison with the rest of the counties. These counties were found to have lower than average deposits despite having a large number of branch locations at 84 and 91 branches, respectively, when compared to counties with similar numbers. 
 - Further segmentation by city level within the two counties identified six branches of concern that had a negative growth rate in 2016. 

#### Therefore, our group presents the following three main recommendations:  
1. **Re-assess the location of underperforming branches**
2. **Optimize branches in cities with high numbers of branches and low average deposits**
    - Counties with a high number of branches and lower average deposits should be targeted for branch optimization strategies. 
    - Underperforming branches should either be slated for closure or audited to determine the cause for negative growth rates 
3. **Assess whether cities with a single branch can sustain the opening of additional locations in the city based on forecasted figures; and implement recommended branch optimization strategies.**
    - Branch optimization strategies should target branches that hold a large share of the segment to ensure that growth rate is not impacted by underperformance in the future. 
    - Using the forecasts built into the interactive dashboard, managers can determine if future growth rates indicate a need for branch optimization based on historical trends.
    
#### Branch Optimization Strategies
- Increase digital channels marketing these online platforms to increase client interactions with branches as mobile adoption has increased in recent years (Gujral et al., 2020).
- Consider reduction or removal of fees for transactions over the monthly limit will also encourage clients to make more deposits or transfer funds between accounts without fear of penalty (Fettig & Feldman, 1998).
- Increase rebates for opening new accounts to encourage making more deposits, and offer to round out transactions made on credit cards by depositing the remainder into savings accounts. 
- In conjunction with removing monthly transaction limits, this would increase the amount of money being deposited into savings accounts and increase customer retention.
    
#### The Forecasting Model
The forecasting model also provides the institution the ability to make more informed decisions on the immediate future of the firm and for a more data-driven approach in strategic planning including for branch optimizations. This will also allow JPMorgan Chase to assess whether short-term goals are being met and develop action plans in anticipation of down years.

### Interactive Dashbaord
The purpose of this dashboard is to assist the Chase Bank to identify, monitor and improve on the branches that are underperforming at the county, city and state level by using Year over Year Growth Rate, Share of Segment and Average Deposits as measurement metrics.

Link to [Interactive Dashboard](https://public.tableau.com/views/JPMorgan_ChaseStory_16537215416810/JPMorgan_Chase?:language=en-US&publish=yes&:display_count=n&:origin=viz_share_link)


## References
Gujral, V., Malik, N., & Taraporevala, Z. (2020, April 13). Rewriting the rules in retail banking. McKinsey & Company. Retrieved December 14, 2021, from https://www.mckinsey.com/industries/financial-services/our-insights/rewriting-the-rules-in-retail-banking. 

Fettig, D., & Feldman, R. J. (1998, July 1). Declining deposits ... is it all bad news? Federal Reserve Bank of Minneapolis. Retrieved December 14, 2021, from https://www.minneapolisfed.org/article/1998/declining-deposits-is-it-all-bad-news 
