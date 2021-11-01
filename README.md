#  Project 1: Standardized Test Analysis

![](https://i.imgur.com/6VmmNpM.jpg)

### Overview

College Spring is non-profit organization offering SAT/ACT prep services to private and charter schools in Southern California, San Francisco Bay, and in New York. Company executives have made the decision to offer services to public schools as well. According to its most recent annual report, the company provided preparatory training to 5,500 students, of which a total of 4,400 were located in California.  College Spring also reports increased college readiness for graduates of the program. Given these metrics, the next step in expanding services is determining the appropriate size for its first partner school district.

### Problem Statement

I have just been hired by College Spring and as such, my first assignment is to provide insight on the best course of action for expansion. Using previous participation and reported increase in college readiness, develop a strategy for expansion.

!["success scalar"](https://i.imgur.com/jSWPRgT.jpg)

Taken from College Spring ([*website*](https://collegespring.org/our-impact/))

### Data Dictionary

|Feature|Type|Dataset|Description|
|---|---|---|---|
|**sname**|*object*|SAT|School Name|
|**dname**|*object*|SAT|District Data|
|**numtsttakr12**|*integer*|SAT|Number of test takers in the 12th grade|
|**numtsttakr11**|*integer*|SAT|Number of test takers in the 11th grade|
|**pct_erw_bm_12**|*float*|SAT|Actual 12th-grade students who met the Evidence-Based Reading & Writing benchmark.|
|**pct_math_bm_12**|*float*|SAT|Actual 12th-grade students who met the Math benchmark.|
|**pct_erw_bm_11**|*float*|SAT|Actual 11th-grade students who met the Evidence-Based Reading & Writing benchmark.|
|**pct_math_bm_11**|*float*|SAT|Actual 11th-grade students who met the Math benchmark.|
|**imp_erw_bm_12**|*float*|SAT|Projected impact: 12th-grade students predicted to meet the Evidence-Based Reading & Writing benchmark. Calculated as percentage of 12th-grade students who met benchmark times College Spring success scalar.|
|**imp_math_bm_12**|*float*|SAT|Projected impact: 12th-grade students predicted to meet the Math benchmark. Calculated as percentage of 12th-grade students who met benchmark times College Spring success scalar.|
|**imp_erw_bm_11**|*float*|SAT|Projected impact: 11th-grade students predicted to meet the Evidence-Based Reading & Writing benchmark. Calculated as percentage of 11th-grade students who met benchmark times College Spring success scalar.|
|**imp_math_bm_11**|*float*|SAT|Projected impact: 11th-grade students predicted to meet the Math benchmark. Calculated as percentage of 11th-grade students who met benchmark times College Spring success scalar.|
|**tot_imp_erw_bm_12**|*integer*|SAT|Number of potential 12th-grade students who could meet SAT Evidence-Based Reading & Writing benchmark.|
|**tot_imp_math_bm_12**|*integer*|SAT|Number of potential 12th-grade students who could meet SAT Math benchmark.|
|**tot_imp_erw_bm_11**|*integer*|SAT|Number of potential 11th-grade students who could meet SAT Evidence-Based Reading & Writing benchmark.|
|**tot_imp_math_bm_11**|*integer*|SAT|Number of potential 11th-grade students who could meet SAT Math benchmark.|

Cleaned and transformed from:
* [`sat_2019_ca.csv`](./data/sat_2019_ca.csv): 2019 SAT Scores in California by School
* [`sat_2020_ca.csv`](./data/sat_2020_ca.csv): 2020 SAT Scores in California by School

### Analysis

In the interest of serving the students with the most immediate need for the program, I used the data on 11th grade students. This is because, typically, students take the test for the college application process in the fall of 12th grade.

First, I considered adopting the strategy of focusing on a singular school district. All things constant and the number of test takers in the next largest district after LAUSD would almost equal the last year's number of participants for all of Southern California. This also does not take into account the diminishing return of the program for schools have higher performance scores than the College Spring averages. The application of the performance scalar makes most sense, the closer to College Spring the schools perform.

Next, I considered the strategy of partnering with schools of similar performance profile. I filtered for just those schools then aggregated the total potential increases in students meeting. Assuming the resources required to service public schools are analogous to doing the same for private and charter schools, this approach is more managable. There is also the added benefit of working with multiple districts.

### Conclusion + Recommendation

In keeping with current company practice of spreading the company's reach, I recommend adopting the second strategy.
- Target schools of similar performance profile in multiple districts, with the intent of providing service to wider area.
- Focus on maximizing impact, given company resources and staffing. College Spring serves all students, but those that come from low-income backgrounds feel the effects of the program the most.
- Top priority is to replicate success in the public school environment.

### External Sources

([*Impact*](https://collegespring.org/our-impact/))

([*2018-2019 Annual Report*](https://collegespring.org/wp-content/uploads/2019/11/CollegeSpring_Annual_Report_November_2019.pdf))