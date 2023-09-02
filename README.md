# VIVENDO-FOOD-CLAIMS-ANALYSIS
This analysis was carried out on Vivendo Fast Food, a restaurant in Brazil with over 200 outlets. This Fast Food received feedback on Customers’ Satisfaction, which include complains of food poisoning. Each customer gets compensation for every food poison claim.
The legal team working for Vivendo Fast Food operate from offices in four locations across the country. In order to improve the duration of time to respond each customer’s claim and the close time for each, the Head of Legal Team wants a report on how location differs in the duration it takes to close claims.
# Business Question asked by the Head of Legal Team are as follows;
•	How does number of claims differ by the four locations?

•	What is the distribution of time for all claims?

•	What is the average time taken to close claims in each location?

Dataset: The data set is made-up of 2000 unduplicated rows and 8 columns.

Description: The description of the dataset is given as follows;

•	Claim_id: Nominal, the unique identifier of the claim.

•	Time to close: Discrete, the number of days to close the claim.

•	Claim amount: Continuous, the initial claim requested in the currency of Brazil (R$), rounded to 2 decimal places.

•	Amount paid: Continuous, final amount paid. In the currency of Brazil (R$). Rounded to 2 decimal places.

•	Location: Nominal, Location of the claim, one of “RECIFE”, “SAO LUIS”, “FORTALEZA”, or “NATAL”.

•	Individuals on claim: Discrete, number of individuals on this claim. Ranging from 1 to 15

•	Linked cases: Nominal, whether this claim is linked to other cases. Either TRUE or FALSE.

•	Cause: Nominal. Cause of the food poisoning. One of “vegetable”, “meat” or “unknown”.
# Data Inspection
The following checks were carried on the dataset to ensure its completeness and readiness for analysis, these include; missing values, data type, inconsistency, duplicates and relevancy of the dataset.
# Observations and Data Cleaning
The following observations were found, accompanied by the respective Data Cleaning carried out.
a. The data in the Claim_amount column was wrongly formatted as “General” and there were inconsistencies in the decimal place. The values range from 0, 1 to 2 decimal places.

The Amount_paid values were not in the currency of Portuguese Brazil R$ and there were inconsistencies in the decimal place.

The Individuals_on_claim values are. However, column format was in “General”

The values match the description. However, there are 16 inconsistencies in the spelling and capitalization of “vegetable” as “VEGETABLES”

b. The Amount_paid column contained 36 missing values

The Linked_cases column contained 26 missing values

c. The Inconsistency in the Claim_amount was resolved as follows
      1.	The column was formatted to “Currency” and “2 Decimal places” by using Find and Replace. 
      2.	The R$ was replaced with blank space 
      3.	The blank space was formatted to “Currency”, 2 Decimal Place and symbol changed to “R$ (Portuguese Brazil)” in the               Find and Replace Dialogue Box.

The Missing Values and inconsistencies in the Amount_paid was resolved as follows;
Missing values was filled with the Median amount paid and this was calculated and follows;
      1.	Median amount_paid was calculated using =MEDIAN(D2:D2001)
      2.	Missing values was filtered and replaced with the Median amount paid (20,105.70) using  “Find and Replace”.
      3.	The column was formatted to Brazilian Currency “R$ (Portuguese Brazil)”, 2 Decimal Places using the Format Cell.

The Individual_on_claim Column Format was change to “Number”

The 26 missing values in the Linked_cases were replaced with FALSE using “Find and Replace”

In the Causes column, the 16 inconsistent spellings were replaced with “vegetable” using “Find and Replace”

