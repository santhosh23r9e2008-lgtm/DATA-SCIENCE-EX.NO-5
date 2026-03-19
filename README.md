# EXNO-5-DS-DATA VISUALIZATION USING MATPLOT LIBRARY

# Aim:
  To Perform Data Visualization using matplot python library for the given datas.

# EXPLANATION:
Data visualization is the graphical representation of information and data. By using visual elements like charts, graphs, and maps, data visualization tools provide an accessible way to see and understand trends, outliers, and patterns in data.

# Algorithm:
STEP 1:Include the necessary Library.

STEP 2:Read the given Data.

STEP 3:Apply data visualization techniques to identify the patterns of the data.

STEP 4:Apply the various data visualization tools wherever necessary.

STEP 5:Include Necessary parameters in each functions.

# Coding and Output:

 # Step 1: Include the necessary libraries
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
sns.set(style="whitegrid")
# Step 2: Read the dataset
df = sns.load_dataset("titanic") # You can also use: pd.read_csv("your_path.csv")
df.head()
# Step 3: Visualize missing data
plt.figure(figsize=(10,6))
sns.heatmap(df.isnull(), cbar=False, cmap='viridis', yticklabels=False)
plt.title("Missing Values Heatmap")
plt.show()
# Step 4: Countplot - Categorical Feature Visualization
plt.figure(figsize=(8,5))
sns.countplot(x='sex', data=df, palette='pastel')
plt.title("Passenger Count by Gender")
plt.show()
# Countplot - Survival vs Class
plt.figure(figsize=(8,5))
sns.countplot(x='survived', hue='class', data=df, palette='Set2')
plt.title("Survival Count by Passenger Class")
plt.xlabel("Survived (0 = No, 1 = Yes)")
plt.ylabel("Count")
plt.legend(title="Class")
plt.show()
# Step 5: Histogram - Continuous Data Distribution
plt.figure(figsize=(8,5))
sns.histplot(data=df, x='age', kde=True, bins=30, color='skyblue')
plt.title("Age Distribution of Passengers")
plt.xlabel("Age")
plt.ylabel("Frequency")
plt.show()
# Step 6: Boxplot - Outlier Detection and Comparison
plt.figure(figsize=(8,5))
sns.boxplot(x='pclass', y='age', data=df, palette='muted')
plt.title("Age Distribution across Passenger Classes")
plt.xlabel("Passenger Class")
plt.ylabel("Age")
plt.show()
# Step 7: Pairplot - Multiple Feature Interactions
sns.pairplot(df[['age', 'fare', 'pclass', 'survived']], hue='survived', palette='coolwarm')
plt.suptitle("Pairwise Relationships", y=1.02)
plt.show()
# Step 8: Correlation Heatmap - Numeric Feature Correlation
plt.figure(figsize=(10,7))
corr_matrix = df.corr()
sns.heatmap(corr_matrix, annot=True, cmap='Blues', linewidths=0.5)
plt.title("Correlation Matrix Heatmap")
plt.show()




<img width="1166" height="237" alt="image" src="https://github.com/user-attachments/assets/9f43094a-b9e7-4054-836e-ae7085f9801f" />



<img width="1001" height="757" alt="image" src="https://github.com/user-attachments/assets/767a3d5a-c0f7-4cc7-a571-14059f01f590" />



<img width="882" height="589" alt="image" src="https://github.com/user-attachments/assets/4606d514-75b8-48f1-bcca-acedeb9f30de" />



<img width="908" height="608" alt="image" src="https://github.com/user-attachments/assets/7ae38360-f183-42cd-880a-b36516d905d5" />



<img width="915" height="616" alt="image" src="https://github.com/user-attachments/assets/813aa925-1c9a-44da-a89e-f65eeaf56eb9" />



<img width="868" height="591" alt="image" src="https://github.com/user-attachments/assets/12440a5f-1f50-41c3-b21e-fbd0b02768cd" />



<img width="1041" height="909" alt="image" src="https://github.com/user-attachments/assets/afb9e5e8-926e-4e5f-8675-b7cf3aaf8102" />



<img width="993" height="788" alt="image" src="https://github.com/user-attachments/assets/e5e7bc96-4ae7-446b-bb7d-9b62b2a8321f" />

# Result:
 hence the data visualization was done on the give dataset using matplot library in python.
