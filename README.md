# Projects

## [Project 1: Exploratory Data Analysis Using AWS Services](https://www.google.com)

### Project Title: Enrollment and Withdrawal Trends Analysis at UCW Using AWS

[Data Exploration Steps](https://github.com/vishakagupta18/Data-Analyst-Portfolio/blob/455663b84ecfec67c5f3ba6bb3a5dce3bbd4b27f/images/DataExplorationUCW.png)

#### Table of Contents ####

- [Project Description](#project-description)
- [Dataset](#dataset)
- [Objective](#objective)
- [Methodology](#methodology)
- [Tools and Technologies](#tools-and-technologies)
- [Deliverables](#deliverables)

### Project Description: ###
This project aims to perform an exploratory data analysis (EDA) of the University's Enrollment and Withdrawal dataset using AWS services to uncover insights related to student enrollment patterns, program distribution, and retention rates. By leveraging AWS tools such as S3, AWS Glue, and Athena, we explore trends based on features like gender, academic programs, and enrollment status. This project demonstrates how cloud-based services streamline large-scale data analysis and visualization.

### Dataset:
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

### Objective:
The objective is to analyze student enrollment and withdrawal patterns using AWS services, gaining insights into student demographics, program distribution, and factors influencing graduation and retention rates.

### Methodology:

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

### Tools and Technologies:
- **AWS S3** for data storage.
- **AWS Glue** for data cleaning, transformation, and cataloging.
- **AWS Athena** for SQL-based querying and analysis.
- **Amazon QuickSight** for creating interactive dashboards and data visualizations.

### Deliverables:
- A comprehensive AWS Glue ETL pipeline documented in a Jupyter Notebook or **Glue Job** code.
- SQL queries used in **AWS Athena** to analyze the dataset.
- A presentation summarizing the insights and findings for university stakeholders or peers.
