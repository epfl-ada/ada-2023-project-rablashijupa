# Analysing the reflection of cultural values in Wikipedia pageview trends

## Abstract: 
Hofstede cultural dimensions model, originally published in the 1970s, is a key tool for understanding cultural differences among countries. The cultures of each country are characterised by 6 scores : “Power Distance”, “Uncertainty Avoidance”, “Masculinity-Femininity”, “Long Term Orientation”, “Individualism”, “Indulgence”. 
This project aims at identifying the extent to which Wikipedia pageview trends across countries reflect the cultural values defined by Hofstede. Culture being defined as a set of values firmly anchored within a group of people, we will assume that each country's culture is stable over a 3-year window. We will thus:
 - Link some of the topics to one of the dimensions of the Hofstede model. For example, “Indulgence” dimension can be linked to the topics “Culture.Food and drink” (culinary practices often reflect indulgence or restraint) or “Culture.Media.Entertainment”.
- Compare the pageviews of each country on the topics related to each dimension to understand whether Wikipedia searches reflect the cultural values of these countries. 
- Look for similar patterns across groups of countries. 

## Research questions:
- To What Extent are Cultural Values, as defined by Hofstede’s dimensions, reflected in Wikipedia pageview trends?
- Do Wikipedia pageview trends reveal information about cultural similarities between different countries?
- Have cultural similarities between countries changed as a result of the COVID 19 pandemic?
- Are there any interesting trends in countries' interests over the 3 years (before and during Covid) ? 
- Is there a correlation between cultural interests and technological access?

## Additional datasets:
- Datasets to make a correlation between cultural interests and technological access :
  + Digital literacy dataset (downloaded from https://tcdata360.worldbank.org/indicators/hb0649ed2?country=BRA&indicator=41400&viz=line_chart&years=2017,2019)
      
  + Internet Usage Statistics: Include data on internet access and device usage per country : ICT Access and Usage by Household and Individual (downloaded from https://stats.oecd.org/Index.aspx?DataSetCode=ICT_HH2 )  

- Dataset used to see if Hofstede’s dimension are reflected in Wikipedia pageviews :
  + Hofstede dataset (downloaded from https://geerthofstede.com/research-and-vsm/dimension-data-matrix/)

## Methods to answer the research question:
### Step 0: Preprocessing  
- Language spoken in multiple countries: estimate the number of pageviews coming from each country based on a demographics dataset and internet usage statistics
https://fr.wikipedia.org/wiki/Wikip%C3%A9dia:Statistiques
https://stats.wikimedia.org/wikimedia/animations/wivivi/wivivi.html
- Scrap data on wikipedia pageviews for a longer period
- Normalise the number of pageviews for a topic by the number of articles in this specific topic

### Step 1: Cultural Value Reflection  
- Perform statistical analyses to compare Wikipedia pageview trends with Hofstede’s cultural dimensions. More specifically, we can use Pearson or Spearman correlation coefficients to assess the strength and direction of the relationship between Hofstede’s cultural dimensions and Wikipedia pageview patterns. This will help in determining if there’s a statistically significant correlation between cultural values and online browsing behaviour.
- ANOVA (Analysis of Variance) can be used to determine if there are statistically significant differences in Wikipedia pageviews between different countries.

## Step 2 : Cultural Similarities  
- Implement cluster analysis to identify groups of countries with similar Wikipedia browsing patterns.
- Examine shifts in these clusters pre and post the COVID-19 pandemic.
- We can use paired t-tests to determine if the differences in pageview trends pre and post COVID-19 are statistically significant

## Step 3 : Trend Analysis  
- Use time-series analysis to track changes in pageview trends over the specified period.
- Temporal Patterns : Analyse how cultural interests change over time and during specific events
- Perform a Difference in Difference regression to investigate any significant deviations during the pandemics and potentially get an estimation of the causal effect of Covid on the change in countries’ interests. The Control data would be the pageviews before Covid and the Treated data would be pageviews after Covid
- Time Series k-means (where we measure the similarity between two temporal sequences) : The defined clusters would be time sequences that overlap = topics that share similar pageview trends 

## Step 4 : Correlation with Technological Access    
- Compare Wikipedia pageviews statistics for mobile versus desktop 
- Analyse the relationship between technological access and the nature of Wikipedia pageviews: Cluster countries in groups according to their average ICT Access and Usage and Perform correlation analysis between pageview patterns within country clusters to understand if they have cultural similarities

## Step 5 : Seasonality Analysis  
- Study the seasonality of the top-viewed topics for each country using autocorrelation plots, periodogram, time serie decomposition (data can be decomposed either as the sum or product of trend, seasonality and residual components) 

# Proposed timeline  

- 17.11.22 Milestone 2 with Step 1 partly done
- 23.11.22 Step 1 + 2 done 
- 01.12.22 Homework 2 submission
- 03.12.22  Step 3+4 done
- 07.12.22 all data analysis done
- 10.12.22 Beginning writing the data story
- 19.12.22 Data story mostly finished, only polishing afterwards
- 21.12.22 Data story done
- 22.12.22 Milestone 3

# Organisation within the team  

Paolo :  
Shivang :   
Julien :  
Blanche :   
Rayan :   
 
