# Shopping Trends Exploratory Data Analysis (EDA) Project

## Project Overview
This project analyzes shopping trends using a dataset containing various features related to customer purchases, such as age, gender, location, and purchase amount. The aim of the Exploratory Data Analysis (EDA) was to uncover insights, patterns, and relationships in the data using Python libraries like `pandas`, `seaborn`, and `matplotlib`.

## Dataset
The dataset used contains the following columns:
- `Customer ID`
- `Age`
- `Gender`
- `Item Purchased`
- `Category`
- `Purchase Amount (USD)`
- `Location`
- `Size`
- `Color`
- `Season`
- `Review Rating`
- `Subscription Status`
- `Shipping Type`
- `Discount Applied`
- `Promo Code Used`
- `Previous Purchases`
- `Payment Method`
- `Frequency of Purchases`

## Libraries Used
- **Pandas**: For data manipulation and analysis.
- **Seaborn**: For creating visualizations to display data trends.
- **Matplotlib**: For additional plotting features.
- **NumPy**: For numerical operations.

## Key Steps in the EDA

### 1. Data Loading and Initial Inspection
The data was loaded using `pandas` and inspected to understand its structure, missing values, and data types.
```python
import pandas as pd

# Load the dataset
data = pd.read_csv('shopping_data.csv')

# View the first few rows
data.head()

# Check for missing values
data.isnull().sum()
```
### 2. Data Cleaning
Handling missing values, checking for duplicates, and ensuring data integrity were critical steps before further analysis.

- **Missing values** were handled by either filling them with appropriate values or dropping the affected rows.
- **Duplicates** were checked and removed to ensure data consistency.

```python
# Drop duplicates
data.drop_duplicates(inplace=True)

# Fill missing values in the 'Review Rating' column with the median value
data['Review Rating'].fillna(data['Review Rating'].median(), inplace=True)
```
### Insights and Findings
Some key findings from the analysis include:

* Top Selling Items: Certain items were more frequently purchased across specific locations.
* Customer Segments: Younger customers (Age 18-30) had higher purchase frequencies compared to older age groups.
* Review Trends: Items with higher review ratings were purchased more frequently, especially in the electronics and clothing categories.
* Purchase Patterns: Promotional offers and discounts had a significant impact on purchasing behavior, especially among frequent buyers.

### Conclusion
The EDA uncovered important insights into customer shopping trends, which can be leveraged for targeted marketing strategies, product recommendations, and inventory management.
