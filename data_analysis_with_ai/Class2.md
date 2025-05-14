# Class 2: Data Analysis Workflow and Descriptive Analysis

Class 2 focuses on the overall workflow of data analysis, including data description and preparation. Participants learn about descriptive data analysis (DDA), which involves summarizing and characterizing datasets using statistical methods. The class also demonstrates how AI tools can support and enhance these early stages of the analysis process.

[Download the slide deck.](./DA2I_Class02_DD_DDA.pdf)

## Hands-on activities and prompts:

### 1. Data Dictionary and Sampling with AI
- For the mammographic dataset, prompt:

Version 1:
```
Generate a data dictionary including the variable name, its definition (meaning), the type of variable (numeric or nominal), and the number of missing values per variable.
```
Version 2:
```
Act as a data analyst. For a data dictionary containing the variable name, its definition (meaning), the type of variable (numeric or nominal), and the number of missing values per variable, create a data dictionary for the mammographic dataset.
```

Version 1:
```
Using a stratified sampling approach, sample 20% of the dataset. Assume variable ‘severity’ as the target variable.
```
Version 2:
```
Act as a data scientist. Using a stratified-sampling approach (by ‘severity’), sample 20% of the dataset so that each severity class is proportionally represented. Return the resulting subset as a new table.
```

Version 1:
```
Using a stratified sampling approach, sample 20% of the dataset. Assume variable ‘shape’ as the target variable.
```
Version 2:
```
Act as a data scientist. Using a stratified-sampling approach (by ‘Shape’), sample 20% of the dataset so that each Shape category is proportionally represented. Return the resulting subset as a new table.
```
- Analyze the results.

### 2. Finding and Imputing Missing Values with AI
- Open the mammographic_masses_nominal dataset using Excel.
- Observe the missing values represented with ‘?’.
- Apply filters in all variables to observe the missing values.
- Prompt the tools to find missing values:

Version 1:
```
Find the missing values of the mammographic data (they are represented by the question mark)
```
Version 2:
```
Act as a data analyst. In the mammographic dataset, identify all missing entries (marked ?). Report, for each column, the number and percentage of missing values.
```
- Prompt the tools to replace (imputate) missing values:

Version 1:
```
Impute these missing values by a central tendency measure of the variable and save the dataset with the name mammographic_data_wo_missing_values.
```
Version 2:
```
Act as a data engineer. For each column in the mammographic dataset with missing values (marked ?), impute by an appropriate central tendency measure of the variable. Save the cleaned dataset as a csv with the name mammographic_data_wo_missing_values and confirm the imputation counts per column.
```

### 3. Data Normalization with AI
- For the Iris dataset of Fisher, prompt the tools to:

Version 1:
```
Normalize the iris dataset attached using a min-max method and the z-score
```
Version 2:
```
Act as a data scientist. Create two normalized versions of the Iris dataset: one with Min–Max scaling and one with Z-score standardization. Return both datasets as csvs and summarize the transformed ranges.
```
- Analyze the results.

### 4. Frequency Table and Pie Chart with AI
- For the normalized or unnormalized mammographic dataset, prompt:

Version 1:
```
Print the frequency table with the absolute, relative, and cumulative frequency, then plot the pie chart of variable 'Shape' in the mammographic dataset.
```
Version 2:
```
Act as a data analyst. Create a frequency table with the absolute, relative, and cumulative frequency, then plot the pie chart of variable 'Shape' in the mammographic dataset.
```
- Analyze the results.

### 5. Contingency Table and Frequency Distribution with AI
- Prompt:

Version 1:
```
Draw the contingency table for variables 'Shape' vs 'Severity' of the mammographic dataset
```
Version 2:
```
Act as a data analyst. Create a contingency table crossing Shape (rows) and Severity (columns) for the mammographic dataset. Include both raw counts and row-percentage margins.
```
- For the forestfires dataset, prompt:

Version 1:
```
Plot the frequency distribution for all variables of the attached forestfires dataset
```
Version 2:
```
Act as a data scientist. For each numeric variable in the forestfires dataset, plot a histogram showing its frequency distribution. Arrange the plots in a grid for side-by-side comparison.
```
- In Claude.ai you may try:

Version 1:
```
I want you to show the visuals. You can create an interactive artifact to show them.
```
Version 2:
```
Act as a data visualization specialist. Identify an appropriate interactive artifact and construct visualizations of the above.
```

### 6. Descriptive Analysis with AI
- Prompt:

Version 1:
```
For the forestfires dataset, do:
    1) Create a table with the central tendency, variability measures, and the measures of shape of the variables in the forest fires dataset.
    2) Plot the correlation matrix of all numeric variables.
    3) Plot the dispersion graphs of some pairs of numeric variables involving ‘temp’ and ‘ffmc’ with the best linear regressors showing their correlation trend.
```
Version 2:
```
Act as a data scientist. Using the forestfires dataset:
1. Identify and compute for each numeric variable: central tendency, measures of variability, and measures of shape. Present results in a summary table.
2. Plot a correlation matrix of all numeric variables.
3. Calculate the best fitted linear regression for the pair (temp, FFMC) and draw scatter plots, displaying the correlation coefficient on each plot.
```
## Do you want to compare with non-AI tools?  
If you want to contrast how to perform Exploratory Data Analysis (EDA) using a standard, non-AI tool, I invite you to watch my classes on **EDA with Excel** at the following link:  
[Watch on YouTube](https://www.youtube.com/watch?v=zxFmJuPDWrs&list=PLDAcHI0EPlZIVv6xCs-ahKSVd7oLzmR-d&index=6)
