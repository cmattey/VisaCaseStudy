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
><b>Assumptions</b>
<br>
1. The location for our store is chosen at the closed Chile Pie store which is situated at the <b>corner of Baker and Fulton Street</b>.<br>
2. The nature of the grocery store, and the types of products we plan to sell has not been finalized and will not be considered in our analysis. In fact, we will use some of the results from our analysis to inform our decision of the types of goods to import and sell( More on that later).<br>
3. All the data used in the analysis is real world data and is available free of charge on open source data sites such as sfgov.org, datasf.org, zillow.com etc.
<br>
>**Analysis**
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
During the Rent trend analysis we chose to use Time Series Analysis and not conventional Machine Learning techniques such as Regression or Random Forests because Regression requires the observations to be independant, but in our case they are dependant on time and therefore prime candidates for using Time Series analysis. Statistical significance for stationarity was found early in the analysis using the Dickey Fuller test **_(p-value = 0.02)_**.



