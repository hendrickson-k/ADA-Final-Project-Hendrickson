The Relationship Between Health Insurance and Cholesterol Levels in Adults in the United States
By Katrina Hendrickson

This project is using data from NHANES (https://wwwn.cdc.gov/nchs/nhanes/continuousnhanes/default.aspx?Cycle=2021-2023) to analyse the relationship between insurance type and status and cholesterol levels.

Getting Started:
There are three options for the data to start with:
  1) The raw data as it is downloaded from NHANES - This is 3 files including DEMO_L.xpt HIQ_L.xpt and TCHOL_L.xpt
  2) The raw data combined - Raw data.xlsx
  3) The clean data - This is the raw data run through the cleaning code "FP Data Cleaning Hendrickson"

The variables in this project include:
  1) Cholesterol Level: The total cholesterol (mg/dL), listed as high if it was 240 or greater, and normal if it was below 240.
  2) Insurance type: Private, Public, or None. If a participant had both public and private it was marked as private. 
  3) Age: Categorized approximately by decade, with everyone 18-30 in one group and everyone 61 and older in one group.
  4) Sex: Male or Female.
  5) Race/Ethnicity: Mexican American, Non-Hispanic Asian, Black, and White, other Hispanic, and Other race - including multiracial.
  6) Income: Measured as a ratio of family income to the poverty level then categorized. 

Once the data is cleaned, analysis is run using "Final Project Code.Rmd" The analysis done is logistic regression, so the first step is testing the assumptions. The first assumption is linearity of age, using Box-Tidwell. This assumption is not met, so further analysis will be using age as a categorical variable. Next the models are run, comparing:
  1) Insurance (public, private, and none) to cholesterol level
  2) Insurance (public, private, and none) to cholesterol level adjusting for age, sex, race, and income
The models all find the VIF and Cook's Distances to ensure no multicolinearity and no influential observations. 

