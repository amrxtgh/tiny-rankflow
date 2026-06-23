# tiny-rankflow

https://grouplens.org/datasets/movielens/1m/

# "How can we systematically combine and enhance classical recommendation models to achieve state-of-the-art performance on this specific dataset, without using deep learning?"

look up to this

- data sparsity checking
- rating bias
- long tail problem

- EDA
- preprocessing
- Train/Test split
- Classical Models
- Evaluation - RMSE, MAE, Precision@K
- Compare accross models

# Global Popularity
# CatPop (Category Popularity)
# UserCF
# ItemCF
# ExplicitMF(SVD)
# ImplicitMF(ALS)
# Content Based Filtering(CBF)

# ItemCF narrows the millions of items into the few hundreds

# For the ranking we can use the gradient boosted decision trees (GBDT) also known as LambdaMART in the market

# What i think i am going to do

# implement collaborative filtering with content based filtering that uses item metadata and user demographics

# GloVe or BERT for creating rich representing of product text

# Exploring sentiment analysis

# k-core filtering
- Keep only users who rated at least 20 movies
- Keep only movies who got at least 20 reviews
- Removes everything else

# Temporal Split
- Instead of the random 80/20 split we split by time the older data trains and newer data tests

`Raw data(1M ratings)-> K-Core Filtering (removes noise, sparse users/items) -> Clean Dense Data -> Temporal Split(honest train/test split) -> Train Set -> Fit SVD, KNN, NMF Test Set -> Evaluate RMSE, MAE`