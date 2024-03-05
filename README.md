# VIVENDO-FOOD-CLAIMS-ANALYSIS
This analysis was carried out on Vivendo Fast Food, a restaurant in Brazil with over 200 outlets. This Fast Food received feedback on Customers’ Satisfaction, which include complaints of food poisoning. Each customer gets compensation for every food poisoning claim.
The legal team working for Vivendo Fast Food operates from offices in four locations across the country. In order to improve the duration of time to respond to each customer’s claim and the close time for each, the Head of Legal Team wants a report on how location differs in the duration it takes to close claims.
## Business Questions asked by the Head of Legal Team are as follows;
- How does number of claims differ by the four locations?
- What is the distribution of time for all claims?
- What is the average time taken to close claims in each location?

## Dataset: 
The data set is made-up of 2000 unduplicated rows and 8 columns.

## Description: 
The description of the dataset is given as follows;

- Claim_id: Nominal, the unique identifier of the claim.
- Time to close: Discrete, the number of days to close the claim.
- Claim amount: Continuous, the initial claim requested in the currency of Brazil (R$), rounded to 2 decimal places.
- Amount paid: Continuous, final amount paid. In the currency of Brazil (R$). Rounded to 2 decimal places.
- Location: Nominal, Location of the claim, one of “RECIFE”, “SAO LUIS”, “FORTALEZA”, or “NATAL”.
- Individuals on claim: Discrete, number of individuals on this claim. Ranging from 1 to 15
- Linked cases: Nominal, whether this claim is linked to other cases. Either TRUE or FALSE.
- Cause: Nominal. Cause of the food poisoning. One of “vegetable”, “meat” or “unknown”.
  
## Data Inspection
The following checks were carried on the dataset to ensure its completeness and readiness for analysis, these include; missing values, data type, inconsistency, duplicates and relevancy of the dataset.

## Observations and Data Cleaning
The following observations were found, accompanied by the respective Data Cleaning carried out.
- The data in the Claim_amount column was wrongly formatted as “General” and there were inconsistencies in the decimal place. The values range from 0, 1 to 2 decimal places.
- The Amount_paid values were not in the currency of Portuguese Brazil R$ and there were inconsistencies in the decimal place.
- The Individuals_on_claim values are. However, column format was in “General”
- The values match the description. However, there are 16 inconsistencies in the spelling and capitalization of “vegetable” as “VEGETABLES”
- The Amount_paid column contained 36 missing values
- The Linked_cases column contained 26 missing values
- The Inconsistency in the Claim_amount was resolved as follows
      - The column was formatted to “Currency” and “2 Decimal places” by using Find and Replace. 
      - The R$ was replaced with blank space 
      - The blank space was formatted to “Currency”, 2 Decimal Place and symbol changed to “R$ (Portuguese Brazil)” in the Find and Replace Dialogue Box.

- The Missing Values and inconsistencies in the Amount_paid was resolved as follows;
- Missing values was filled with the Median amount paid and this was calculated and follows;
      - Median amount_paid was calculated using =MEDIAN(D2:D2001)
      - Missing values was filtered and replaced with the Median amount paid (20,105.70) using  “Find and Replace”.
      - The column was formatted to Brazilian Currency “R$ (Portuguese Brazil)”, 2 Decimal Places using the Format Cell.

- The Individual_on_claim Column Format was change to “Number”

- The 26 missing values in the Linked_cases were replaced with FALSE using “Find and Replace”

- In the Causes column, the 16 inconsistent spellings were replaced with “vegetable” using “Find and Replace”
## Data Exploration and Visualization
- Create a visualization that shows the number of claims in each location. Use the visualization to:
![image](https://github.com/Adesugba1/VIVENDO-FOOD-CLAIMS-ANALYSIS/assets/143879001/8c32539c-751b-4cf4-96f2-b9a1f9512b46)

### State which category of the variable location has the most observations.
According to the chart above, the category with the most observations is Recife with a total number of 885 claims.

### Explain whether the observations are balanced across categories of the variable location.
The bar chart above shows that, the observations are not balance across categories as claims in Natal is 287 (lowest claims) and Recife recorded 885(highest claim) within the four locations. This means that, claims in Recife is 208% more than claims in Natal, 71% more than claims in Sao Luis and 185% more than claims in Frontaleza. The Bar Chart was chosen because the visualization involves Categorial data (Location) and Continuous data (Number of Claims).

### Describe the distribution of time to close for all claims. Your answer must include a visualization that shows the distribution.
![image](https://github.com/Adesugba1/VIVENDO-FOOD-CLAIMS-ANALYSIS/assets/143879001/c8545f12-17bd-40fc-994a-0261390ee5cb)
From the chart above, 1428 claims take between 100 to 199 days to close, 489 claims take 200 to 299 days to close, 53 claims take between 300 to 400 days to close, 24 claims take less than 100 days to close and 6 claims take more than 400 days to close. The column chart was chosen because the description deals with categorical data (grouped time to close) and continuous data (no of claims).

### Describe the relationship between time to close and location. Your answer must include a visualization to demonstrate the relationship
![image](https://github.com/Adesugba1/VIVENDO-FOOD-CLAIMS-ANALYSIS/assets/143879001/4f580581-8b74-4e96-af2c-92c7a414297b)
The box plot shows the five summary of the time to close for all claims and the outliers. From the box the minimum is given as 76, lower quartile is given as 158, median is given as 179, upper quartile is 204 and the maximum is 518. Also, the statistical data set is normally distributed.
