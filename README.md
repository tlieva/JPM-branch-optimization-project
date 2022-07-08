# JP Morgan Chase & Co. Branch Optimization Project
This is a repository for my collaborative term project completed for BUS4022 Programming Fundamentals for Analytics during my post-graduate studies at George Brown College in Analytics for Business Decision-Making

## Project Background
JPMorgan Chase & Co. (NYSE: JPM) is a leading global financial services firm with assets of $1.2 trillion and operations in more than 50 countries. The firm is a leader in financial services for consumers and several other lines of business. JPM serves millions of consumers in the United States under its JPMorgan and Chase brands (Chase Bank).

Our goal was to develop branch optimization strategies in the United States that will:
1. **Optimize use of branch channels for retail customers.**
2. **Increase Primary Banking customer base by 9% by December 31, 2016.**
3. **Enhance use of existing branch channels to keep client retention and grow its customer base.**

We were provided with  Chase Bank data for retail deposits (i.e. mainly checking and savings accounts) at the branch level from 2010 to 2016. This includes information on locations across the United States, the date in which the branch was established, and acquired date if applicable. 

The raw dataset can be found here.

Applications used: SAS, Tableau

## Methodology
**Summary of approach:** To develop appropriate optimization strategies, we looked to identify underperforming branches under JPMorgan Chase & Co by segmenting the deposit data provided by the firm by state, county, and city. Performance will be measured by analyzing the year-over-year, share of segments, total and average deposits at each segment level to identify the underperforming branches that require further evaluation to increase optimization. Appropriate recommendations are to be provided based on identification of underperforming branches at JPMorgan Chase & Co.

Data cleaning and processing was completed via Structured Query Language (SQL)-based queries in SAS analytical software whereby duplicate records and outliers were removed from the raw dataset. This was determined by identifying the upper outer limit of the interquartile range which excluded the extreme outliers from the dataset with deposits from 2010 to 2016 totalling to greater than $2,000,000. 

Furthermore, branches that have not been active over the last seven years from 2010 to 2016 with deposits totalling to less than $10 were also removed from the final analytical file. 

The final processed data was exported from SAS into an Excel file for further modeling and forecasting in Tableau. Data at the data source level was pivoted to accurately display time series calculations, and generate yearly growth rates, segment shares and average deposits using table calculations. 

**Applications used:** SAS, Tableau


## Summary Data Analysis & Findings


