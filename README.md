# VisaCaseStudy
An exploration of case studies provided by VISA

>CASE STUDY 1:<br>
>How would you determine if a specific block in your neighborhood is suitable for a new grocery store??

## Proposal

Our Proposal will cover the following sections:
1. Assumptions - To frame the problem
2. Analysis Methodology - To explain your analysis approach and chosen analytics techniques
3. Expected Results and Findings
4. Recommendations – Based on expected results and findings
5. Potential Limitations inherent in the approach

<br>
Here we layout the assumptions and some basic groundwork for our analysis.<br><br>
Consider the Plotline:<br>
You are a very talented individual, who has recently decided to take the grocery world by storm. And your first order of business is to determine the suitability of a particular block in your neighbourhood. On your daily walk to the University, while contemplating about your new found interest in the world of retail, you come across this sign:
<br>
<img src="https://github.com/cmattey/VisaCaseStudy/blob/master/images/chile_closed.jpg" alt="Chile Closed" width="500" height="500">
<br>
Your favorite Pie Store has shut down! But being the optimist that you are, you look on the bright side, and see this as an opportunity. What if this is the new site for your grocery store!? You decide to put your analysis skills to the test.
<br>
### Assumptions
<br>
1. The location for our store is chosen at the closed Chile Pie store which is situated at the <b>corner of Baker and Fulton Street</b>.<br>
2. The nature of the grocery store, and the types of products we plan to sell has not been finalized and will not be considered in our analysis. In fact, we will use some of the results from our analysis to inform our decision of the types of goods to import and sell( More on that later).<br>
3. All the data used in the analysis is real world data and is available free of charge on open source data sites such as sfgov.org, datasf.org, zillow.com etc.
<br>
### Analysis
<br>
Through out our analysis we researched specific areas of concern that will help us make an informed decision while determining the suitability of our chosen location. The areas addressed were as follows:<br>
1. Security<br>
2. Population Demographics around the block<br>
3. Types of nearby businesses<br>
4. Rent in the area<br>
<br>
Details about the analysis and the source code can be found in the Ipython Notebook included in the associated repository.<br>
In each of the above mentioned areas, we begin our analysis by looking at our data, and its description. We check for missing values that might affect our analysis, we plot out the features of interest, looking at the distribution if the features are numeric or at barplots if they are categorical. As we wil see, most of the features of interest in our analysis were categorical in nature.<br>
We took the following approach:<br>
1. Get a fair idea of our data using exploratory techniques such as plotting etc.<br>
2. Extract the relevant features of interest from the data.<br>
3. Look for either visible patterns or use Machine Learning models/ Time series analysis to predict patterns in our data.<br>
4. Use the insights gained from the analysis to inform our decision and make recommendattions.<br>
<br>
During the Rent trend analysis we chose to use Time Series Analysis and not conventional Machine Learning techniques such as Regression or Random Forests because Regression requires the observations to be independant, but in our case they are dependant on time and therefore prime candidates for using Time Series analysis. Statistical significance for stationarity was found early in the analysis using the Dickey Fuller test(<b>p-value = 0.02</b>).

### Results an Findings
> Security

Security is a major concern while planning to run a successful business. We need to ensure that our store is located in a safe neighbourhood, to ensure the safety of our customers and staff. <br>
We found that our store was located in the Park district which has the least number of distress calls made in the year 2018 so far. We plotted the Crime statistics for the store vicinity and found that the number was as low as 25  compared to the total  46,668 distress calls made in 2018 in the city.<br>
<img src="https://github.com/cmattey/VisaCaseStudy/blob/master/images/SF_District.png" alt="Store Location" width="400" height="400"><br>
<h4> Crime Statistics by District</h4>
<img src="https://github.com/cmattey/VisaCaseStudy/blob/master/images/crime_stats_district.png" alt="Crime stats by District" width="600" height="500"><br>
<h4> Crime statistics near our store</h4>
<img src="https://github.com/cmattey/VisaCaseStudy/blob/master/images/crime_stats_local.png" alt="Crime stats near store" width="600" height="500"><br>

> Population Demographics in Store Vicinity

We looked at two particular aspects of the population, ie their Income and their ethnicity. We chose to analyze these two aspects as knowing the trend in the mean income of a household allows us to determine the economic stability of our customer base. Knowing the majority ethnicity of our customers can help inform decision about the types of goods to import and also help with specific marketing strategies.<br>
From our analysis we found that the households in the store vicinity had an increasing trend in household income and our location was on par with the rest of the city and even had a higher average household income in 2016.<br>
<h4>Household Income Trend in Store Vicinity</h4>
<img src="https://github.com/cmattey/VisaCaseStudy/blob/master/images/local_income_trend.png" alt="Local income trend" width="600" height="500"><br>
<h4>Household Income Comparison with the rest of the city</h4><br>
<img src="https://github.com/cmattey/VisaCaseStudy/blob/master/images/income_comparison_trend.png" alt="income_trend" width="600" height="500"><br>






