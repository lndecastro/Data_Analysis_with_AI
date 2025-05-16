# Class 5: Full Data Analysis Project with AI Integration

The final class is a capstone session where participants apply the entire AI-augmented analysis workflow to a comprehensive project. This includes setting project requirements, defining learning objectives, and integrating all previously learned skills. The class also encourages discussion about the limitations, ethics, and accuracy of AI-generated outputs, ensuring a well-rounded understanding of AI in data analysis.

[Download the slide deck.](./DA2I_Class05_FinalClass.pdf)

## 5.1 Small, LLM-Compatible Datasets for Data Analysis Projects

1. **Wine Quality**
Data on physicochemical tests of red and white wine samples, with quality ratings.
[Download CSV](https://archive.ics.uci.edu/ml/machine-learning-databases/wine-quality/winequality-red.csv)

2. **Titanic Survivors**
Passenger data from the Titanic, used for survival prediction.
[Download CSV](https://raw.githubusercontent.com/datasciencedojo/datasets/master/titanic.csv)

3. **Penguins Dataset**
Alternative to Iris; contains data on penguin species, island, bill length, etc.
[Download CSV](https://raw.githubusercontent.com/mwaskom/seaborn-data/master/penguins.csv)

4. **Heart Disease**
Medical attributes used to predict heart disease presence.
[Download CSV](https://raw.githubusercontent.com/datablist/sample-csv-files/main/files/people-heart.csv)

5. **Student Performance**
Grades and demographics of secondary school students in Portugal.
[Download CSV](https://archive.ics.uci.edu/ml/machine-learning-databases/00320/student.zip)

6. **Bank Marketing**
Data related to direct marketing campaigns of a Portuguese banking institution.
[Download CSV](https://archive.ics.uci.edu/ml/machine-learning-databases/00222/bank.zip)

7. **Diabetes (Pima Indians)**
Medical data for predicting diabetes in Pima Indian women.
[Download CSV](https://raw.githubusercontent.com/jbrownlee/Datasets/master/pima-indians-diabetes.data.csv)

8. **Spotify Top Tracks**
Top Spotify songs with audio features and popularity scores.
[Download CSV](https://raw.githubusercontent.com/murpi/wilddata/master/spotify.csv)

9. **COVID-19 Cases by Country**
Summary of confirmed COVID-19 cases, deaths, and recoveries by country.
[Download CSV](https://raw.githubusercontent.com/datasets/covid-19/master/data/countries-aggregated.csv)

10. **Housing Prices (Boston)**
Historic dataset of housing prices and neighborhood statistics.
[Download CSV](https://raw.githubusercontent.com/selva86/datasets/master/BostonHousing.csv)

11. **Loan Prediction**
Loan application data used to predict loan approval.
[Download CSV](https://raw.githubusercontent.com/dphi-official/Datasets/master/Loan_Data/loan_data.csv)

12. **Fake vs Real News**
A dataset containing labeled real and fake news articles.
[Download CSV](https://raw.githubusercontent.com/clmentbisaillon/fake-and-real-news-dataset/master/data/fake.csv)

13. **Employee Attrition**
HR analytics dataset to predict employee attrition.
[Download CSV](https://raw.githubusercontent.com/IBM/employee-attrition-aif360/master/data/emp_attrition.csv)

14. **Video Game Sales**
Global video game sales data by platform and publisher.
[Download CSV](https://raw.githubusercontent.com/GregorUT/vgsales.com/master/vgsales.csv)

15. **Netflix Titles**
Metadata of movies and TV shows available on Netflix.
[Download CSV](https://raw.githubusercontent.com/sharmaroshan/Netflix-Datasets/main/netflix_titles.csv)

16. **Airbnb NYC 2019**
Listings in New York City with price, neighborhood, and room type.
[Download CSV](https://raw.githubusercontent.com/datasciencedojo/datasets/master/Airbnb%20NYC%202019.csv)

17. **Countries of the World**
Socio-economic indicators for countries: population, GDP, birthrate, etc.
[Download CSV](https://raw.githubusercontent.com/cs109/2014_data/master/countries.csv)

## 5.2 Data Analysis Workflow Prompt Chain

### Step 1: Data Description and Preparation

**Prompt 1.1 – Data Dictionary**
```
I am a senior data analyst responsible for running a full data analysis project, including data preparation, descriptive statistics, data visualization, data storytelling, and dashboard design.
I uploaded a dataset, please generate a data dictionary including:
- Variable name
- Description (infer based on name or dataset metadata)
- Data type (categorical or numerical)
- Domain (e.g., numeric range, category values)
- Number of missing values

Output as a table.
```

**Prompt 1.2 – Data Cleaning and Preprocessing**
```
Perform initial data preparation steps on the uploaded dataset:
- Show summary statistics for all variables.
- Indicate variables with missing values.
- Ask if I want to impute missing values (mean, median, mode, or drop rows/columns).
- Ask if I want to sample the data (e.g., random 10%, stratified, etc.).
- Ask if I want to apply feature scaling (z-score or mn-max).

Once I confirm the options, apply them and return a summary of changes made.
```

### Step 2: Descriptive Data Analysis

**Prompt 2.1 – Summary Statistics**

```
Using the prepared dataset, calculate and display for all numerical variables:
- Mean and median
- Standard deviation, range, interquartile range
- Skewness and kurtosis
For the categorical variables calculate:
- Mode
- Absolute and relative count per category 

Present results in one or more tables.
```

**Prompt 2.2 – Contingency Matrix** 
```
Generate contingency tables (cross-tabulations) for all discrete/categorical variables in relation to a given target variable. 

Ask me to specify the target variable (e.g., 'Churn', 'Outcome', etc.). If not specified, identify the most likely one automatically based on cardinality and naming.
```

### Step 3: Data Visualization

**Prompt 3.1 – Visualization Suite**

```
Based on the dataset, generate the following recommended visualizations:
- Histogram or boxplot for each numerical variable
- Bar chart for categorical variable frequencies
- Pairplot or correlation heatmap (if more than 3 numerical variables)
```

**Prompt 3.2 – Exploring Visualizations**
```
Based on the dataset, recommend visuals that can potentially help me extract useful insights from the dataset and explain the recommendations.

Also ask me the following:
- Which plots would you like to see?
- Do you want a downloadable file with all plots as images?
```

### Step 4: Data Storytelling (Narrative)

**Prompt 4.1 – Narrative Insights**

```
Help me create a data storytelling narrative using the following structure:

1. Audience and Purpose: Recommend an audience and what decision or insight they seek.
2. Key Message and Depth: Recommend a key message I could deliver and the depth of analysis.
3. Narrative Creation: Based on previous recommendations, generate a compelling narrative summarizing the findings, patterns, and implications tailored to the audience and message.
```

**Prompt 4.2 – Narrative Framework**

```
Help me create a data storytelling narrative using the following structure:

1. Audience and Purpose: Ask me who the audience is (e.g., executives, students, clients) and what decision or insight they seek.
2. Key Message and Depth: Ask for the key message I want to deliver (e.g., "Revenue increased due to marketing efforts") and the depth of analysis (e.g., overview vs deep dive).
3. Narrative Creation: Based on previous analysis, generate a compelling narrative summarizing the findings, patterns, and implications tailored to the audience and message.
```

### Step 5: Dashboard Design

**Prompt 5.1 – Dashboard Planning**

```
Design a dashboard for this dataset. Ask me to specify:
- Preferred tool (Power BI, Tableau, Python Dash, etc.)
- Layout preferences
- Key KPIs or variables to highlight
- Filters or interactivity (e.g., time filters, segment selection)

Then suggest:
- Dashboard layout (e.g., 2x2 grid)
- Recommended visualizations per section
- Color scheme (light/dark, branded colors)
- Textual elements (title, annotations)

Optionally, generate sample code or a storyboard sketch if Plotly Dash is selected.
```
