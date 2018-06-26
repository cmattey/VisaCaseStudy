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

>Consider the Plotline:<br>

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
3. All the data used in the analysis is real world data and is available free of charge on open source/government data sites such as sfgov.org, datasf.org, zillow.com etc.
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
<img src="https://github.com/cmattey/VisaCaseStudy/blob/master/images/SF_District.png" alt="Store Location" width="500" height="400"><br>
<h4> Crime Statistics by District</h4>
<img src="https://github.com/cmattey/VisaCaseStudy/blob/master/images/crime_stats_district.png" alt="Crime stats by District" width="600" height="500"><br>
<h4> Crime statistics near our store</h4>
<img src="https://github.com/cmattey/VisaCaseStudy/blob/master/images/crime_stats_local.png" alt="Crime stats near store" width="600" height="500"><br>

> Population Demographics in Store Vicinity

We looked at two particular aspects of the population, ie their Income and their ethnicity. We chose to analyze these two aspects as knowing the trend in the mean income of a household allows us to determine the economic stability of our customer base. Knowing the majority ethnicity of our customers can help inform decision about the types of goods to import and also help with specific marketing strategies.<br>
From our analysis we found that the households in the store vicinity had an increasing trend in household income and our location was on par with the rest of the city and even had a higher average household income in 2016. This ensures an economically stable customer base.<br>
<h4>Household Income Trend in Store Vicinity</h4>
<img src="https://github.com/cmattey/VisaCaseStudy/blob/master/images/local_income_trend.png" alt="Local income trend" width="600" height="500"><br>
<h4>Household Income Comparison with the rest of the city</h4><br>
<img src="https://github.com/cmattey/VisaCaseStudy/blob/master/images/income_comparison_trend.png" alt="income_trend" width="600" height="500"><br>

The ethnicty distribution told us that the majority of local customers were white, followed by Asians and African Americans. The distribution in the local tracts looked as follows:<br>
<img src="https://github.com/cmattey/VisaCaseStudy/blob/master/images/eth_count.png" alt="ethinicity count" width="700" height="500"><br>

> Types of nearby businesses

Analyzing the businesses in the vicinity of our store gives us information about other competing market traders and well as gives us information about the kind of customers which we might expect to see around our store, further helping us improve our marketing strategy. After filtering through the open businesses in the region, and looking at their types it could be seen that we have a lot of restuarants in our location, but not many grocery stores(in fact 0 according to the data). The high number of restaurants would mean a lot of foot traffic boosting our brand awareness.<br>
<img src="https://github.com/cmattey/VisaCaseStudy/blob/master/images/local_businesses.png" alt="local businesses" width="700" height="500"><br>
A more deatiled look at the types of local businesses can be found in the Python notebook.

> Rent Trend 

We looked at Rent trend in the store vicinity (zipcode:94117) from Nov 2013 to April 2018. This would help us determining our cost estimates in the coming months. Using this data, a time series forecaster was created using the ARIMA model to give us an approximate rent estimate. The rent in the coming months from May 2018 - August 2018 was found to be $4,580.<br>
<h4>Rent Trend around store location</h4>
<img src="https://github.com/cmattey/VisaCaseStudy/blob/master/images/rent_trend.png" alt="rent trend" width="700" height="500"><br>
<h4>ARIMA Time Series Predictions</h4>
<img src="https://github.com/cmattey/VisaCaseStudy/blob/master/images/rent_prediction.png" alt="arima predictions" width="600" height="500"><br>

### Recommendations

>From our analysis the following recommendations can be made:<br>
1. We have chosen a safe neighbourhood for our store so the store can remain open relatively late at night.<br>
2. Since the household income around the store is higher on average than the rest of the city, we can import relatively pricier products and be assured that these won't be shelved indefinitely.<br>
3. Since a majority of the nearby food businesses are restaurants, we can plan our marketing around the peak timings at these restaurants to increase our brand awareness and capture some of the overflow.<br>
4. Rent prediction helps us plan our initial investments with more confidence, and allows us to segregate our investments to different aspects of the business such as additional infrastructure, marketing.<br>

### Potential Limitations

The main limitation of our analysis is that not all of the data is up-to-date. The local household income analysis was done from 2013 to 2016. And we are not considering the trends in the last couple of years. Also the rent analysis was done for Multi-Family 5+ units and not commerical spaces so the actual rent trend might be different from the one we have predicted. Also our rent time series was within 5% of stationarity, we can further increase to this to within 1% by using methods that remove trend and seasonality using Aggregation, Smoothing and Decomposition.<br>

> That Concludes our Proposal. Thank you for reading!<br>I encourage you to take a look at the Python Notebook for more details about the analyis. Feel free to contact me for suggestions and improvements. Thank you!

