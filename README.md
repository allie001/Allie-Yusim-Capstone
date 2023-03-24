# From Crayons to Diplomas: The Impact of State Preschool Programs on Mothers in Florida and Washington, DC
This repository includes the data, code, executive summary, and write up for my Capstone project. The study is an analysis of the impact of state preschool programs on maternal educational outcomes in DC and Florida.

**Abstract:** Access to affordable child care through programs like universal public preschool offers time to parents (and mothers in particular) who may otherwise stay home to care for their child. Using data from the American Community Survey (ACS), I explore whether mothers use this time to pursue further education. I use Florida and Washington, DC’s universal preschool programs as case studies. Regression discontinuity design allows me to take advantage of age eligibility cutoffs in both programs. I find little to no effect on all educational outcomes in Florida. In Washington, DC, I find that mothers whose youngest child was young enough to enroll in public preschool in 2009 had slightly higher educational attainment (around 1.4 years, statistically significant at a 10% singificance level) than mothers whose child was slightly too old to enroll. However, the results across all outcomes fluctuate, potentially due to limitations in the data.

**Accessing the data:**
The full ACS dataset is too large to upload, but is available through IPUMS. Follow this link: https://usa.ipums.org/usa-action/variables/group

On the IPUMS webstie, you can select any variable and sample. In my full dataset, I include the following variables (in addition to automatically selected variables): STATEICP, HHINCOME, YNGCH, SEX, AGE, MARST, RACE, EDUC, EDUCD. I download samples from the years 2005-2014.

This repository includes a cleaned dataset for Washington, DC ("clean_data_dc_moms.csv"). The cleaned Florida data is also too large to upload. You can access it through this link: https://drive.google.com/file/d/1LLLeF_V0hKAL0gHf8kQuSUJ5D3ptfFfR/view?usp=sharing

In my code, the cleaned data is called "dcmoms" and "floridamoms".

**Code and Analysis:**
The *Data Cleaning* file includes the code I use to clean the large ACS dataset. To prepare the data for my analysis, I created subgroups of moms in Florida and DC during the relevent years of analysis, converted the ACS' default EDUC and EDUCD variables into actual years of schooling, and created binary variables that indicated martial status, race, and whether an individual had a particular type of college degree.

In the *DC Analysis* file, I run several regression discontinuity models to explore the effect of DC's universal preschool program on mothers' educational attainment and their rates of college degrees. I include models for 2, 3, 4, and 5-years after the program's implementation for each outcome variable. The *Florida Analysis* file runs a similar analysis on Florida's preschool program. Both of the Analysis files run independently of the Data Cleaning file if using the cleaned data uploaded to this repository (DC) or to Google Drive (Florida). 

In the *DC Summary Stats* file, I calculate summary statistics for all moms in DC from 2009-2014, as well as specifically for the moms included in my regression discontinuity design. These include all of the outcome variables I measure in my analysis and important demographic statistics such as age, income, martial status, race. The *Florida Summary Stats* file calculates these statistics for all moms in Florida 2005-2010, as well as those included in the regression discontinuity bandwidth. I measure the same characteristics in Florida as I do in DC.
