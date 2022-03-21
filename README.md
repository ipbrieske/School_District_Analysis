# School_District_Analysis

## Overview

The goal of this project was to create useful dataframes from two separate csv files provided by the school district. The files documented all students across the district as well as information about each school within the district. We united these two data sets using Pandas in Python in order to determine class scores by grade, scores by school spending, scores by school size, and scores by school type. The data first had to be cleaned of any faculty, and we also faced the challenge of updating our dataset when we were informed of incorrect entries within our student data. 

## Results

After our initial analysis of all district data, we were tasked with ignoring the data provided by Thomas High School's 9th grade class, due to academic dishonesty. In order to do so, we leveraged Numpy's .nan function in order to omit the affected data points. This change in the data altered the final grade averages for Thomas High School significantly, though had a minor affect on the district data as a whole. 

![THS Before After](https://github.com/ipbrieske/School_District_Analysis/blob/main/Photos/THS_before_after.png)

Eliminating 9th grade scores for Thomas High School improved their overall percentage of students passing both reading and math by 25 percentage points. This was enough to move Thomas High School from what would have been the bottom of the rankings of schools by overall passing percentage to 2nd place. That is a significant improvement!

Replacing the 9th grade scores affected all of the following:

- Math and Reading scores by grade 

	- ![Scores by grade before](https://github.com/ipbrieske/School_District_Analysis/blob/main/Photos/scores_by_grade_before.png)
	- ![Scores by grade after](https://github.com/ipbrieske/School_District_Analysis/blob/main/Photos/scores_by_grade_after.png)
	- Included here is an improvement in the original code to leverage a for loop to assign formatting to the final scores. This saves us some variable assignments by avoiding creating a new unique variable for each grade's reading and math scores. Instead, we created a new dataframe and pulled relevant information from columns in that dataframe. We then leveraged a for loop in order to simplify the formatting process. 

- Scores by school spending

	- ![Spending before after](https://github.com/ipbrieske/School_District_Analysis/blob/main/Photos/spending_before_after.png)
	- Only the $630 to $644 category was affected, and only marginally. A difference of only 0.13 percentage points occurred between our original unclean and cleaned data. 

- Scores by school size
	
	-![Size before after](https://github.com/ipbrieske/School_District_Analysis/blob/main/Photos/size_before_after.png)
	- Scores by school size were similarly marginally affected.

- Scores by school type 
	
	-![School type before after](https://github.com/ipbrieske/School_District_Analysis/blob/main/Photos/type_before_after.png)


## Summary

Overall, omitting the unclean 9th grade data had a significant affect on Thomas High School's scores individually, but a very small difference on the district analysis as a whole. The number of affected students was two orders of magnitude smaller than our total student population, and did not change the final results by more than a single percentage point. We see a surprising inverse relationship between budget dollars per student and passing percentages, a difference in overall passing rates of 38 percentage points between district and charter schools in the favor of charter schools, and a negative correlation between class size and passing percentages. From this data, we can see that passing percentages are higher in schools with fewer students. Budgets are higher for schools with more students, but this doesn't necessarily translate into higher passing rates. Charter schools in this district also tend to have smaller class sizes, and may contribute to their clear success compared to district schools. Further analysis is necessary to determine exactly why this relationship exists. 