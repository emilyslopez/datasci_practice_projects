# Predictive Modeling Project
### *Using predictive modeling on California Local Educational Agency (LEA) data to predict which locations are more likely to have school closures.* 
#### Goal: To demonstrate skills in data analysis, predictive modeling, and data visualization.
#### By: Emily Lopez-Lemus
#### Last Updated: May 23, 2024
*Refer to the end of [LEA_predictive_modeling.ipynb](https://github.com/emilyslopez/datasci_practice_projects/blob/main/predictive_modeling/LEA_predictive_modeling.ipynb) 
for additional details on project findings*

---
## Repo Contents
**LEA_predictive_modeling.ipynb:**
  - JupyterNotebook that contains project datasets, analysis, and observations 

**documentation:**
  - Folder with documenation for the datasets used in the project to understand the different variables and context

**outputs:**
  - Folder with the charts and graphs that were produced in my anaylsis

**presentations:**
  - Folder with the presentation and speaker notes I delivered to the Institutional Planning and Research Department at Mount Saint Mary's
    University in Los Angeles

---
## Project Overview

### Definitions:
- **Local Educational Agency (LEA):** An LEA is a local entity involved in education including but not limited to school districts, county offices of education, direct-funded charter schools, and special education local plan area (SELPA).
- **Title 1:** Federal education program that supports low income students throughout the nation. Funds are distributed to high poverty schools, as determined by the number of students who qualify for free or reduced lunch. https://www.cde.ca.gov/sp/sw/#:~:text=Helps%20disadvantaged%20students%20meet%20state,Student%20Succeeds%20Act%20(ESSA). 

### Purpose:
Through my experience with AmeriCorps Reading Partners Silicon Valley, I learned about the daily reality of teachers, 
students and staff at a California public school post-pandemic. I was happy to see similarities to my elementary school years,
but I was also very surprised to see the dramatic effect that COVID-19 had on school processes, staff retention,
and student outcomes. 

I served as the onsite Program Coordinator for our literacy program so I was able to work closely with volunteers, teachers, and staff. 
I learned that many students were far behind the reading level for their grade, there were serious shortages of teachers, and students frequently
enrolled and transferred schools due to school closures or family circumstances. I also learned that some teachers must teach 2 different
grade-levels in the same class due to lack of instructors. 

Reading Partners specifically functions at Title 1 elementary schools where most students' families experience financial hardship. Based on
the definition of a Title 1 school, most Title 1 schools are in districts that are located in neighborhoods with reported low incomes.
Since I first learned about school closures while working for this program, I was curious to see if there's a relationship between school
closures and districts that are in neighborhoods with historically low-reported incomes. I've attended title 1 schools K-12 in Whitter, CA,
so I felt a strong desire to understand the current circumstances regarding school closures and students' experiences.

Through predictive modeling, I would like to understand if a school's location is predictive of it being closed or open. These datasets from
the National Center for Education Statistics (NCES) on California Local Educational Agencies (LEA) could help me move towards this goal by
observing school closure trends at a state level and/or district level.

### Data Loading, Cleaning and Transformation

- **Dataset 1: LEA - Information on the Common Core of Data (CCD), Local Education Agency (School District) Universe Survey Data, (v.1a),
  nonfiscal year 2022-2023** 
    - The primary purpose of the CCD is to provide basic information on public elementary and secondary schools, local education agencies
      (LEAs), and state education agencies (SEAs) for each state, the District of Columbia, and the outlying territories with a U.S. relationship. 
    - Gives us the main information, like location, name and status. 
    - Will be our primary dataset.

- **Dataset 2: GEO - Public School District Geocode File for 2022-2023** 
    - The National Center for Education Statistics (NCES) Education Demographic and Geographic Estimates
(EDGE) program develops data resources and information to help data users investigate the social and
spatial context of education. 
    - Can tell us if LEA is located in suburban, town, rural, or city areas.
    - Will be our secondary dataset.

- **Primary Key: LEAID**
    - NCES Agency Identification Number is unique to each LEA and independent of state. This will be the key we join both tables on. 

- **Scope: Focus only on LEAs in California**
    - I reduced the scope to CA LEAs to understand the relationship between closures of LEAs and locations in CA. 

--- 

## Potential Applications of Findings:

Once this analysis and modeling is complete, the insights could: 
- inform decisions on what distrcits need additional funding, resources and support, like teaching staff, due to more closures in
   their area and help decision makers determine best course of action for distributing funds and resources
- help institutional analysts understand how neighboring LEAs within the same city compare to one another
- be compared to student assessment data/performance metrics and student and teacher satisfaction metrics to see what implications
   the school closures may have in the locations we identify
- help us identify what school distrcits will face the implications of these closures

Overall, these findings could help education decision makers and administrators determine which areas may experience more closures in
advance. This could inform strategic planning and interventions to faciliate closures which could minimize negative implications of these
transitions on students, educators and neighborhoods.

