# School District Analysis

# Overview
- Maria asked me to draw up a detailed report of all of the schools in her district to be reviewed by the school board. I set up a pandas dataframe in python but before I could begin my analysis I cleaned up the data first. Many students used prefixes and suffixes, like "Mrs." or "PhD", that needed to be cleaned up first before the board was to view it. After the student's names were cleaned and the data was checked for empty values, I began analysis.
- I found the average class scores and passing percentages across the whole district and compiled it into the board's summary. I further broke down the district's performance by analyzing the scores in each school and comparing them with the type of school and the budget per student. 
- The school board was suspicious of 9th grade students cheating at Thomas High School and asked that I perform the same analysis again, but without the grades from the freshmen at Thomas High School.

## Results
1. District Summary Report:
- The district summary report before the ninth graders' grades from Thomas High School were omitted from the summary is shown here: 
  
![d-summary-before-omission](https://github.com/taherrin92/School_District_Analysis/blob/main/Resources/Before-Omission.png)


   - The district summary report after the omission only accounts for the tenth through twelfth graders from Thomas High School is shown here : ![d-summary-before-omission](https://github.com/taherrin92/School_District_Analysis/blob/main/Resources/After-Omission.png)
      - When the ninth-grade students from Thomas are omitted from the district summary, the average math scores go down by .1% and the average reading scores remain unchanged. The passing math percentage drops by .2%, the reading percentage drops by .3% and the overall passing percentage drops by .2%.

2. Per School Summary Report:
- The per school summary report before the ninth graders' grades from Thomas High School were omitted from the summary here: 


![ps-summary-before-omission](https://github.com/taherrin92/School_District_Analysis/blob/main/Resources/Per_school-Before-Omission.png)


  - The district summary report after the omission only accounts for the tenth through twelfth graders from Thomas High School is shown here: 

![Per_school-After-Omission](https://github.com/taherrin92/School_District_Analysis/blob/main/Resources/Per_school-After-Omission.png)


  - The changes between the summary after corrected to account only for upper-classmen shows a .06% drop in average math scores and a .5% rise in the average reading score. The percent of students passing math dropped .09% and the students passing reading dropped .3%. The overall percent passing dropped .3%.
  - Replacing the students scores did not have an impact on Thomas High School's overall performance compared to other schools, it still ranked second before and after the change.

3. Replacing the ninth-grade scores with NaN does not affect math and reading scores by grade, because the `ninth_grade.groupby(['school_name']).mean()['math_score']` code groups all of the ninth grade students by their school, and because all of the grades omitted were at Thomas High School, other school's grade averages and even the upper-classmen's grade averages are unchanged. 
- The reports posting scores by school size, spending and type show no change in average grades or percentages.

## Summary
1.  After changing the ninth graders' grades to NaN the percent averages for Thomas High School dropped down into the 60's. That is because the percent equations were dividing by zero. The correction to only include upper-classmen had to be made if the percent passing class were to be accurate.
2. The average math scores compared to the passing math % both declined after the scores were omitted. The average reading scores, however, rose by .04% but the passing reading percent dropped by .3%. The average math scores to percent passed appear normal after the change.
   - The rise in the average reading grade but the .3% drop in the passing reading percent is a red flag. If the average reading grade rose, but the percentage of students who passed reading dropped, then students cheating in their reading class is highly likely.
3. The overall change on the district summary appears small, but all of the average scores and percentages change as expected except for the reading values. The % of students passing reading drops by .3% but the average reading score remains unchanged. This would mean that the ninth graders pulled from the summary had the same average as everyone else, but caused the percent passing reading value to drop. 
   - If some Thomas High School freshmen were not cheating in reading, then the average grade when they were pulled would have rose, because the cheating outliers boost the average score by a noticeable margin.
4. Because the reports posting scores by school size, spending, and type were requested to be rounded to either one decimal place or no decimal, the incremental change that occured by replacing their grades with the upper-classmen was too small to have any effect on the report. The change is there if the formatting was adjusted to account for at least two decimal places.

(the PyCitySchools_Function.ipynb notebook used a function that defined and calculated math and reading scores by grade and another function that combined the series into the dataframes and formatted them at the same time. Cutting the lines of code in half)
