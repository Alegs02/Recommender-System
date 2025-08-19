# Recommender-System
This project tackles the FIT5212 Recommender System Challenge, using Amazon product review data to build and evaluate different recommendation models. The dataset includes over 200k products with user ratings, votes, and helpfulness scores.

Several approaches were explored:

Alternating Least Squares (ALS): Tested for scalability but performed poorly on explicit rating data.

Singular Value Decomposition (SVD): Tuned with GridSearch, achieving the best RMSE (~0.92) and chosen for the final submission.

Content-Based Filtering (TF-IDF + KNN): Explored product-title similarity but suffered from high runtime and weak results.

XGBoost: Incorporated additional features like helpful votes and product averages, but underperformed compared to SVD.

Key Findings:

Matrix factorization methods (particularly tuned SVD) outperformed other approaches.

Features such as helpful votes and votes provided little value for rating prediction.

Preprocessing experiments (e.g., removing low-vote reviews, weighted rankings) often degraded performance.

The final model used a tuned SVD implementation, balancing accuracy and generalization, and was submitted to the Kaggle competition with strong results
.

Deliverables include the Jupyter notebook with full code, a CSV of predictions, and a detailed analysis report.
