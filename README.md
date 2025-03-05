# Customer Coupon Analysis

## Overview
This project aims to analyze factors that influence whether a customer accepts a coupon while driving. Using a dataset from the UCI Machine Learning repository, we explore customer demographics, contextual factors, and coupon attributes to understand decision-making patterns.

## Dataset Description
The dataset was collected via a survey on Amazon Mechanical Turk and contains various attributes, including:

- **User Attributes:** Gender, age, marital status, number of children, education, occupation, and income.
- **Behavioral Data:** Frequency of visiting bars, coffee houses, takeaway restaurants, and dining establishments with different price ranges.
- **Contextual Attributes:** Driving destination, weather, temperature, time of day, and passengers in the car.
- **Coupon Attributes:** Type of coupon and expiration duration.
- **Outcome Variable (Y):** Whether the customer accepts the coupon (1) or not (0).

## Problem Statement
The objective is to determine the key factors influencing a driver’s decision to accept a coupon. This involves analyzing correlations between contextual, behavioral, and demographic factors and the likelihood of coupon acceptance.

## Data Preprocessing and Analysis
The dataset is loaded and examined for missing values and data types:

```hcl
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns

data = pd.read_csv('data/coupons.csv')
print(data.head())
print(data.info())
```

## Occupation Distribution for Coffee House Coupon Acceptance
This visualization explores how occupation influences coupon acceptance for coffee houses:
```hcl
plt.figure(figsize=(10,5))
sns.barplot(x=all_occupations.index, y=all_occupations.values)
plt.xticks(rotation=90)
plt.title("Occupation Distribution for Coffee House Coupon Acceptance")
plt.xlabel("Occupation")
plt.ylabel("Count")
plt.show()
```
## How to Run the Analysis
1. Clone the repository:
   ```hcl
   git clone <repository_url>
   cd customer-coupon-analysis
   ```
2. Install required dependencies:
   ```hcl
   pip install pandas numpy matplotlib seaborn
   ```
3. Run the script:
   ```hcl
   python analysis.py
   ```

## Conclusion
By analyzing customer behaviors and contextual factors, this project aims to provide insights into how businesses can optimize their coupon distribution strategies to maximize acceptance rates.

## License
This project is licensed under the MIT license
