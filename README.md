# finaltask5
---

## 📓 notebooks/Titanic_EDA.ipynb (Core Code Example)

Here is a simplified version of your notebook code:

```python
import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt

# Load dataset
df = pd.read_csv('../data/titanic.csv')

# Pairplot with survival hue
sns.pairplot(df[['age', 'fare', 'pclass', 'survived']], hue='survived')
plt.show()

# Age distribution
plt.hist(df['age'].dropna(), bins=30, color='skyblue')
plt.title("Age Distribution of Passengers")
plt.xlabel("Age")
plt.ylabel("Frequency")
plt.show()

# Boxplot: Fare by Passenger Class
sns.boxplot(x='pclass', y='fare', data=df)
plt.title("Fare Distribution by Passenger Class")
plt.xlabel("Passenger Class")
plt.ylabel("Fare")
plt.show()

# Violinplot: Age by Gender and Survival
sns.violinplot(data=df, x='sex', y='age', hue='survived', split=True)
plt.title("Age Distribution by Gender and Survival")
plt.show()

created by:Ankit Kumar Maity
