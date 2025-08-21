# Groceries-dataset-for-Market-Basket-Analysis-MBA-
 The initial dataset was collected from Groceries dataset. Then data was modified and fragmented into 2 datasets for ease of MBA implementation. Here the "groceries data.csv" contains groceries transaction data from which you can do EDA and pre-process the data to feed it in the apriori algorithm.





🛒 Groceries Dataset for Market Basket Analysis (MBA)
📌 Overview

This dataset contains grocery store transaction records that can be used for Market Basket Analysis (MBA), a common technique in data mining to uncover associations between items frequently purchased together. MBA is widely applied in recommendation systems, cross-selling strategies, and retail analytics.

📂 Dataset Description

Each record represents a customer’s shopping basket.

Items purchased together appear in the same transaction.

The dataset is suitable for applying association rule mining algorithms such as Apriori, FP-Growth, or Eclat.

Key Features:

Transaction ID → Unique ID for each purchase.

Items → List of grocery items bought in that transaction.

🎯 Use Cases

Identify items frequently bought together.

Create product bundling and cross-sell opportunities.

Develop recommendation systems for retail/online stores.

Analyze shopping patterns and seasonal demand.

⚙️ Example Applications

Generate rules like:

{Bread, Butter} → {Jam}

{Milk} → {Cookies}

Visualize frequent itemsets with heatmaps, bar charts, or network graphs.

Support decision-making in retail marketing.

🚀 How to Use

Load the dataset using Python (pandas) or R.

Apply association rule mining with libraries such as:

mlxtend (Python)

arules (R)

Interpret the results using support, confidence, and lift metrics.

📊 Example (Python - Apriori)
from mlxtend.frequent_patterns import apriori, association_rules
import pandas as pd

# Load dataset
data = pd.read_csv("groceries.csv")

# Apply Apriori
frequent_itemsets = apriori(data, min_support=0.02, use_colnames=True)
rules = association_rules(frequent_itemsets, metric="lift", min_threshold=1)

print(rules.head())
