# IBM Recommendations Project

This project focuses on analyzing user interactions with articles on the IBM Watson Studio platform and making recommendations to users about new articles they might like.

## Table of Contents

1. [Exploratory Data Analysis](#exploratory-data-analysis)
2. [Rank Based Recommendations](#rank-based-recommendations)
3. [User-User Based Collaborative Filtering](#user-user-based-collaborative-filtering)
4. [Matrix Factorization](#matrix-factorization)
5. [Conclusion](#conclusion)

## Exploratory Data Analysis

In this section, we perform exploratory data analysis on the IBM Watson Studio platform datasets. Key findings include:
- The distribution of user-article interactions follows a long-tail pattern, with most users interacting with very few articles.
- There are 45,993 total user-article interactions.
- The most viewed article had 937 interactions.

## Rank Based Recommendations

Here, we implement a simple rank-based recommendation system. This recommends the most popular articles to all users, regardless of their individual preferences. The top 10 most popular articles are identified.

## User-User Based Collaborative Filtering

In this section, we build a collaborative filtering model for making recommendations. The key steps are:
1. Create a user-item matrix 
2. Compute similarity between users 
3. Recommend articles based on similar users

Challenges with this approach include the "cold start" problem, where recommendations cannot be made for users with no prior interactions.

## Matrix Factorization

Lastly, we use matrix factorization to make article recommendations to users. We perform SVD on the user-item matrix, and use the resulting matrices to predict unknown entries (potential recommendations).

Key findings:
- A greater number of latent features results in a higher accuracy on the training data, but lower accuracy on the test data, suggesting overfitting.
- Only 20 users could be used for testing due to the small dataset and the cold start problem.

To verify if the recommendations are an improvement over the current system, an A/B test measuring user engagement could be conducted.

## Conclusion

This project implemented and evaluated several methods for making article recommendations to users on the IBM Watson Studio platform. Rank-based recommendations, user-user collaborative filtering, and matrix factorization were explored. Challenges such as the "cold start" problem were encountered. Further work could include deploying the model and conducting A/B tests to measure its effectiveness.