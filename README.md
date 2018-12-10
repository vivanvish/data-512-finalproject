## Data 512: Final Project 
### Quantitative analysis of the rise in college tuition
Vishnu Nandakumar

### I. Introduction
This is the repository for my final project of DATA 512: Human Centered Data Science. For details on initial considerations and thought process please refer the `A3-FinalProjectPlan.ipynb`. Majority of the data used for the analysis is present in the data folder. Due to file size restrictions some files could not be provided here. The links to those datasets and instructions on how to use them will be given in **Data Sources** section. <br/>
The code and entire analysis description are provided in the `FinalProjectAnalysis.ipynb` folder. A bit of background and a brief discussion on some interesting results from the analysis will be discussed here.

### II. Analysis and Results
The analysis focussed on the increase in tuition costs for post secondary education in the US. The analysis was broken down into a process of finding the answers to three research questions. For details about the research questions and the process and also to explore the results please refer to the analyis in `FinalProjectAnalysis.ipynb`.

### III. Data Sources

The primary data source for institutional data such as income and expenditure, is the [Delta Cost Project Database](https://nces.ed.gov/ipeds/use-the-data/delta-cost-project-finance-data). It comes under the National Center for Education Statistics and is a part of the **Integrated Postsecondary Education Data System**. It is a comprehensive collection of data on institutional characteristics such as finance, enrollment, completions, graduation rates, student financial aid, and human resources from 1987 through 2012. It has a total of ** 215,613 observations and 974 variables**. For a more detailed description of the data please refer to the [data dictionary](https://nces.ed.gov/ipeds/deltacostproject/download/Delta_Data_Dictionary_1987_2012.xls). <br/>

Out of those 974 variables, these are some of the variables that got used were:
- academicyear          : Academic year the data was collected 
- unitid                : The unique identifier assigned to each univerity/institution
- instname              : Name of the institute
- state                 : The state in which the institute is located
- sector                : Whether the institute is public 4-year or 2-year, or private etc.
- tuition02_tf          : The average instate tuition.
- tuition03_tf          : The average out of state tuition
- loan_pct              : The percentage of students having student loans. 
- fall_total_undergrad  : Total fall undergrad enrollment 
- total_enrollment      : Total enrollment (includes graduates and part-time enrollment)
- cpi_scalar_2012       : CPI index to convert to 2012 dollars
- federal07             : Gross amount in Federal Aid
- tuition_reliance_a2   : Share of tuition in total revenue
- other05               : Revenue from hospitals and other independent services and sources.
- instruction01         : Gross expense related to instructional activities.
- research01            : Gross expense related to research activities
- nettuition_share      : Share of instructional expense covered by tuition.

Due to size restrictions the raw data files could not be uploaded to github. So I have uploaded it to a google drive and you can download the data from [here](https://drive.google.com/open?id=1ur9Ahh0NGru6L5HfCs3j7R4Cf4xJXPDa): <br/>
Please make sure that both files are downloaded and stored in the data folder.

The second source of data is Historical Median Household Income by State data from 2000-2017. It was downloaded from [here](https://www.census.gov/data-tools/demo/saipe/saipe.html?s_appName=saipe&map_yearSelector=2017&map_geoSelector=aa_c&s_USStOnly=y&menu=trends&s_measures=mhi_snc&s_inclStTot=y&s_inclUsTot=y). You can find the data in the `data` folder under the named as `household_income.csv`

The third file in `data` folder is the `state_name_code_mapping.csv`. It is a file I created manually to map the US State names with their Postal codes.

The analytical dataset used for fitting the Mixed Effects Linear Model is also available in the data folder, saved as `data_for_panel_reg.csv`.

### IV. Reproducibility

The analytic process will be carried out by keeping the notion of reproducibility in mind. To ensure maximum reproducibility, the code, the data used, external sources etc will be included with the final deliverable.
The code used for analysis is in Python 3 and also needs jupyter to be installed in your system. The following packages needs to be installed for the notebook to run.

- matplotlib
- numpy
- pandas
- seaborn
- sklearn
- statsmodels


### V. Data License
Both sources of data (IPDES' Delta Cost Database and Median Household Income data) are Federal Public Datasets are covered by [U.S. Public Domain License](http://www.usa.gov/publicdomain/label/1.0/). Their terms of use are defined in the [Federal Open Data Policy](https://project-open-data.cio.gov/policy-memo/#c-ensure-information-stewardship-through-the-use-of-open-licenses). For more information on federal open data licensing, please vist [here](https://project-open-data.cio.gov/open-licenses/). <br/>
The custom datasets stored here are released under [Creative Commons CCZero](http://opendefinition.org/licenses/cc-zero/).

### VI. Repository License
This repository and the code included are covered by [MIT License](LICENSE).

### VII. Contact
For any questions or feedback please contact me at vishnn@uw.edu
