# Market Basket Analysis Project

## Power BI Dashboard Overview

The Market Basket Analysis project utilizes Power BI to visualize associations between grocery items based on transaction data. The dashboard focuses on showcasing associations using DAX metrics for two-item sets, highlighting patterns and insights that can be derived from customer purchase behaviors.

### Dashboard Features
- **Association Metrics**: Displays support, confidence, and lift for two-item sets.
- **Visualization**: Uses charts and tables to illustrate item associations.
- **Interactivity**: Allows filtering and exploration of association rules.

### Insights from Power BI Dashboard
- Identified strong associations:
  - Beef is frequently purchased with root vegetables, indicating potential recipes or meal combinations.
  - Wipped Cream has good association with curd, berries and butter suggesting common shopping patterns.
  - Yogurt is a common product linked with curd and cream cheeze, indicating cross-category purchasing habits.

[Link to the Dashboard](https://app.powerbi.com/groups/me/reports/a625c135-0031-48f5-930b-2ed44cc019c4/ReportSection?experience=power-bi)

## Apriori Algorithm Implementation for Further Analysis and Learning

In addition to the dashboard insights, the project incorporates the Apriori algorithm to uncover deeper associations beyond two-item sets. Here are some notable findings from the analysis.

It nvolves performing Market Basket Analysis on a dataset of grocery transactions. The analysis identifies frequent itemsets and association rules using the Apriori algorithm.

## Dataset
The dataset contains rows representing unique transactions, with columns indicating the items purchased in each transaction. Some rows may have null values, indicating fewer items in those transactions.

## Steps and Code Explanation

### Data Preparation
1. Fill null values in the dataset.
2. Convert the dataset to a list of transactions.
3. Remove null values from each transaction.

### Transforming Transactions
1. Use `TransactionEncoder` to transform the transaction data into a one-hot encoded format suitable for analysis.

### Applying Apriori Algorithm
1. Apply the Apriori algorithm to find frequent itemsets with a minimum support threshold.
2. Add a length column to the frequent itemsets DataFrame.
3. Sort itemsets by length in descending order.

### Generating Association Rules
1. Generate association rules from the frequent itemsets using lift as the metric.

### Visualization
**Scatter Plot**: Visualize the relationship between support, confidence, and lift of the association rules.

### Insights and Recommendations

### Association Rules Insights:
1. **Beef & Root Vegetables**
   - Support: 4.43%
   - Confidence: 34.09%
   - Lift: 3.56
   - Interpretation: Beef purchases are strongly associated with root vegetables, suggesting meal pairing opportunities.

2. **Tropical Fruit, Whole Milk & Root Vegetables**
   - Support: 3.71%
   - Confidence: 30.24%
   - Lift: 3.16
   - Interpretation: Customers buying tropical fruit and whole milk often include root vegetables in their shopping basket, indicating healthy eating patterns or recipe combinations.

3. **Root Vegetables & Yogurt**
   - Support: 2.32%
   - Confidence: 58.85%
   - Lift: 2.65
   - Interpretation: Root vegetables paired with yogurt show a high likelihood of also purchasing whole milk, suggesting a breakfast or snack combination preference.

#### Recommendations
1. **Cross-Selling Opportunities**: Use the identified associations to create cross-selling strategies.
2. **Promotional Strategies**: Design promotions for bundles of associated products.
3. **Inventory Management**: Ensure that frequently associated items are always stocked together.

## How to Run the Code
1. Clone this repository.
2. Install the required libraries:
   ```bash
   pip install pandas mlxtend matplotlib seaborn networkx
