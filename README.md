# 🛍️ TASK 3: Customer Segmentation using K-Means Clustering

## 📌 Overview
This project uses the **K-Means clustering** algorithm to divide mall customers into groups of similar shoppers. The best number of groups is found with the **Elbow Method**, confirmed with the **Silhouette Score**, and the final groups are visualized with easy-to-read charts.

Knowing the groups helps a business plan the right offer for the right customer, instead of one offer for everyone.

## 🎯 Objectives
- Load and understand the customer dataset
- Check for missing values and duplicate records
- Explore the data with simple charts
- Scale the features so they are treated fairly
- Find the best number of clusters using the **Elbow Method**
- Train a **K-Means** model and visualize the clusters
- Explain each customer group in simple words

## 📁 Dataset
The project uses `Mall_Customers.csv` (**200 customers, 5 columns**).

| Column | Description |
|---|---|
| `CustomerID` | Unique ID of the customer (not used for clustering) |
| `Gender` | Male or Female |
| `Age` | Age of the customer |
| `Annual Income (k$)` | Yearly income in thousand dollars |
| `Spending Score (1-100)` | Score given by the mall. A higher score means the customer spends more |

> The Spending Score is built from shopping behaviour, so it works as a summary of customer transactions.

## 🛠️ Technologies Used
Python • Pandas • NumPy • Matplotlib • Seaborn • Scikit-learn • Google Colab

## 📊 Steps Performed
1. Import libraries
2. Load the dataset and view the first rows
3. Check shape, columns, and data types
4. Check missing values and duplicates
5. Statistical summary
6. Exploratory charts (gender count, histograms, correlation heatmap, income vs spending scatter plot)
7. Select features: Annual Income and Spending Score
8. Scale the features with `StandardScaler`
9. **Elbow Method** to find the best K
10. **Silhouette Score** as a second check
11. Train the final K-Means model (K = 5)
12. Visualize the clusters with centroids
13. Profile and name each cluster
14. Final named cluster chart with segment sizes
15. Compare segments by income, spending, age, and gender
16. Business ideas for each segment

## 📈 Choosing the Number of Clusters
- The **Elbow Method** shows the bend at **K = 5**. After 5, the inertia drops only a little.
- The **Silhouette Score** is also highest at **K = 5** (about **0.555**).
- Both methods agree, so **5 clusters** were used.

## 👥 Customer Segments Found

| Segment | Customers | Avg Age | Avg Income | Avg Spending | Meaning |
|---|---:|---:|---:|---:|---|
| **Big Spenders** | 39 | ~33 | ~87k | ~82 | High income, high spending. Best customers |
| **Fun Spenders** | 22 | ~25 | ~26k | ~79 | Young, low income, but love to spend |
| **Average Customers** | 81 | ~43 | ~55k | ~50 | Largest group, middle in everything |
| **Budget Savers** | 23 | ~45 | ~26k | ~21 | Low income, low spending |
| **Careful Rich** | 35 | ~41 | ~88k | ~17 | High income, but spend very little |

## 💡 Business Ideas

| Segment | Idea |
|---|---|
| Big Spenders | VIP treatment, loyalty cards, early access to new products |
| Fun Spenders | Discounts, festival sales, fashion and entertainment offers |
| Average Customers | Regular offers and combo deals to slowly increase spending |
| Careful Rich | Quality and luxury offers, personal attention to find out why they spend little |
| Budget Savers | Small coupons and low-price products, avoid heavy advertising |

## 🔍 Key Insights
- The data is clean: **no missing values and no duplicates**.
- Income and Spending Score are **not related** (correlation 0.01), so clustering finds groups that a simple rule cannot.
- **Big Spenders** and **Careful Rich** have almost the same income, but very different spending (about 82 vs 17).
- **Younger customers** (Fun Spenders and Big Spenders) tend to spend more.
- **Gender does not decide the group.** Males and females appear in every segment.

## ⚠️ Limitations
- Only two features were used for clustering. Adding Age or Gender may give different groups.
- The dataset is small (200 customers).
- K-Means works best with round-shaped groups. Other methods, such as DBSCAN, may suit other shapes.

## 📁 Project Structure
```
├── README.md
├── Mall_Customers.csv
└── Task_3_Customer_Segmentation_KMeans.ipynb
```

## ▶️ How to Run
```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```
Place `Mall_Customers.csv` in the same folder as the notebook (or upload it in Google Colab) and run all cells.

## 📝 Conclusion
K-Means clustering divided the mall customers into **5 clear groups**: Average Customers, Big Spenders, Careful Rich, Fun Spenders, and Budget Savers. The Elbow Method and Silhouette Score both pointed to K = 5. These groups help the mall plan the right offers for the right customers and grow sales.

## 👤 Author
**Prathana Kamlesh Tandel**
