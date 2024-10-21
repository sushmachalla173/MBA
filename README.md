# MBA
Overview
This project performs Market Basket Analysis using a dataset of e-commerce transactions. The analysis aims to identify patterns and associations in the data using association rule mining techniques like the Apriori algorithm. Market Basket Analysis helps in understanding customer purchasing behaviors and can be used for recommendation systems, inventory management, and marketing strategies.

Features
Data Loading and Preprocessing: Reads and cleans the e-commerce data.
Exploratory Data Analysis (EDA): Examines the dataset to gain insights.
Frequent Itemset Mining: Uses the Apriori algorithm to find frequently occurring item sets.
Association Rule Mining: Identifies relationships between items using association rules.
Data Cleaning and Preprocessing:

Columns were stripped of whitespace, converted to appropriate data types, and some columns (like StockCode) were dropped.
Duplicate entries were removed, and some data (e.g., transactions with non-numeric InvoiceNo) were filtered out.
Country-Specific Analysis:

The analysis focused on transactions in Germany. This approach suggests looking at localized purchasing behavior to identify patterns specific to that market.
Data Transformation:

Transactions were converted into a "basket" format, where each row represents an invoice, and columns represent different products. The presence of a product in the invoice was encoded as 1, and the absence as 0.
Items like "POSTAGE" were excluded from the analysis to avoid skewing results.
Next, I’ll delve into more cells to find any specific insights or visualizations that were generated, such as frequent itemsets and association rules.

Frequent Itemsets Generation:

The Apriori algorithm was used to identify frequent itemsets with a minimum support of 5%. This step reveals commonly co-purchased products in the German transactions.
Association Rule Mining:

Rules were generated based on the frequent itemsets using metrics such as "lift" and "confidence" to measure the strength and reliability of the associations.
Filtering of Rules:

Rules with a confidence of at least 0.7 and a lift greater than 1.5 were considered significant. These thresholds help filter out less meaningful associations, focusing on strong relationships between products.

Support tells you how frequently items appear together in the dataset.
Confidence indicates the strength of the implication from the antecedent to the consequent.
Lift helps assess the value of the rule by comparing the observed frequency of co-occurrence to the expected frequency if the items were independent.

