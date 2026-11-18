
# Customer Segmentation Using K-Means and DBSCAN

## Project Overview

Developed as part of the Elevvo Machine Learning Internship.

This project applies unsupervised machine learning to segment
200 mall customers based on annual income and spending score.

## Dataset

Mall Customer Segmentation Dataset

Source:
https://www.kaggle.com/datasets/vjchoudhary7/customer-segmentation-tutorial-in-python

- Records: 200
- Features: 5
- Missing values: 0
- Duplicate records: 0

## Technologies

- Python
- Pandas
- NumPy
- Matplotlib
- Scikit-learn
- Google Colab

## Methodology

1. Data loading and inspection
2. Exploratory Data Analysis
3. Feature selection
4. StandardScaler
5. Elbow Method
6. Silhouette Score
7. K-Means clustering
8. DBSCAN clustering
9. DBSCAN parameter tuning
10. Customer spending analysis

## K-Means Results

- Clusters: 5
- Customers: 200
- Silhouette Score: 0.5547
- Inertia: 65.5684

### Customer Segments

| Cluster | Customers | Income | Spending |
|---|---:|---:|---:|
| 0 | 81 | 55.30 | 49.52 |
| 1 | 39 | 86.54 | 82.13 |
| 2 | 22 | 25.73 | 79.36 |
| 3 | 35 | 88.20 | 17.11 |
| 4 | 23 | 26.30 | 20.91 |

## DBSCAN Results

Initial configuration:
- EPS: 0.3
- Min Samples: 5
- Clusters: 7
- Noise points: 35
- Silhouette Score excluding noise: 0.5243

Tuned configuration:
- EPS: 0.4
- Min Samples: 5
- Clusters: 4
- Noise points: 15

The tuned configuration provides a useful alternative with
fewer noise points. DBSCAN and K-Means scores are not
directly comparable because the DBSCAN score excludes noise.

## Parameter Optimization

DBSCAN parameters were tested using multiple combinations
of epsilon and minimum samples.

The highest observed silhouette score was 0.6452 at
EPS 0.3 and Min Samples 7, with 72 noise observations.

## Average Spending Analysis

Cluster 1 had the highest average spending score (82.13),
followed by Cluster 2 (79.36).

Cluster 3 had the lowest average spending score (17.11).

## Visualizations

See the images folder for all project visualizations.

## How to Run

1. Open Google Colab.
2. Upload the project notebook.
3. Download the dataset from Kaggle.
4. Upload Mall_Customers.csv.
5. Run notebook cells sequentially.

Install dependencies:

pip install -r requirements.txt

## Author

Stewart Daniel
MSc Applied Informatics
Vytautas Magnus University, Lithuania

## Internship

Elevvo - Machine Learning Track
Task 2 - Customer Segmentation

#MachineLearning #Python #KMeans #DBSCAN
#CustomerSegmentation #DataScience #Elevvo
