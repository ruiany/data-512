# DATA 512 Final Project

## Abstract 
For the final project of the class, I studied food access in the United States by looking at the prevalence of food deserts and whom they affect the most, as well as the relationship between food access and physical health. I found out that on average, over 20% of the people in each state are affected by low food access and it can potential increase people's risk of becoming obese.

Please see [DATA-512-Final-Project.ipynb](https://github.com/ruiany/data-512/blob/main/data-512-final/DATA-512-Final-Project.ipynb) for the full report and code used in this project.

## Requirement
#### Programming language:
- Python version 3.0 and above

#### Packages:
- NumPy 1.11.1
- pandas 1.0.4
- matplotlib 1.5.3
- geopanda 0.7.0
- plotly 4.8.1
- notebook 6.0.3
- seaborn 0.11.0
- scipy 1.4.1

## Data
#### Raw
The datasets I used are the US food access data from the [Food Access Research Atlas](https://www.ers.usda.gov/data-products/food-access-research-atlas/) and the Nutrition, Physical Activity, and Obesity - Behavioral Risk Factor Surveillance System from the [Centers for Disease Control and Prevention (CDC)](https://chronicdata.cdc.gov/Nutrition-Physical-Activity-and-Obesity/Nutrition-Physical-Activity-and-Obesity-Behavioral/hn4x-zwk7). The Food Access Research Atlas dataset is released under a Creative Commons CC Zero License (cc-zero) and the CDC dataset is under a Public Domain license. Both datasets allow public use. 

The first dataset contains information on supermarket access at various distances depending on if the neighborhood is rural or urban. It also combines food access data with other fields such as age, race, and income. The second dataset contains data on adult's diet, physical activity, and weight status from Behavioral Risk Factor Surveillance System, which provides national and state specific data on obesity, nutrition, physical activity, and breastfeeding. I'm hoping to join the two datasets by geographic information and see if there's any correlation between food access and physical health measured by obesity rate. 
#### Final
The final cleaned data used for analysis and visualization can be found in [data/final](https://github.com/ruiany/data-512/tree/main/data-512-final/data/final)
The resulting food_access.csv and food_access_health_merge.csv file have the following schemas:

**food_access.csv**

Column | Format | Description |
|-----|------------|----|
State	| String | State name
County | String | County name
Urban	| Boolean | Flag for urban tract
lapop1	| Float | Population count beyond 1 mile from supermarket
lapop10	 | Float | Population count beyond 10 miles from supermarket
LAPOP1_10	| Float | Population count beyond 1 mile for urban areas or 10 miles for rural areas from supermarket
POP2010	| Float | Population count from 2010 census	
lalowi1	| Float | Low income population count beyond 1 mile from supermarket
lalowi10	| Float | Low income population count beyond 10 miles from supermarket
lakids1	| Float | Kids population count beyond 1 mile from supermarket
lakids10 | Float | Kids population count beyond 10 miles from supermarket
laseniors1	| Float | Seniors population count beyond 1 mile from supermarket
laseniors10	| Float | Seniors population count beyond 10 miles from supermarket
lawhite1	| Float | White population count beyond 1 mile from supermarket
lawhite10	| Float | White population count beyond 10 miles from supermarket
lablack1	| Float | Black or African American population count beyond 1 mile from supermarket
lablack10	| Float | Black or African American population count beyond 10 miles from supermarket
laasian1	| Float | Asian population count beyond 1 mile from supermarket
laasian10	| Float | Asian population count beyond 10 miles from supermarket
lahisp1	| Float | Hispanic or Latino ethnicity population count beyond 1 mile from supermarket
lahisp10	| Float | Hispanic or Latino ethnicity population count beyond 10 miles from supermarket
TractLOWI	| Float | Total count of low-income population in tract 
TractKids	| Float | Total count of children age 0-17 in tract 
TractSeniors	| Float | Total count of seniors age 65+ in tract 
TractWhite	| Float | Total count of White population in tract 
TractBlack	| Float | Total count of Black or African American population in tract 
TractAsian	| Float | Total count of Asian population in tract 
TractHispanic	| Float | Total count of Hispanic or Latino population in tract 
la1_ratio	| Float | Ratio of population beyond 1 mile from supermarket
la10_ratio	| Float | Ratio of population beyond 10 miles from supermarket
la_ratio	| Float | Ratio of population beyond 1 mile and 10 miles from supermarket
la_percentage	| Float | Percentage of population beyond 1 mile and 10 miles from supermarket
pop_ratio_poverty	| Float | Ratio of population living with income at or below the Federal poverty thresholds for family size
pop_ratio_kid	| Float | Population ratio of children age 0-17 
pop_ratio_senior	| Float | Population ratio of seniors age 65+
pop_ratio_white	| Float | Population ratio of White people
pop_ratio_black	| Float | Population ratio of Black or African American people
pop_ratio_asian	| Float | Population ratio of Asian people
pop_ratio_hisp	| Float | Population ratio of Hispanic or Latino people
la_ratio_poverty	| Float | Low food access ratio of population living with income at or below the Federal poverty thresholds for family size
la_ratio_kid	| Float | Low food access ratio of children age 0-17
la_ratio_senior	| Float | Low food access ratio of seniors age 65+
la_ratio_white	| Float | Low food access ratio of White people
la_ratio_black	| Float | Low food access ratio of Black or African American people
la_ratio_asian	| Float | Low food access ratio of Asian people
la_ratio_hisp	| Float | Low food access ratio of Hispanic or Latino people
PovertyRate	| Float | Share of the tract population living with income at or below the Federal poverty thresholds for family size
MedianFamilyIncome | Float | Tract median family income

**food_access_health_merge.csv**

Column | Format | Description |
|-----|------------|----|
index | Int | The unique census tract identifier |
GeoLocation | Object | Lattitude and longitude of the state |
LocationAbbr| String | State abbreviation |
LocationDesc | String | State full name |
Question | String| Health survey question |
Data_Value | Float | The percentage of people who answer 'yes' to the survery question |
State | String | State name | 
la_ratio | Float | The percentage of people who suffer from low food access |

## Conclusions
#### Food desert is especially severe in the midwest and the west of the US.
<img src="./plots/food_access_map.png" width="600">
<img src="./plots/food_access_by_state.png" width="1000">

#### Low income people were more susceptible to low food access in rural areas.
<img src="./plots/food_access_vs_income.png" width="1100">

#### No detectable bias for food access between different races, though the race ratio in the dataset was biased.
<img src="./plots/food_access_race.png" width="900">

#### There is a weak correlation between people who live food deserts and people who are overweight.
<img src="./plots/food_access_vs_health.png" width="1000">

## License

The MIT License is a permissive free software license originating at the Massachusetts Institute of Technology (MIT). As a permissive license, it puts only very limited restriction on reuse and has therefore an excellent license compatibility. For detailed description of the contents of license please refer to the file [License](https://github.com/ruiany/data-512/blob/main/data-512-final/LICENSE).


