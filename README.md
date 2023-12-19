Introduction

Tuberculosis is one of the largest pathological burdens worldwide and affects approximately 10.6 million people per year (Litvinjenko et al., 2023).
Though the communicable disease is cureable, treatment outcomes across the globe are varied, depending on a number of different factors (WHO,2023).
The aim of the code written is to take TB outcomes downloaded from WHO recorded from the past 13 years and make a dataset including the countries income status and GDP invested into Public Health (WHO,2023; World Bank,2023).
This way we can analyse whether these variables have a significant impact on TB outcomes and potentially could be used to predict how much money should be allocated to public health in order to increase treatment outcome.

Methods

The annotated code was written using Jupyter Notebook on Anaconda to create and run a file using Python 3.12.0.
The libraries that are needed to run the code are as follows:
- Pandas
- Seaborn
- Sklearn

The code calls for the import of these libraries using the command import <library> as ...

The code requires the download of 3 files that can be found in the SWBio git repository. The file names are as follows:

- TB_outcomes.csv (Downloaded from WHO,2023., as a dataframe of countries and their no. of TB cases and treatment outcomes since 2010)
- API_SH.XPD.CHEX.GD.ZS_DS2_en_csv_v2_6226442 (Downloaded from World Bank,2023., as a dataframe of countries and their health expendatures as % GDP per year)
- Metadate_Country_API_SH.XPD.CHEX.GD.ZS_DS2_en_csv_v2_6226442 (Downloaded from World Bank, 2023., as a dataframe of countries and their income group).

The downloaded files will need to be placed into the same directory as the notebook that contains the code for the code to run correctly.
If not, the relative paths in the read.csv function will return an error, in which the code will need to be edited to an absolute path to where you have downloaded the files.


Results

The data showed that TB treatment success rate was higher in lower income countries. This may be down to an increase in multi-drug resistant TB in higher income countries that increase the treatment failure rate (Falzon et al., 2015)
No correlation was found between GDP expendature and countries success rate, which can be down to confounding variables that may be at play that have not been considered in this investigation.
There was a positive linear relationship when we looked at the success rate regionally with average GDP expendature, however a linear regression model was unable to accurately predict success rate from GDP based on the data given.
This is potentially due to the lack of datapoints to calibrate the model (All countries are organised into only 6 regions, therefore the model has only 6 averages to work with).
Further data visualisation and interpretation can be found within the code.


Conclusions

To conclude, GDP and country income alone are not good indicators of TB outcome. GDP expendatures into public health is too broad as different countries may invest different amounts into different areas of public health.
As such, countries with higher TB burdens may invest more into the treatment, whilst higher income countries may have more cases of multidrug-resistance.
It is likely that a more accurate predictive model could be created if more variables were accounted for.

Bibliography

Falzon, D., Mirzayev, F., Wares,F., Baena, I., Zignol, M., Linh, N., Weyer, K., Jaramillo, E., Floyd, K., Raviglione, M. (2015). Multidrug-resistant tuberculosis around the world: what progress has been made? European Respiratory Journal, 45(1), 150-160.

Litvinjenko, S., Magwood, O., Wu, S., Wei, X. (2023). Burden of tuberculosis among vunerable populations worldwide: an overview of systematic reviews. The Lancet Infectious Diseases, 23(12), 1395-1407.

WHO(2023) Global Tuberculosis report 2023. Available at https://www.who.int/teams/global-tuberculosis-programme/tb-reports. [Last accessed: 19/12/23]

World Bank (2023). Current Health expendature (% of GDP). Available at https://data.worldbank.org/indicator/SH.XPD.CHEX.GD.ZS?end=2021&most_recent_value_desc=false&start=2000&view=chart. [Last accessed: 19/12/32]

