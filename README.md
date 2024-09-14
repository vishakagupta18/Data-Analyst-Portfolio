# Data Analysis Projects

## Exploratory Data Analysis

### Project Title: Surviving the Titanic: An Exploratory Data Analysis

**Project Description:**  
The primary goal of this project is to perform an exploratory data analysis (EDA) on the Titanic dataset to uncover patterns, trends, and insights related to passenger survival. By analyzing various features such as age, gender, class, and fare, we aim to understand the factors that influenced the likelihood of survival during the Titanic disaster.

### Dataset:
The Titanic dataset consists of passenger information from the ill-fated voyage of the RMS Titanic, including details such as:
- **Passenger ID**: Unique identifier for each passenger
- **Survived**: Survival status (0 = No, 1 = Yes)
- **Pclass**: Passenger class (1st, 2nd, 3rd)
- **Name**: Name of the passenger
- **Sex**: Gender of the passenger
- **Age**: Age of the passenger
- **SibSp**: Number of siblings/spouses aboard
- **Parch**: Number of parents/children aboard
- **Ticket**: Ticket number
- **Fare**: Fare paid by the passenger
- **Embarked**: Port of embarkation (C = Cherbourg, Q = Queenstown, S = Southampton)

### Objective:
Perform an exploratory data analysis to uncover key insights related to survival rates on the Titanic.

### Methodology:

1. **Data Collection and Preparation**:
   - Load the Titanic dataset using Python libraries like Pandas.
   - Perform initial data cleaning, which includes handling missing values, correcting data types, and renaming columns for clarity.

2. **Descriptive Statistics**:
   - Generate summary statistics (mean, median, mode) for numerical features (like Age and Fare) and frequency distributions for categorical features (like Pclass and Sex).

3. **Data Visualization**:
   - Create visualizations to illustrate key insights:
     - **Histograms and Boxplots**: Analyze the distribution of continuous variables like Age and Fare.
     - **Bar Charts**: Showcase survival rates across different categories (e.g., Sex, Pclass).
     - **Heatmaps**: Visualize correlations between numerical variables.

4. **Survival Analysis**:
   - Compare survival rates:
     - **By gender**: Determine if there is a significant difference in survival rates between male and female passengers.
     - **By class**: Analyze how passenger class affected survival chances.
     - **By age group**: Create age bins to assess survival across different age demographics.

5. **Insights and Findings**:
   - Summarize the findings based on data visualizations and statistical analyses, highlighting notable trends and patterns (e.g., women and children had higher survival rates, first-class passengers had a significant survival advantage).

6. **Conclusion**:
   - Discuss the implications of the findings and suggest further analyses or data-driven decisions that could be explored, such as building predictive models to classify survival based on passenger features.

### Tools and Technologies:
- Python (Pandas, NumPy, Matplotlib, Seaborn)
- Jupyter Notebook for interactive data exploration
- Any additional data visualization tools like Tableau or Power BI (optional)

### Deliverables:
- A comprehensive Jupyter Notebook containing all steps of the analysis, including code, visualizations, and narrative explanations of findings.
- A presentation summarizing key insights and visualizations for stakeholders or peers.

