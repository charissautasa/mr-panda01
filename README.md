# Data Analysis: Reading Habits in Indonesia (2020-2023)

This repository contains an analysis of reading habits and internet usage across different provinces in Indonesia from 2020 to 2023. The project explores trends in reading interest, average daily reading duration, and the relationship between internet access and reading habits. It also includes merging datasets and advanced data manipulation techniques.

## Table of Contents
- [Project Overview](#project-overview)
- [Assignments](#assignments)
  - [Assignment 3: Initial Analysis](#assignment-3-initial-analysis)
  - [Assignment 4: Data Merging](#assignment-4-data-merging)
  - [Assignment 5: Advanced Analysis](#assignment-5-advanced-analysis)
- [File Structure](#file-structure)
  - [Main Branch](#main-branch)
  - [File-Structure-Update Branch](#file-structure-update-branch)
  - [Final-Reflection Branch](#final-reflection-branch)
- [Data Source](#data-source)
- [Key Insights](#key-insights)
- [How to Use](#how-to-use)

## Project Overview
The goal of this project is to analyze reading habits in Indonesia and understand how factors like internet access influence reading interest. The analysis is conducted using Python and Jupyter Notebook, with visualizations created using libraries like Matplotlib and Seaborn. The project also includes merging datasets and advanced data manipulation techniques.

---

## Assignments

### Assignment 3: Initial Analysis
- **Objective**: Explore the dataset and perform initial analysis on reading habits and internet usage.
- **Key Files**:
  - `Assignment3_CharissaUtasa.ipynb`: Jupyter Notebook containing the data exploration and analysis.
  - `output_5_1.png`: Visualization of the distribution of reading interest.
  - `output_5_2.png`: Visualization of the average daily reading duration by year.
- **Key Insights**:
  - The average daily reading duration has slightly increased over the years.
  - Provinces with higher internet access tend to have higher reading interest scores.

### Assignment 4: Data Merging
- **Objective**: Merge two datasets (`main_df` and `new_df`) to analyze reading habits alongside additional data.
- **Key Files**:
  - `merged-data.ipynb`: Jupyter Notebook containing the data merging process.
  - `merged_data.csv`: The merged dataset saved after performing an outer join.
- **Key Insights**:
  - An **outer join** was used to retain all rows from both datasets, even if there were no matching values in the `Year` column.
  - Missing values (`NaN`) in the merged dataset indicate where the datasets do not overlap, providing a comprehensive view of the data.

### Assignment 5: Advanced Analysis
- **Objective**: Perform advanced data manipulation and analysis, including handling compound keys and refining the merged dataset.
- **Key Files**:
  - `Assignment5Reflection_CharissaUtasa`: Reflection on the project and lessons learned.
  - `Assignment5_writeup.md`: Write-up document for Assignment 5.
- **Key Insights**:
  - Compound keys were used to differentiate between entries with similar attributes (e.g., Iron Man from comics vs. movies).
  - The merged dataset was further refined to ensure accurate analysis and insights.

---

### Main Branch
The `main` branch contains the core files for the project:
- **`Assignment3_CharissaUtasa.ipynb`**: Jupyter Notebook for Assignment 3.
- **`Assignment3_CharissaUtasa.html`**: HTML export of the notebook.
- **`Assignment3_CharissaUtasa.md`**: Markdown export of the notebook.
- **`output_5_1.png`**: Visualization of the distribution of reading interest.
- **`output_5_2.png`**: Visualization of the average daily reading duration by year.
- **`README.md`**: Project overview and instructions.
- **`LICENSE`**: License file for the project.

### File-Structure-Update Branch
The `file-structure-update` branch organizes files into folders for better structure:
- **`documents`**:
  - `Assignment3_CharissaUtasa.md`: Markdown export of the notebook.
- **`results`**:
  - `output_5_1.png`: Visualization of the distribution of reading interest.
  - `output_5_2.png`: Visualization of the average daily reading duration by year.
- **`scripts`**:
  - `Assignment3_CharissaUtasa.html`: HTML export of the notebook.
  - `Assignment3_CharissaUtasa.ipynb`: Jupyter Notebook for Assignment 3.
  - `merged-data.ipynb`: Jupyter Notebook for Assignment 4 (data merging).
  - `.gitignore`: Specifies files to ignore in Git.
  - `LICENSE`: License file for the project.
  - `README.md`: Project overview and instructions.

### Final-Reflection Branch
The `final-reflection` branch includes the final write-up and reflection for Assignment 5:
- **`documents`**:
  - `Assignment5_writeup.md`: Write-up document for Assignment 5.
- **`scripts`**:
  - `Assignment5Reflection_CharissaUtasa`: Reflection document for Assignment 5.
  - `Assignment3_CharissUtasa.html`: HTML export of the notebook.
  - `Assignment3_CharissaUtasa.ipynb`: Jupyter Notebook for Assignment 3.
  - `Assignment3_CharissaUtasa.md`: Markdown export of the notebook.
  - `.gitignore`: Specifies files to ignore in Git.
  - `LICENSE`: License file for the project.
  - `README.md`: Project overview and instructions.
  - `output_5_1.png`: Visualization of the distribution of reading interest.
  - `output_5_2.png`: Visualization of the average daily reading duration by year.

---

## Data Source
The dataset used in this analysis was obtained from [Kaggle](https://www.kaggle.com/datasets/imaditia/Indonesia-reading-interest-2020-2023/resource-download). It includes data on reading habits and internet usage across Indonesian provinces from 2020 to 2023. Additional data from the PISA dataset was also used for merging in Assignment 4.

---

## Key Insights
- **Increase in Reading Duration**: The average daily reading duration has slightly increased over the years.
- **Internet Access and Reading Interest**: Provinces with higher internet access tend to have higher reading interest scores.
- **Regional Variations**: There are significant differences in reading habits between provinces, with urban areas showing higher reading interest compared to rural areas.
- **Data Merging**: An outer join was used to retain all data from both datasets, ensuring no data loss and providing a comprehensive view.

---

## How to Use
1. **Clone the Repository**:
   ```bash
   git clone https://github.com/YourUsername/mr-panda01.git
   cd mr-panda01
2. Explore the Data:
Open the Jupyter Notebooks (Assignment3_Charissultasa.ipynb and merged-data.ipynb) to explore the data and analysis.
Alternatively, view the HTML or Markdown files for a static version of the notebooks.
3. Run the Analysis:
Install the required dependencies.
Run the notebooks to reproduce the analysis or modify them for further exploration.


---

### **Key Updates in the New README**:
1. **File Structure Section**: Added detailed descriptions of the `main`, `file-structure-update`, and `final-reflection` branches, including their respective folders and files.
2. **Assignments Section**: Updated to include all assignments (3, 4, and 5) with their objectives, key files, and insights.
3. **Data Source**: Mentioned the additional PISA dataset used in Assignment 4.
4. **Key Insights**: Expanded to include insights from Assignments 4 and 5, such as data merging and compound keys.
5. **User-Friendly**: Made the instructions clear and concise for anyone who wants to use or contribute to the project.

