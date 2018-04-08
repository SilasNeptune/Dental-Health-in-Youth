# Steps taken for Data Wrangling Capstone 1 Dental Predictions Wrangling 


The libraries imported were Pandas and NumPy.
So far I have 6 different files that all needed to be cleaned and prepared. Most of them came from a Kaggle dataset and were very similar. These files had information for a large number of countries, each with records over a span of 2 and 20 years, littered with missing data and odd formatting. The first is on adult literacy (named adultliteracy.csv), where I reset the index to Country, dropped rows with no values, and removed columns that were not relevant. I then found the average percent literacy for that country before 2004, ignoring missing values. 

I took very similar steps with GDP, health expenditures, and sugar consumption. The table on dental health (number of tooth issues in children under 13) has information for 2004 only and is the year that I am making the comparison for, so all data past 2004 has been discarded for now. I have been looking for other possible variables to compare to and added water sanitation information also. This file was cleaned and many values needed to be converted to numeric values to fit with the other files.

Using .describe() for each file, I was able to check that there were no unexplained min or max values that could be outliers.

I then merged all the files on Country and ran a Spearman correlation method for a quick analysis. 
