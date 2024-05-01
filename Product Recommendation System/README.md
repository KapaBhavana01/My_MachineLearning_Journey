# E-commerce Product Recommendation System
This project implements a product recommendation system for e-commerce businesses to help improve customer experience and drive sales.

## 1. Popularity and Collaborative Filtering Recommendations
For customers with previous purchase history, recommendations are generated using a the below two approach:

- Popularity Based Recommendations: The most popular products based on overall sales are shown first to leverage the long tail effect.

- Collaborative Filtering: A utility matrix is constructed from purchase histories. Products are then recommended based on similarity between the target customer's previous purchases and those of other customers.

This leverages both overall product popularity and individualized recommendations.

### Dataset : [Amazon Ratings Dataset](https://www.kaggle.com/datasets/skillsmuggler/amazon-ratings)

## 2. Text Clustering Based Recommendations (Cold Start Recommendation)
This recommendation approach is well-suited for businesses setting up their e-commerce website initially without any user purchase history data. It helps provide relevant product recommendations to new customers from the start.

The system works as follows:

- When a new customer visits without a purchase history, their search terms are used to identify the closest matching product cluster based on text clustering of descriptions.

- The top products from that identified cluster are then surface as recommendations to the customer.

This helps deliver an initial set of personalized recommendations. As purchase history for customers is subsequently collected, the model-based collaborative filtering approach can then be utilized to generate even more customized recommendations based on similarities to other user purchase patterns.
