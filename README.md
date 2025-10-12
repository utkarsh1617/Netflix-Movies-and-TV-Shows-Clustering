# Netflix Movies and TV Shows Clustering

## Project Overview

This project uses unsupervised machine learning to segment the Netflix content library into distinct clusters based on features like genre, rating, and duration. The goal is to uncover meaningful patterns in the data that can be used to improve content recommendations, identify niche categories, and understand market trends.

## Project Workflow

1.  **Data Cleaning:** Handled missing values in `director`, `cast`, and `country` columns, and corrected data type errors.
2.  **Feature Engineering:** Created new features like `content_age` from `release_year` and processed the `duration` column into separate numerical features for movies (`duration_min`) and TV shows (`duration_seasons`).
3.  **Data Preprocessing:** Converted categorical features (genre, rating) into a numerical format using TF-IDF Vectorization and One-Hot Encoding. Scaled all numerical features using StandardScaler.
4.  **Modeling:** Applied K-Means clustering, determining the optimal number of clusters (k=3) using the Elbow Method.
5.  **Evaluation:** Assessed model performance with the Silhouette Score and Davies-Bouldin Index. Validated results with Hierarchical Clustering.
6.  **Visualization:** Used PCA and t-SNE to visualize the resulting clusters in 2D space.

## Key Findings

The analysis successfully segmented the Netflix library into three stable and meaningful clusters:

* **Cluster 0: The Modern Movie Collection:** The largest cluster, consisting of recent movies with an average runtime of 98 minutes.
* **Cluster 1: The TV Show Universe:** A large cluster composed entirely of TV shows, typically with 1-2 seasons.
* **Cluster 2: The Classic Film Library:** A small, niche cluster of older movies (average age of ~38 years) with a longer runtime.

Both K-Means and Hierarchical Clustering models produced a strong **Silhouette Score of 0.3530**, confirming the validity of these groupings.

## Technologies Used

* Python
* Pandas
* NumPy
* Scikit-learn
* Matplotlib
* Seaborn
* Jupyter Notebook

## Repository Contents

* `NetflixDataetl.ipynb`: The complete Jupyter Notebook with the Python code for the entire analysis.
* `processed_netflix_data_with_clusters.csv`: The final, cleaned dataset with an added 'cluster' column.
* `Netflixdocu.pdf`: The final project report documenting the approach, findings, and business implications.
## How to Use

To explore this project, you can review the `NetflixDataetl.ipynb` notebook to see the code and analysis, and read the `Netflixdocu.pdf` for a comprehensive summary of the project's findings.
