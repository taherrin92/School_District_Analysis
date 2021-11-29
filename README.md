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
   - The per school summary report before the ninth graders' grades from Thomas High School were omitted from the summary is shown here:  
  
![ps-summary-before-omission](https://github.com/taherrin92/School_District_Analysis/blob/main/Resources/Per_school-Before-Omission.png)


   - The district summary report after the omission only accounts for the tenth through twelfth graders from Thomas High School is shown here : ![ps-summary-after-omission]((https://github.com/taherrin92/School_District_Analysis/blob/main/Resources/Per_school-After-Omission.png)
