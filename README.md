## A3: Final Project Plan
Vishnu Nandakumar

### I. Introduction
This is a detailed overview of the final project of the course **Data 512: Human Centered Data Science**. 
My analysis intends to explore the reasons behind the significantly high tuition fees charged by Universities across the US. An article published last year ([link](https://www.cnbc.com/2017/11/29/how-much-college-tuition-has-increased-from-1988-to-2018.html)), highlighted this issue. Quoting the article:
```
Students at public four-year institutions paid an average of $3,190 in tuition for the 1987-1988 school year, with prices adjusted to reflect 2017 dollars. Thirty years later, that average has risen to $9,970 for the 2017-2018 school year. That's a 213 percent increase.
```
The trend is similar across both private and public Universities, with the former showing even steeper increase. One could argue that the high tuition has conributed to the quality and volume of research and infrastructure that are at the students disposal. But the problem with this arguement is that while we are observing a uniform rise in the tuition fees across all institutes, we do not know if the research quality and infrastructure improvements are also being improved. Some institutes have better funding and research opportunities than others.

Quoting this [article](https://www.forbes.com/sites/zackfriedman/2018/06/13/student-loan-debt-statistics-2018/#7f8b83d27310) from the Forbes: 
```
The average student in the Class of 2016 has $37,172 in student loan debt.
```
The data here ([link](https://fred.stlouisfed.org/graph/?id=SLOAS,#0)) from the Federal Reserve Economic Data shows that as of 2018, the total debt in student loans is **$1.53 trillion!**.  No other country in the world even comes close to this. 
Having a college degree significantly impacts a student's marketabilty in the industry. This is the major reason that motivates students to complete college and earn their degree. However the supply and demand varies across sectors. Computer Science majors will probably find more opportunities after graduation than an Arts major. However, the fees and expenditure incurred by the students will, more or less, be the same. This makes one wonder whether the fees should be determined by the ROI. But that's something I won't be pursuing this question in my analysis here.

### II. Research Questions

All of this motivated me to explore this issue further as the main topic of my project. The human centred aspect of this project is the subject around which the analysis arounds: **the students.** As a student, I too am interested in knowing how my fees are being utilized and how much of it is actually being spent on me. Hence part of my analysis I intend to explore the following three questions:
- How did the average tuition fees increase over the years?
- What are the factors that have contributed to the above increase?
- Where is the money going, i.e, are students receiving benefits that are proportional to the fees that they are charged? 

### III. Data Sources

The primary data source for institutional data such as income and expenditure, is obtained from the [Delta Cost Project Database](https://nces.ed.gov/ipeds/use-the-data/delta-cost-project-finance-data). It comes under the National Center for Education Statistics and is a part of the **Integrated Postsecondary Education Data System**. It is a comprehensive collection of data on institutional characteristics such as finance, 
enrollment, completions, graduation rates, student financial aid, and human resources from 1987 through 2012. It has a total of ** 215,613 observations and 974 variables**. For a more detailed description of the data please refer to the [data dictionary](https://nces.ed.gov/ipeds/deltacostproject/download/Delta_Data_Dictionary_1987_2012.xls).
Out of those 974 variables, these are some of the variables that will:
- academicyear
- instname
- state
- sector
- sector_revised
- iclevel
- control
- fte_count
- tuition01
- tuition02
- tuition03
- net_student_tuition
- federal03
- state03
- local03
- state_local_app
- federal07
- federal07_net_pell
- state06
- local06
- state_local_grant_contract
- federal10
- federal10_net_pell
- state09
- fed_state_loc_grants_con
- private03
- affiliate01
- investment01
- endowment03
- priv_invest_endow
- edactivity03
- auxiliary03
- hospital03
- other03
- other04
- independent03
- other05
- auxother_rev
- stable_operating_rev
- total03_revenue
- tot_rev_wo_auxother_sum
- tot_rev_w_auxother_sum
- unrestricted_revenue
- restricted_revenue
- tuition_reliance_a1
- tuition_reliance_b1
- tuition_reliance_c1
- tuition_reliance_a2
- tuition_reliance_b2
- tuition_reliance_c2
- govt_reliance_a
- govt_reliance_b
- govt_reliance_c

I will also use the Current Population Survey (CPS) census [data](https://www.census.gov/data/tables/time-series/demo/income-poverty/historical-income-households.html), for obtaining the values for median family income and unemployement related data. 
 
### III. Analysis Plan

The analysis will be presented in a jupyter notebook, one that starts with providing a birds eye view of the observed trends and gradually moves into exploring the factors and variables in much more detail. I have given below an initial draft of my analysis plan, which is subject to change as I explore the data in more detail.
- Explore the historical trend in average tuition fees.
- Correlate the trend with historical policy changes and interest rates.
- Break down and analyze the Universities' revenue stream.
- Mathematically model the tuition fee trend using the identified factors and observed how much of it its explained.
- Finally, examine the affordability of a college education by using the median household income data.

### IV. Reproducibility

The analytic process will be carried out by keeping the notion of reproducibility in mind. To ensure maximum reproducibility, the code, the data used, external sources etc will be included with the final deliverable.

### V. Data License
Both sources of data (IPDES' Delta Cost Database and CPS data) are Federal Public Datasets are covered by [U.S. Public Domain License](http://www.usa.gov/publicdomain/label/1.0/). Their terms of use are defined in the [Federal Open Data Policy](https://project-open-data.cio.gov/policy-memo/#c-ensure-information-stewardship-through-the-use-of-open-licenses). For more information on federal open data licensing, please vist [here](https://project-open-data.cio.gov/open-licenses/).

### VI. Repository License
This repository and the code included are covered by [MIT License](LICENSE).

### References
These are the list of resources I have utilized so far. Will update the list as project progesses.</br>
[1] Emmie Martin, 29th Nov 2017, Here’s how much more expensive it is for you to go to college than it was for your parents, https://www.cnbc.com/2017/11/29/how-much-college-tuition-has-increased-from-1988-to-2018.html</br>
[2] Zack Friedman, 13th Jun 2018, Student Loan Debt Statistics In 2018: A $1.5 Trillion Crisis, https://www.forbes.com/sites/zackfriedman/2018/06/13/student-loan-debt-statistics-2018/#3617c1cc7310</br>
[3] FRED, (https://fred.stlouisfed.org/graph/?id=SLOAS,#0</br>
[4] Grey Gordon, Aaron Hedlund, Accounting for the Rise in College Tuition, 2017</br>
[5] R. B. Archibald and D. H. Feldman.  Explaining increases in higher education costs.
The Journal of Higher Education, 2008
