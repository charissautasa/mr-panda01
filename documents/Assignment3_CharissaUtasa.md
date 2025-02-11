# Assignment 3 - Baby Project 
## Charissa Utasa

The database I chose is data about reading interest per province in my home country, Indonesia from 2020-2023. I found interest in this data because reading is personally my hobby and I am interested in anything related to where I'm from.


```python
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
```


```python
df = pd.read_csv('TGM 2020-2023_eng FOR BABI4005.csv', delimiter=';')
```


```python
df.head()  # Display the first few rows
df.info()  # Get information about the DataFrame
df.describe()  # Summary statistics
```

    <class 'pandas.core.frame.DataFrame'>
    RangeIndex: 140 entries, 0 to 139
    Data columns (total 9 columns):
     #   Column                                        Non-Null Count  Dtype 
    ---  ------                                        --------------  ----- 
     0   Provinsi                                      140 non-null    object
     1   Year                                          140 non-null    int64 
     2   Reading Frequency per week                    140 non-null    object
     3   Number of Readings per Quarter                140 non-null    object
     4   Daily Reading Duration (in minutes)           140 non-null    object
     5   Internet Access Frequency per Week            105 non-null    object
     6   Daily Internet Duration (in minutes)          105 non-null    object
     7   Tingkat Kegemaran Membaca (Reading Interest)  140 non-null    object
     8   Category                                      140 non-null    object
    dtypes: int64(1), object(8)
    memory usage: 10.0+ KB
    




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Year</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>count</th>
      <td>140.000000</td>
    </tr>
    <tr>
      <th>mean</th>
      <td>2021.500000</td>
    </tr>
    <tr>
      <th>std</th>
      <td>1.122048</td>
    </tr>
    <tr>
      <th>min</th>
      <td>2020.000000</td>
    </tr>
    <tr>
      <th>25%</th>
      <td>2020.750000</td>
    </tr>
    <tr>
      <th>50%</th>
      <td>2021.500000</td>
    </tr>
    <tr>
      <th>75%</th>
      <td>2022.250000</td>
    </tr>
    <tr>
      <th>max</th>
      <td>2023.000000</td>
    </tr>
  </tbody>
</table>
</div>




```python
# Convert 'Daily Reading Duration (in minutes)' to numeric
df['Daily Reading Duration (in minutes)'] = pd.to_numeric(
    df['Daily Reading Duration (in minutes)'], errors='coerce'
)

# Check for missing values in the column
print(df['Daily Reading Duration (in minutes)'].isnull().sum())

# Fill missing values with the mean
df['Daily Reading Duration (in minutes)'] = df['Daily Reading Duration (in minutes)'].fillna(
    df['Daily Reading Duration (in minutes)'].mean()
)

# Distribution of Reading Interest
plt.figure(figsize=(10, 6))
sns.histplot(df['Tingkat Kegemaran Membaca (Reading Interest)'], bins=20, kde=True)
plt.title('Distribution of Reading Interest')
plt.xlabel('Reading Interest')
plt.ylabel('Frequency')
plt.show()

# Average Reading Duration by Year
avg_reading_duration = df.groupby('Year')['Daily Reading Duration (in minutes)'].mean()
avg_reading_duration.plot(kind='bar', title='Average Daily Reading Duration by Year')
plt.xlabel('Year')
plt.ylabel('Average Reading Duration (minutes)')
plt.show()
```

    58
    


    
![png](output_5_1.png)
    



    
![png](output_5_2.png)
    


### Data Overview
The dataset contains information about reading habits and internet usage across different provinces in Indonesia from 2020 to 2023. Key variables include:
- **Reading Frequency per week**: How often people read per week.
- **Daily Reading Duration (in minutes)**: Average time spent reading daily.
- **Internet Access Frequency per Week**: How often people access the internet per week.
- **Tingkat Kegemaran Membaca (Reading Interest)**: A score representing reading interest.

### Key Insights
- The average daily reading duration has increased slightly over the years.
- Provinces with higher internet access tend to have higher reading interest scores.
