# Problem Statement

California is a large and diverse state with 58 counties greatly different geographically, and demographically. These counties also produce varying educational outcomes for its youth.

The goal of this study is to identify the counties that have the worst and best overall student performance on the SAT and ACT tests, to determine which counties are in most need of educational resources, and which ones can be scaled back. Furthermore, it seeks to identify county-level demographic indicators, which may be useful in predicting SAT and ACT participation rates and performance in the future. 

I took California county-level data retrieved from Cubit.com. Find out more about their sources and methodology [here.](https://demographics-by-cubit.helpscoutdocs.com/category/38-data-questions)
The county-level data was divided up into five sheets: 
Age, Income, Race, Education, and Household   
I combined these smaller .csv files in with my test data using the merge function; and county name as my key value. 

# Data Dictionary

|Feature|Type|Dataset|Description|
|---|---|---|---|
|**county_name**|*object*|sat_2019_ca.csv|Name of County|
|**twelfth_grade_enrollment_sat**|*integer*|sat_2019_ca.csv|Enrollment of Grade 12|
|**num_test_takers_sat**|*integer*|sat_2019_ca.csv|Number of Test Takers Grade 12|
|**prct_ewr_benchmark_sat**|*float*|sat_2019_ca.csv|The percent of students who met or exceeded the benchmark for Evidence-Based Reading & Writing (ERW) test for Grade 12.
|**prct_math_benchmark12_sat**|*float*|sat_2019_ca.csv|	The percent of students who met or exceeded the benchmark for SAT Math test for Grade 12.
|**prct_both_benchmark_sat**|*float*|sat_2019_ca.csv|The percent of students who met the benchmark of both Evidence-Based Reading & Writing (ERW) and Math Grade 12.|
|**twelfth_grade_enrollment**|*integer*|act_2019_ca.csv|Enrollment of Grade 12|
|**num_test_takers**|*integer*|act_2019.ca.csv|Number of Test Takers|
|**avg_english_score_act**|*integer*|act_2019.ca.csv|Average ACT English Score|
|**avg_reading_score_act**|*integer*|act_2019.ca.csv|Average ACT Reading Score|
|**avg_math_score_act**|*integer*|act_2019.ca.csv|Average ACT Math Score|
|**avg_science_score_act**|*integer*|act_2019.ca.csv|Average ACT Science Score|
|**pct_comp_score_21plus**|*float*|act_2019.ca.csv|Percent of Test Takers Whose ACT Composite Scores Are Greater or Equal to 21|

# Findings
#### Counties with lowest SAT participation:
1. Mono (.08)
2. Nevada (.09)
3. Tehama (.13)
4. Tuolumne (.15)
5. Inyo (.16)
#### Counties with highest SAT participation:
1. San Francisco (.51)
2. San Mateo (.43)
3. Los Angeles (.42)
4. Ventura (.42)
5. Riverside (.41)

#### Counties with lowest ACT participation:
1. Nevada (.04)
2. Tuolumne (.04)
3. Mono (.05)
4. Inyo (.05)
5. Yuba (.06)
#### Counties with highest ACT participation:
1. Modoc (.63)
2. Tehama (.44)
3. Marin (.28)
4. San Francisco (.24)
5. Contra Costa (.21)

#### Counties with lowest SAT composite scores:
1. Colusa (.19)
2. Glenn (.28)
3. Madera (.29)
4. Merced (.29)
5. Inyo (.32)
#### Counties with highest SAT composite scores:
1. El Dorado (.73)
2. Mariposa (.72)
3. Placer (.69)
4. Marin (.69)
5. Nevada (.69)

#### Counties with lowest ACT composite scores:
1. Modoc (.20)
2. Kings (.25)
3. San Bernardino (.29)
4. Merced (.30)
5. Madera (.33)
#### Counties with highest ACT composite scores:
1. Calaveras (.88)
2. Marin (.80)
3. Mono (.70)
4. Amador (.78)
5. Tuolumne (.78)

All the varibles within the score categories had very strong correlations to one another.  
There was a strong correlation beteen the number of test takers and number of enrolled students for obvious reasons. SAT participation rates had a moderate correlation with test-takers and enrollment. ACT participation rates have weak but noteworthy correlations with average English scores and composite benchmark clearance rates. 

#### Best demographic indicators for SAT particpation rates
1. Percent Pop. HH Income 50-79K (-.72)
2. Percent Pop. Asian (.68)
3. Percent Pop Female, Age 40-49 (.68)
4. Percent Pop Some College Education (-.68)
5. Median Value of Owner-Occupied Homes (.68)

#### Best demographic indicators for ACT particpation rates

1. Percent Pop. HH Income 50-79K (-.25)
2. Percent Pop Female, Age 40-49 (.25)
3. Percent Pop Some College Education (-.24)
4. Median Value of Owner-Occupied Homes (.20)
5. Population Density (.17)

#### Best demographic indicators for SAT performance rates

1. Percent Pop. No Diploma (-.83)
2. Percent Pop. Hispanic (-.73)
3. Percent Pop. Male Age 0-9 (-.67)
4. Percent Pop. Below Poverty Line (-.61)
5. Total Household Income (.57)

#### Best demographic indicators for ACT performance rates

1. Percent Pop. No Diploma (-.78)
2. Percent Pop. Hispanic (-.69)
3. Percent Pop. Below Poverty Line (-.73)
4. Percent Pop. Male Age 0-9 (-.65) 
5. Percent Pop HH Income 100-199K (.57)

# Recommendations

Nevada, Tuolumne, Mono,  and Inyo counties all appear in the top five lowest participating counties, for both tests.
Merced and Madera counties suffer from lower composite scores on both tests.
Based on what can be inferred from the strength of the correlation indicators, resources for participation should be focused on communities with lower median values of owner-occupied homes and less educational attainment. Resources for test performance should likewise be focused on younger communities with less educational attainment and larger Hispanic communities.
