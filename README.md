# Projects

#### Table of Contents ####
- [Project 1: Exploratory Data Analysis Using AWS Services](#Project-1-Exploratory-Data-Analysis-Using-AWS-Services)
- [Project 2: Descriptive Analysis Using AWS Services](#Project-2-Descriptive-Analysis-Using-AWS-Services)
- [Project 3: Diagnostic Analysis Using AWS Services](#Project-3-Diagnostic-Analysis-Using-AWS-Services)
- [Project 4: Data Wrangling for University Enrollment Analysis Using AWS Services](#Project-4-Data-Wrangling-for-University-Enrollment-Analysis-Using-AWS-Services)
- [Project 5: City of Vancouver Building Permits Analysis](#Project-5-City-of-Vancouver-Building-Permits-Analysis)

--- 

## [Project 1: Exploratory Data Analysis Using AWS Services](https://www.google.com)

### Project Title: Enrollment and Withdrawal Trends Analysis at University Canada West Using AWS

![Data Exploration Steps](https://github.com/vishakagupta18/Data-Analyst-Portfolio/blob/455663b84ecfec67c5f3ba6bb3a5dce3bbd4b27f/images/DataExplorationUCW.png)

#### Table of Contents ####

- [Project Description](#project-description)
- [Dataset](#dataset)
- [Objective](#objective)
- [Methodology](#methodology)
- [Tools and Technologies](#tools-and-technologies)
- [Deliverables](#deliverables)

#### Project Description: ####
This project aims to perform an exploratory data analysis (EDA) of the University's Enrollment and Withdrawal dataset using AWS services to uncover insights related to student enrollment patterns, program distribution, and retention rates. By leveraging AWS tools such as S3, AWS Glue, and Athena, we explore trends based on features like gender, academic programs, and enrollment status. This project demonstrates how cloud-based services streamline large-scale data analysis and visualization.

#### Dataset:
The dataset contains student information from the University of Canada West (UCW), with details such as:
- **StudentID**: Unique identifier for each student.
- **FirstName**: First name of the student.
- **LastName**: Last name of the student.
- **DateOfBirth**: Date of birth of the student.
- **Gender**: Gender of the student.
- **Program**: The academic program in which the student is enrolled.
- **EnrollmentDate**: The date when the student enrolled.
- **ExpectedGraduationDate**: The expected graduation date for the student.
- **Status**: Enrollment status (Enrolled, Graduated).
- **Email**: Contact email of the student.

#### Objective:
The objective is to analyze student enrollment and withdrawal patterns using AWS services, gaining insights into student demographics, program distribution, and factors influencing graduation and retention rates.

#### Methodology:

1. **Data Collection and Preparation**:
   - **Data Storage**: Upload the dataset to an Amazon S3 bucket for secure and scalable storage.
   - **Data Cleaning and Transformation**:
     - Use **AWS Glue** to create an ETL pipeline to clean the dataset, handle missing values, and format date columns (`DateOfBirth`, `EnrollmentDate`, `ExpectedGraduationDate`) for analysis.
     - Convert the data into a queryable format (e.g., Parquet) for optimized performance.
   - **AWS Glue Catalog**: Create a data catalog to manage metadata and make data easily discoverable for querying.

2. **Descriptive Statistics**:
   - Use **AWS Athena** to run SQL queries on the dataset stored in S3, generating summary statistics:
     - Calculate the average age of students based on `DateOfBirth`.
     - Count students per program and per enrollment status (Enrolled, Graduated).
     - Calculate the distribution of enrollment dates to observe academic cycles.

3. **Data Visualization**:
   - **Amazon QuickSight** for interactive data visualization:
     - **Bar Charts**: Display student counts across programs like MBA, MA, BA, and BCom, and visualize the enrollment status breakdown (Enrolled vs. Graduated).
     - **Pie Charts**: Visualize the gender distribution of students.
     - **Line Charts**: Plot enrollment trends over time, showing how many students enrolled in each semester.
     - **Stacked Bar Charts**: Explore program-wise gender distribution and their corresponding enrollment status to determine retention trends.

4. **Enrollment and Graduation Trends Analysis**:
   - Use **Athena** to compare enrollment and graduation rates across programs and genders:
     - **Program Trends**: Identify which programs (MBA, MA, BA) show higher graduation rates.
     - **Gender Analysis**: Analyze whether male or female students tend to graduate at higher rates.
     - **Year-over-Year Analysis**: Track how enrollment has changed over time, identifying any trends or anomalies.

5. **Insights and Findings**:
   - Summarize key insights based on the data exploration:
     - **Program-specific Analysis**: MBA and Leadership programs show high enrollment, while some programs may have lower graduation rates.
     - **Gender-based Patterns**: Gender distribution may show differences in enrollment trends.
     - **Enrollment Growth**: Year-over-year enrollment analysis may highlight academic cycles and potential areas for university outreach.

6. **Conclusion**:
   - Discuss actionable insights, such as identifying programs with low retention and suggesting strategies for improvement.
   - Highlight how AWS services streamlined the data pipeline, from storage to analysis and visualization.
   - Future analysis could include predictive modeling using **AWS SageMaker** to predict student retention based on historical trends.

#### Tools and Technologies:
- **AWS S3** for data storage.
- **AWS Glue** for data cleaning, transformation, and cataloging.
- **AWS Athena** for SQL-based querying and analysis.
- **Amazon QuickSight** for creating interactive dashboards and data visualizations.

#### Deliverables:
- A comprehensive AWS Glue ETL pipeline documented in a Jupyter Notebook or **Glue Job** code.
- SQL queries used in **AWS Athena** to analyze the dataset.
- A presentation summarizing the insights and findings for university stakeholders or peers.


## [Project 2: Descriptive Analysis Using AWS Services](https://www.google.com)

### Project Title: Descriptive Analysis of City of Vancouver Issued Building Permits in the Downtown Region (2023-2024) Using AWS

![Data Exploration Steps](https://github.com/vishakagupta18/Data-Analyst-Portfolio/blob/455663b84ecfec67c5f3ba6bb3a5dce3bbd4b27f/images/DataExplorationUCW.png)

#### Table of Contents ####

- [Project Overview](#project-overview)
- [Key Features of the Dataset](#Key-Features-of-the-Dataset)
- [Objective](#objective)
- [AWS Architecture](#AWS-Architecture)
- [Insights & Findings](#Insights-&-Findings)
- [Tools and Technologies](#tools-and-technologies)
- [Deliverables](#deliverables)

#### Project Overview:
This project focuses on analyzing building permits issued in Vancouver's downtown region during the years 2023 and 2024. The goal is to gain insights into the types of construction projects, timelines for permit issuance, project values, and trends influencing urban development in the city. The project leverages AWS services such as S3 for data storage, Glue for ETL processes, Athena for querying, and QuickSight for data visualization.

#### Key Features of the Dataset:
- **PermitNumber**: Unique identifier for each building permit.
- **PermitNumberCreatedDate**: Date the permit number was generated.
- **IssueDate**: Date the permit was officially issued.
- **PermitElapsedDays**: Time (in days) between permit creation and issuance.
- **ProjectValue**: Monetary value of the construction project.
- **TypeOfWork**: Type of construction work (e.g., Addition, Alteration, New Construction).
- **Address**: Location of the construction site.
- **ProjectDescription**: Detailed description of the construction project.
- **PermitCategory**: Category of the building permit.
- **Applicant**: Individual or entity applying for the permit.
- **ApplicantAddress**: Address of the permit applicant.
- **PropertyUse**: Intended use of the property (e.g., Dwelling, Retail).
- **SpecificUseCategory**: Detailed property use category.
- **BuildingContractor**: Contractor responsible for the construction project.
- **IssueYear**: Year the permit was issued.
- **GeoLocalArea**: Geographical area within Vancouver.
- **YearMonth**: Year and month of permit issuance.
- **geo_point_2d**: Geospatial coordinates for mapping.

#### AWS Architecture:
##### 1. **Data Ingestion:**
- The dataset is ingested into **Amazon S3** in CSV format for secure and scalable storage.

##### 2. **Data Cleaning and Transformation:**
- **AWS Glue** is used to clean, transform, and categorize the data. Key transformations include:
  - Parsing date fields for better date-related analysis.
  - Calculating project timelines (permit elapsed days).
  - Categorizing the types of construction work, property use, and contractor activities.

##### 3. **Data Querying:**
- **Amazon Athena** is used to query the processed data. The following insights are derived through SQL queries:
  - Average project value categorized by property use type.
  - Analysis of permit processing time trends over time.
  - Identification of the most common types of construction work in Vancouver's downtown area.
  - Geographic distribution of high-value construction projects.

##### 4. **Data Visualization:**
- **AWS QuickSight** is employed to create interactive visualizations that help uncover trends and insights:
  - **Project Values Over Time**: A time series analysis showing fluctuations in project values across months and years.
  - **Geographic Heatmaps**: Displaying permit concentrations and high-value projects across different downtown neighborhoods.
  - **Permit Processing Times**: Visualizing permit approval timelines, revealing bottlenecks and efficiency trends in the process.

#### Insights & Findings:
- **Permit Trends**: Insights into the average time to issue permits, the types of work commonly requested, and the geographic areas with the most activity.
- **High-Value Projects**: Key findings around the distribution of high-value construction projects and their locations.
- **Construction Trends**: Understanding of the types of work that dominate downtown construction (e.g., additions, alterations).

#### Tools and Technologies:
- **Amazon S3**: For scalable data storage.
- **AWS Glue**: For ETL processes (data cleaning, transformation, and categorization).
- **Amazon Athena**: For querying structured datasets.
- **AWS QuickSight**: For creating interactive dashboards and visualizations.

#### Deliverables:
- A detailed **report** summarizing insights, findings, and construction trends.
- **Visualizations** in AWS QuickSight showcasing key project trends and metrics.
- A **presentation** for stakeholders with visual dashboards to guide city planning and development strategy.

## [Project 3: Diagnostic Analysis Using AWS Services](https://www.google.com)

### Project Title: Diagnostic Analysis of City of Vancouver Issued Building Permits in the Downtown Region (2023-2024) Using AWS

![Diagnostic Analysis Steps](https://github.com/vishakagupta18/Data-Analyst-Portfolio/blob/455663b84ecfec67c5f3ba6bb3a5dce3bbd4b27f/images/DataExplorationUCW.png)

#### Table of Contents ####

- [Project Overview](#project-overview)
- [Objective](#objective)
- [Dataset Key Features](#Dataset-Key-Features)
- [AWS Architecture](#AWS-Architecture)
- [Project Insights & Findings](#Project-Insights-&-Findings)
- [Challenges and Solutions](#Challenges-and-Solutions)
- [Tools and Technologies](#tools-and-technologies)
- [Deliverables](#deliverables)
- [Timeline](#Timeline)

#### Project Overview:
This project focuses on the diagnostic analysis of building permits issued in the downtown region of Vancouver during 2023 and 2024. The objective is to uncover insights into the types of work being performed, permit timelines, project values, and other key factors affecting construction trends in the city. The analysis is powered by AWS services like S3 for data storage, Glue for data cleaning and transformation, Athena for querying, and QuickSight for visualization.

#### Objective:
The primary goal of this project is to conduct a diagnostic analysis of building permits issued in the downtown region of Vancouver during 2023-2024. By analyzing various data points, including project values, permit processing timelines, types of construction work, and geographic distribution, we aim to uncover key trends and factors influencing construction activity. This analysis will provide actionable insights for urban planners and city officials to optimize permit processing, identify high-value projects, and support data-driven decisions for future urban development and planning in Vancouver.

#### Dataset Key Features:
- **PermitNumber:** Unique identifier for each building permit.
- **PermitNumberCreatedDate:** Date the permit number was created.
- **IssueDate:** Date the permit was issued.
- **PermitElapsedDays:** Days between permit creation and issuance.
- **ProjectValue:** Value of the project covered by the permit.
- **TypeOfWork:** Type of construction work (e.g., Addition, Alteration).
- **Address:** Location of the building.
- **ProjectDescription:** Detailed description of the construction work.
- **PermitCategory:** Category of the permit.
- **Applicant:** Individual/entity applying for the permit.
- **ApplicantAddress:** Address of the applicant.
- **PropertyUse:** Intended use of the property (e.g., Dwelling, Retail, Office).
- **SpecificUseCategory:** A more specific use category within PropertyUse.
- **BuildingContractor:** Contractor responsible for the project.
- **IssueYear:** Year the permit was issued.
- **GeoLocalArea:** Geographic area within the city.
- **YearMonth:** Year and month of permit issuance.
- **geo_point_2d:** Geospatial coordinates for mapping.

#### AWS Architecture:

1. **Data Ingestion:**
   - Building permits data is stored in Amazon S3 in CSV format.

2. **Data Cleaning and Transformation:**
   - AWS Glue is utilized to clean and transform the dataset. The transformations involve:
     - Parsing date fields.
     - Calculating additional metrics, such as project timelines.
     - Categorizing data to streamline analysis.

3. **Data Querying:**
   - Amazon Athena is used to query the dataset, generating key insights:
     - **Average project value** by property use type.
     - **Permit processing time trends** across the years.
     - **Most common types of work** in the downtown area.
     - **Geographic distribution** of high-value projects.

4. **Visualization:**
   - **AWS QuickSight** is used to create interactive dashboards for visualizing:
     - **Project values** by month and year.
     - **Geographic heatmaps** showing concentration of permits.
     - **Time series analysis** for permit processing times.

#### Project Insights and Trends:
- **Permit Processing Efficiency:**
  - Identified average permit processing times based on project types, uncovering potential delays in certain work categories.
  
- **Geospatial Trends:**
  - Heatmaps reveal high concentrations of large-scale projects in certain geographic areas within downtown Vancouver.

- **Financial Trends:**
  - Analysis of **ProjectValue** shows trends in construction spending, with spikes during specific months, often corresponding to infrastructure-related projects.

#### Challenges and Solutions:
- **Data Consistency Issues:** 
  - Variability in data entry (e.g., inconsistent date formats) was resolved through comprehensive data cleaning using AWS Glue.

- **Geospatial Data Visualization:**
  - Mapping permit locations required transforming and standardizing geospatial coordinates to ensure accurate plotting in QuickSight.

#### Tools and Technologies:
- **AWS S3**: For secure storage of the building permits dataset.
- **AWS Glue**: To perform ETL operations, including cleaning and transforming the data.
- **Amazon Athena**: For querying the dataset and generating insights.
- **AWS QuickSight**: To visualize trends and insights through dashboards.

#### Deliverables:
- **Comprehensive Data Analysis Report**: Summarizes findings, key metrics, and trends identified in the analysis.
- **Interactive Dashboards**: Includes visualizations of project values, geographic trends, and permit timelines.
- **Recommendations**: Actionable insights for the City of Vancouver on optimizing permit processing and identifying high-value construction trends.

#### Timeline:
- **Expected completion**: 6 weeks.
- Regular check-ins and status reports will be provided to ensure alignment with stakeholders' objectives and to address any emerging challenges.


## [Project 4: Data Wrangling for University Enrollment Analysis Using AWS Services](https://www.google.com)

### Project Title: Diagnostic Analysis of City of Vancouver Issued Building Permits in the Downtown Region (2023-2024) Using AWS

![Data Wrangling Steps](https://github.com/vishakagupta18/Data-Analyst-Portfolio/blob/455663b84ecfec67c5f3ba6bb3a5dce3bbd4b27f/images/DataExplorationUCW.png)

#### Table of Contents ####

- [Project Overview](#project-overview)
- [Objective](#objective)
- [Dataset Key Features](#Dataset-Key-Features)
- [AWS Architecture](#AWS-Architecture)
- [Project Insights & Findings](#Project-Insights-&-Findings)
- [Challenges and Solutions](#Challenges-and-Solutions)
- [Tools and Technologies](#tools-and-technologies)
- [Deliverables](#deliverables)
- [Timeline](#Timeline)

#### **Project Overview:**
This project involves performing data wrangling on a dataset of student enrollments at the University. The goal is to clean, transform, and consolidate the student data for enhanced analysis and reporting. The analysis uses AWS services such as S3 for data storage, Glue for ETL, and Athena for querying the data. The wrangled dataset will be used to gain insights into student enrollment trends, graduation timelines, and program distribution, aiding the university in decision-making processes.

#### Objective:
The primary objective of this project is to perform comprehensive data wrangling on the university’s enrollment dataset. By cleaning and transforming the data, the goal is to improve its usability and accuracy, enabling further descriptive analysis of enrollment patterns, graduation rates, and student demographics.

#### Dataset Key Features:
- **StudentID:** Unique identifier for each student.
- **FirstName, LastName:** Names of the students.
- **DateOfBirth:** Birthdate of the students.
- **Gender:** Gender of the students.
- **Program:** The academic program in which the student is enrolled.
- **EnrollmentDate:** Date of student enrollment.
- **ExpectedGraduationDate:** The anticipated graduation date.
- **Status:** Current enrollment status (Enrolled or Graduated).
- **Email:** Contact email of the students.

#### AWS Architecture:

##### Data Ingestion:
- The student enrollment data is ingested into **Amazon S3** in CSV format for storage.

##### Data Cleaning and Transformation:
- **AWS Glue** is used to clean and transform the data:
    - Parse date fields such as `DateOfBirth`, `EnrollmentDate`, and `ExpectedGraduationDate`.
    - Standardize gender entries (e.g., "M/F").
    - Calculate additional metrics like the number of days from enrollment to expected graduation.
    - Address missing data (if any) and normalize categorical variables like `Status` (e.g., "Enrolled", "Graduated").

##### Data Querying:
- **Amazon Athena** is utilized for querying the cleaned dataset. Some of the queries include:
    - Distribution of students across different programs.
    - Graduation timelines and trends based on the `ExpectedGraduationDate`.
    - Breakdown of enrollment status by program and year.

##### Data Visualization:
- **AWS QuickSight** is used to visualize:
    - Enrollment trends by year and program.
    - Gender distribution across different academic programs.
    - Average time to graduation per program.
    - Dashboard visualizations for tracking student enrollment and graduation rates over time.

#### Methodology:

1. **Data Collection:**
   - The student enrollment dataset is ingested into S3 in CSV format.

2. **Data Assessment:**
   - Conduct an initial assessment of the dataset to identify issues such as missing values, duplicate records, and format inconsistencies.
   - Document data types and assess any discrepancies across key fields like `Status` and `Program`.

3. **Data Cleaning:**
   - Address any missing values or data inconsistencies.
   - Remove duplicate records if present.
   - Standardize categorical variables such as `Gender` and `Status`.
   - Ensure consistency in date formats.

4. **Data Transformation:**
   - Convert string fields into appropriate data types (e.g., convert date strings to `datetime` objects).
   - Calculate new features such as `EnrollmentDuration` (time between `EnrollmentDate` and `ExpectedGraduationDate`).
   - Perform data aggregations, such as counting the number of students by program or calculating the average graduation time.

5. **Data Consolidation:**
   - Consolidate all relevant information into a unified dataset for further analysis.
   - Ensure that key identifiers such as `StudentID` are consistently used for accurate linkage across records.

6. **Validation:**
   - Conduct exploratory data analysis (EDA) to validate the accuracy and completeness of the wrangled dataset.
   - Perform checks on the cleaned dataset for consistency across fields like `Gender`, `Program`, and `Status`.

#### Tools and Technologies:
- **AWS S3**: For data storage and retrieval.
- **AWS Glue**: For data cleaning, transformation, and ETL operations.
- **Amazon Athena**: For querying the dataset.
- **AWS QuickSight**: For creating interactive dashboards and visualizations.
- **Python (Pandas, NumPy)**: For additional data wrangling and validation tasks.
- **Jupyter Notebook**: For documenting and running Python scripts.

#### Deliverables:
- **Cleaned Dataset**: A well-structured dataset in CSV format that has been cleaned and transformed for further analysis.
- **Data Wrangling Report**: Documentation of the data wrangling process, including methods used to clean and transform the dataset, challenges encountered, and data validation results.
- **Visualizations**: Interactive dashboards built in AWS QuickSight that highlight key insights such as enrollment trends, gender distribution, and time-to-graduation.

#### Timeline:
- **Data Wrangling and Transformation**: 2 weeks
- **Data Querying and Analysis**: 1 week
- **Dashboard Creation in AWS QuickSight**: 1 week
- **Final Report Preparation and Deliverables**: 1 week

This data wrangling project ensures the preparation of a high-quality dataset that enables the university to conduct detailed analysis of enrollment patterns, helping improve student retention strategies, optimize academic offerings, and enhance overall operational efficiency.

## [Project 5: City of Vancouver Building Permits Analysis](https://www.google.com)

### Project Title: Data Quality Control Analysis of Vancouver Downtown Building Permits Using AWS Services

![Data Quality Control Steps](https://github.com/vishakagupta18/Data-Analyst-Portfolio/blob/455663b84ecfec67c5f3ba6bb3a5dce3bbd4b27f/images/DataExplorationUCW.png)

#### Table of Contents ####

- [Project Overview](#project-overview)
- [Objective](#objective)
- [Dataset Key Features](#Dataset-Key-Features)
- [AWS Architecture](#AWS-Architecture)
- [Project Insights & Findings](#Project-Insights-&-Findings)
- [Challenges and Solutions](#Challenges-and-Solutions)
- [Tools and Technologies](#tools-and-technologies)
- [Deliverables](#deliverables)
- [Timeline](#Timeline)

#### Project Overview:
This project involves analyzing building permits issued in Vancouver's downtown region between 2023 and 2024. The dataset contains details such as project value, type of work, contractor information, permit processing time, and geographic coordinates. The aim is to derive insights to inform urban development strategies and improve permit processing efficiency.

#### Objectives:
- Perform ETL (Extract, Transform, Load) on the dataset using AWS services.
- Visualize trends and patterns related to building permits (e.g., project types, values, timelines).
- Analyze geographic data to understand the distribution of permit types across downtown Vancouver.

#### Tools and Technologies:
- **AWS S3**: Store raw and processed data.
- **AWS Glue**: ETL pipeline for data extraction and transformation.
- **AWS Athena**: Query transformed data.
- **AWS QuickSight**: Visualize the data.
- **Tableau/Power BI**: Additional visualization options.
- **Python (pandas, geopandas)**: Analyze and clean the dataset.
- **GitHub**: Store and present the project code.

#### 1. Data Ingestion:
- **City of Vancouver Open Data Catalogue.**
- Dataset uploaded to AWS S3 in CSV format.

##### Dataset Fields:
- `PermitNumber`: Unique identifier for each permit.
- `PermitNumberCreatedDate`: Date the permit number was created.
- `IssueDate`: Date the permit was issued.
- `PermitElapsedDays`: Time between creation and issuance.
- `ProjectValue`: Value of the project in CAD.
- `TypeOfWork`: Type of construction or alteration work.
- `Address`: Project location.
- `ProjectDescription`: Detailed description of the project.
- `PermitCategory`: Classification (e.g., Residential, Commercial).
- `Applicant`: Name of the permit applicant.
- `ApplicantAddress`: Address of the applicant.
- `PropertyUse`: Usage type of the property (e.g., Dwelling, Commercial).
- `SpecificUseCategory`: Specific use type (e.g., Retail Store, Restaurant).
- `BuildingContractor`: Name of the contractor.
- `BuildingContractorAddress`: Contractor's address.
- `IssueYear`: Year the permit was issued.
- `GeoLocalArea`: Geographical area of the project within Vancouver.
- `Geom`: Geographic coordinates of the building (lat-long).
- `YearMonth`: Year and month of permit issuance.
- `geo_point_2d`: Latitude and longitude in plain text.

#### 2. Data Transformation (ETL):
##### AWS Glue ETL Pipeline:
- **Extract**: Load the dataset from AWS S3.
- **Transform**:
  - Clean missing or erroneous values.
  - Convert geographic data into usable formats for spatial analysis using `geopandas`.
  - Calculate additional fields such as `Permit Processing Time` (from `PermitElapsedDays`).
- **Load**: Store the transformed dataset back into AWS S3 for analysis.

#### 3. Data Analysis:
Queries in AWS Athena were designed to explore different dimensions of the dataset, such as:
- **Average Permit Processing Time** by type of work.
- **Top 10 Most Expensive Projects**.
- **Distribution of Permit Categories** (e.g., Commercial, Residential).
- **Geographic Distribution** of permits across downtown Vancouver.

#### 4. Data Visualization:

##### 1. Permit Processing Time by Project Type:
- **Visualization Tool**: AWS QuickSight / Tableau
- **Type of Visualization**: Bar Chart
- **Description**: 
  - This bar chart presents the **average time** taken to issue permits for different types of work (e.g., Residential, Commercial, Industrial).
  - It provides a comparative view of processing times, helping identify which project types experience longer delays.
  
##### 2. Geographic Distribution of Permits
- **Visualization Tool**: AWS QuickSight / Tableau
- **Type of Visualization**: Map
- **Description**:
  - A map was created to **visualize the geographical distribution** of building permits across downtown Vancouver.
  - The map is **color-coded** to distinguish between various permit categories such as **residential**, **commercial**, and **other types of permits**.
  - This visualization highlights areas with high development activity, offering a clear view of where major construction projects are concentrated within the downtown region.
  - This tool enables stakeholders to better understand urban development trends and identify zones of higher development density.

##### 3. Top 10 Projects by Value
- **Visualization Tool**: AWS QuickSight / Tableau
- **Type of Visualization**: Pie Chart
- **Description**:
  - A **pie chart** was used to present the **top 10 most expensive projects** based on their project value in Canadian dollars (CAD).
  - Each slice of the pie chart represents a high-value project, providing a comparative view of the **largest financial investments** in downtown Vancouver's construction activities.
  - This visualization helps in identifying the **major developments** in the region and where substantial resources are being allocated, giving insights into the most significant projects shaping Vancouver’s urban landscape.

##### 4. Trends in Permit Issuance
- **Visualization Tool**: AWS QuickSight / Tableau
- **Type of Visualization**: Line Chart
- **Description**:
  - A **line chart** was developed to visualize the **trends in building permit issuance** over time, with data broken down by month and year.
  - The chart highlights **fluctuations in permit issuance**, allowing for the observation of seasonal patterns or potential **impacts of city policies** on the frequency of permit applications.
  - This visualization is key in understanding the rhythm of urban development and identifying **periods of higher or lower construction activity**, which can inform future urban planning and resource allocation.


