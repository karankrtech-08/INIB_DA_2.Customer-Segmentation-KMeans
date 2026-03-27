# INIB_DA_2.Customer-Segmentation-KMeans
Customer segmentation using K-Means clustering on the Mall Customers dataset. This project identifies distinct customer groups based on annual income and spending score to enable targeted marketing strategies.
# Customer Segmentation using K-Means Clustering

## Project Overview
This project performs customer segmentation using unsupervised machine learning (K-Means clustering) on the **Mall Customers dataset**. The goal is to group customers based on their annual income and spending score, allowing businesses to tailor marketing strategies for each segment.

## Dataset
- **Source**: # (Kaggle)
- **Size**: 200 customer records
- **Features**:
  - `CustomerID` – unique identifier
  - `Gender` – customer gender
  - `Age` – customer age
  - `Annual Income (k$)` – yearly income in thousands of dollars
  - `Spending Score (1-100)` – score based on purchase behavior

## Tools & Libraries
- Python 3
- Jupyter Notebook
- Pandas, NumPy – data handling
- Matplotlib, Seaborn – visualization
- Scikit-learn – scaling, clustering, evaluation

## Project Steps
1. **Data Loading & Exploration**  
   - Load the dataset and check for missing values.
   - Visualize distributions of annual income and spending score.

2. **Feature Selection & Preprocessing**  
   - Selected features: `Annual Income (k$)` and `Spending Score (1-100)`
   - Standardized the features using `StandardScaler` for equal contribution.

3. **Determining Optimal Clusters**  
   - **Elbow Method**: Plot WCSS vs. number of clusters to find the "elbow".
   - **Silhouette Score**: Evaluate cluster cohesion and separation.
   - **Result**: Both methods suggest **k=5** clusters.

4. **Applying K-Means**  
   - Fit K-Means with `n_clusters=5`, `init='k-means++'`, `random_state=42`.
   - Assign each customer to a cluster.

5. **Visualizing Clusters**  
   - Scatter plot of Annual Income vs. Spending Score with cluster colors.

6. **Cluster Profiling & Interpretation**  
   - Grouped by cluster to compute average income, spending score, age, and majority gender.
   - Identified five customer segments:

| Cluster | Income (avg) | Spending (avg) | Age (avg) | Gender (majority) | Segment Name               |
|---------|--------------|----------------|-----------|-------------------|----------------------------|
| 0       | 55.30        | 49.52          | 42.72     | Female            | Average Customers          |
| 1       | 86.54        | 82.13          | 32.69     | Female            | Premium Customers          |
| 2       | 25.73        | 79.36          | 25.27     | Female            | Impulsive Buyers           |
| 3       | 88.20        | 17.11          | 41.11     | Male              | Careful Spenders           |
| 4       | 26.30        | 20.91          | 45.22     | Female            | Economy Shoppers           |

7. **Business Insights & Recommendations**  
   - **Premium Customers**: VIP loyalty programs, exclusive offers.
   - **Careful Spenders**: Value deals, bulk discounts.
   - **Impulsive Buyers**: “Buy now, pay later”, flash sales.
   - **Average Customers**: Bundle deals, upselling.
   - **Economy Shoppers**: Essential products, price guarantees.

License
This project is for educational purposes.
---

## How to Upload to GitHub

1. **Create a new repository** on GitHub (name it `Customer-Segmentation-KMeans`).
2. **On your local machine**, navigate to your project folder (where the `.ipynb` file and `README.md` are).
3. Initialize Git:
   ```bash
   git init
   
4.Add files:
git add .

5Commit:
git commit -m "Initial commit: Customer segmentation project"

6.Link to remote repository:
git remote add origin https://github.com/yourusername/Customer-Segmentation-KMeans.git

7.Push:
git push -u origin main
