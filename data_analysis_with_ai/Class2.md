# Class 2: Data Analysis Workflow and Descriptive Analysis

Class 2 focuses on the overall workflow of data analysis, including data description and preparation. Participants learn about descriptive data analysis (DDA), which involves summarizing and characterizing datasets using statistical methods. The class also demonstrates how AI tools can support and enhance these early stages of the analysis process.

[Download the slide deck.](./DA2I_Class02_DD_DDA.pdf)

## Hands-on activities and prompts:

### 1. Sampling with AI
- For the mammographic dataset, prompt:
```
Using a stratified sampling approach, sample 20% of the dataset. Assume variable ‘severity’ as the target variable.
```
```
Using a stratified sampling approach, sample 20% of the dataset. Assume variable ‘shape’ as the target variable.
```
- Analyze the results.

### 2. Finding and Replacing Missing Values with AI
- Open the mammographic_masses_nominal dataset using Excel.
- Observe the missing values represented with ‘?’.
- Apply filters in all variables to observe the missing values.
- Prompt the tools to find missing values:
```
Find the missing values of the mammographic data (they are represented by the question mark)
```
- Prompt the tools to replace (imputate) missing values:
```
Replace these missing values by a central tendency measure of the variable and save the dataset with the name mammographic_data_wo_missing_values.
```

### 3. Data Normalization with AI
- For the Iris dataset of Fisher, prompt the tools to:
```
Normalize the iris dataset attached using a min-max method and the z-score
```
- Analyze the results.

### 4. Frequency Table and Pie Chart with AI
- For the normalized or unnormalized mammographic dataset, prompt:
```
Print the frequency table with the absolute, relative, and cumulative frequency, then plot the pie chart of variable 'Shape' in the mammographic dataset
```
- Analyze the results.

### 5. Contingency Table and Frequency Distribution with AI
- Prompt:
```
Draw the contingency table for variables 'Shape' vs 'Severity' of the mammographic dataset
```
- For the forestfires dataset, prompt:
```
Plot the frequency distribution for all variables of the attached forestfires dataset
```
- In Claude.ai you may try:
```
I want you to show the visuals. You can create an interactive artifact to show them.
```

### 6. Descriptive Analysis with AI
- Prompt:
```
For the forestfires dataset, do:
    1) Create a table with the central tendency, variability measures, and the measures of shape of the variables in the forest fires dataset.
    2) Plot the correlation matrix of all numeric variables.
    3) Plot the dispersion graphs of some pairs of numeric variables involving ‘temp’ and ‘ffmc’ with the best linear regressors showing their correlation trend.
```
