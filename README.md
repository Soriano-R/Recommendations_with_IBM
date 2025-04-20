# Recommendations with IBM

## Project Overview
This project analyzes user interactions with articles on the IBM Watson Studio platform and makes recommendations about new articles users might like.

## Dataset
The project uses two main datasets:
- user-item-interactions.csv: Contains user interactions with articles
- articles_community.csv: Contains information about the articles

## Implementation
The recommendation system implements several techniques:
1. Rank-based recommendations
2. User-user collaborative filtering
3. Content-based recommendations
4. Matrix factorization

## Files
- Recommendations_with_IBM.ipynb: Main notebook with all code and analysis
- project_tests.py: Unit tests for the implementation
- data/: Directory containing the datasets
- top_*.p: Pickle files with ranked article information
- user_item_matrix.p: User-item interaction matrix

## Requirements
- Python 3.x
- Pandas
- NumPy
- Matplotlib
- Scikit-learn
