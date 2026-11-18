# Customer Segmentation Using K-Means Clustering

## Project Overview

This project was developed as part of the **Elevvo Machine Learning Internship – Machine Learning Track**.

The objective is to segment mall customers into distinct groups based on their annual income and spending behaviour using unsupervised machine learning.

The project applies K-Means clustering to identify customer groups and explores how these segments can support targeted marketing strategies and customer relationship management.

## Objectives

- Explore customer demographic and spending information.
- Perform exploratory data analysis (EDA).
- Visualize relationships between annual income and spending scores.
- Apply feature scaling using StandardScaler.
- Determine the optimal number of clusters.
- Implement K-Means clustering.
- Evaluate clustering quality using the Silhouette Score.
- Interpret customer segments and their business implications.

## Dataset

**Dataset:** Mall Customer Segmentation

**Source:** [Kaggle – Customer Segmentation Tutorial](https://www.kaggle.com/datasets/vjchoudhary7/customer-segmentation-tutorial-in-python)

Dataset information:
- Total customers: 200
- Total columns: 5
- Numerical features: CustomerID, Age, Annual Income, Spending Score
- Categorical feature: Gender

### Selected Clustering Features

1. Annual Income (k$)
2. Spending Score (1-100)

CustomerID was excluded because it is an identifier rather than a meaningful behavioural feature. Gender and Age were retained for exploratory analysis but excluded from the primary clustering model.

## Technologies and Libraries

| Technology | Purpose |
|---|---|
| Python | Programming language |
| Google Colab | Development environment |
| Pandas | Data manipulation |
| NumPy | Numerical operations |
| Matplotlib | Data visualization |
| Scikit-learn | Machine learning |
| StandardScaler | Feature scaling |
| K-Means | Customer clustering |

## Project Methodology

### 1. Data Loading and Exploration

The dataset was loaded and inspected.

Initial findings:
- 200 customer records.
- 5 columns.
- No missing values.
- No duplicate records.

### 2. Exploratory Data Analysis

The following visualizations were created:

- Gender distribution.
- Age distribution.
- Annual income distribution.
- Spending score distribution.
- Annual income vs spending score.
- Feature correlation analysis.

Key findings:

- Female customers: 112 (56%).
- Male customers: 88 (44%).
- Average age: 38.85 years.
- Average annual income: $60.56k.
- Average spending score: 50.20.

The correlation between age and spending score was approximately -0.3272, indicating a negative relationship.

### 3. Feature Selection and Scaling

Annual Income and Spending Score were selected as the primary clustering features.

StandardScaler was applied to standardize both features before clustering.

### 4. Optimal Number of Clusters

Two evaluation methods were used.

**Elbow Method**

The WCSS curve showed a significant reduction up to five clusters, after which the improvement became smaller.

**Silhouette Score**

Silhouette scores were calculated for K values between 2 and 10.

The highest score was obtained at K = 5.

| K | Silhouette Score |
|---|---:|
| 2 | 0.3213 |
| 3 | 0.4666 |
| 4 | 0.4939 |
| 5 | 0.5547 |
| 6 | 0.5399 |
| 7 | 0.5281 |
| 8 | 0.4552 |
| 9 | 0.4571 |
| 10 | 0.4432 |

Therefore, five clusters were selected for the final model.

### 5. K-Means Clustering

The final K-Means model was trained using:

- Number of clusters: 5
- Random state: 42
- Number of initializations: 10

The model successfully segmented all 200 customers.

## Customer Segmentation Results

Five customer segments were identified.

| Cluster | Customers | Income | Spending |
|---|---:|---:|---:|
| 0 | 81 | 55.30k | 49.52 |
| 1 | 39 | 86.54k | 82.13 |
| 2 | 22 | 25.73k | 79.36 |
| 3 | 35 | 88.20k | 17.11 |
| 4 | 23 | 26.30k | 20.91 |

### Customer Segment Interpretation

**Cluster 0 – Standard Customers**

Customers with average income and average spending behaviour. They represent the largest segment, accounting for 40.5% of the dataset.

Suggested strategy: Loyalty programmes and general promotional campaigns.

**Cluster 1 – Premium Customers**

Customers with high annual income and high spending scores.

Suggested strategy: Premium products, exclusive offers and VIP loyalty programmes.

**Cluster 2 – Young Active Spenders**

Customers with lower annual income but high spending scores.

Suggested strategy: Affordable products, discounts and personalized promotions.

**Cluster 3 – Careful High Earners**

Customers with high annual income but relatively low spending scores.

Suggested strategy: Personalized recommendations and targeted marketing campaigns.

**Cluster 4 – Low-Income Low Spenders**

Customers with lower income and lower spending scores.

Suggested strategy: Budget-friendly products and value-based promotions.

These descriptions are business interpretations of the cluster averages rather than confirmed individual customer motivations.

## Model Evaluation

The final K-Means model achieved:

| Metric | Result |
|---|---:|
| Number of clusters | 5 |
| Total customers | 200 |
| Silhouette Score | 0.5547 |
| Inertia | 65.5684 |

The Silhouette Score indicates reasonably well-separated customer segments.

## Visualizations

The project includes:

1. Customer gender distribution.
2. Age, income and spending score distributions.
3. Annual income vs spending score.
4. Customer feature correlation.
5. Elbow Method.
6. Silhouette Score comparison.
7. Final K-Means customer segmentation plot.

## How to Run the Project

### Google Colab

1. Download or clone this repository.
2. Open Google Colab.
3. Upload `Elevvo_Task_2_Customer_Segmentation.ipynb`.
4. Download the dataset from Kaggle.
5. Upload `Mall_Customers.csv` when prompted.
6. Run all notebook cells sequentially.

### Local Environment

Clone the repository:

```bash
git clone https://github.com/YOUR_USERNAME/Elevvo-Task-2-Customer-Segmentation.git
```

Install the dependencies:

```bash
pip install pandas numpy matplotlib scikit-learn jupyter
```

Launch Jupyter:

```bash
jupyter notebook
```

## Repository Structure

```text
Elevvo-Task-2-Customer-Segmentation/
│
├── Elevvo_Task_2_Customer_Segmentation.ipynb
├── README.md
├── requirements.txt
├── Customer_Segmentation_Results.csv
│
└── images/
    ├── gender_distribution.png
    ├── feature_distributions.png
    ├── income_vs_spending.png
    ├── correlation_matrix.png
    ├── elbow_method.png
    ├── silhouette_scores.png
    └── final_customer_clusters.png
```

## Future Improvements

- Experiment with DBSCAN clustering.
- Compare alternative clustering algorithms.
- Investigate customer age and gender within each segment.
- Explore additional customer behaviour variables.
- Develop more detailed customer marketing strategies.

## Internship Information

**Organization:** Elevvo

**Program:** Machine Learning Internship

**Track:** Machine Learning

**Task:** Task 2 – Customer Segmentation

**Environment:** Google Colab

## Author

**Stewart Daniel**

MSc Applied Informatics  
Vytautas Magnus University, Lithuania

Interested in Artificial Intelligence, Machine Learning, Natural Language Processing and Data Science.

#MachineLearning #Python #KMeans #CustomerSegmentation #DataScience #Elevvo
