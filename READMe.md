# Hybrid Recommendation System

This project implements a hybrid recommendation system to suggest the top 3 posts for each user based on user profile information, past engagement data, and post attributes.

## Project Structure

The project is implemented as a Colab notebook. The key components are:

1.  **Data Loading and Exploration**: Loading the user, post, and engagement data from CSV files and performing initial data validation and exploration.
2.  **Data Preprocessing and Feature Engineering**: Cleaning the data, extracting relevant features (like interests and tags), and creating interaction features (like positive engagement counts).
3.  **Content-Based Filtering**: Building a content-based component using TF-IDF on post tags and calculating cosine similarity between posts.
4.  **Collaborative Filtering**: Creating a user-item interaction matrix from the engagement data.
5.  **Hybrid Recommendation System**: Combining the content-based and collaborative filtering approaches using a weighted sum of scores.
6.  **Recommendation Generation**: Generating the top 3 post recommendations for each user based on the hybrid scores.
7.  **Evaluation**: Evaluating the performance of the recommendation system using metrics like Precision@k, Recall@k, and Mean Average Precision (MAP).
## Approach

The recommendation system employs a hybrid approach combining:

*   **Content-Based Filtering**: Leverages the similarity of post tags using TF-IDF and cosine similarity.
*   **Collaborative Filtering**: Utilizes user-item engagement patterns from the historical data.

A weighted sum is used to combine the scores from both components, allowing for tuning the influence of each method.

## Evaluation

The performance of the recommendation system is evaluated using standard top-N recommendation metrics:

*   **Precision@k**: Measures the accuracy of the top `k` recommendations.
*   **Recall@k**: Measures the coverage of relevant items within the top `k` recommendations.
*   **Mean Average Precision (MAP)**: A ranking-aware metric that considers the order of relevant items.

For this project, `k=3` was used, and positive engagements (`engagement == 1`) were considered the ground truth for relevance.

## Results


✅ Top 3 Post Recommendations for Each User:
User U1: ['P57', 'P48', 'P23']
User U2: ['P5', 'P69', 'P17']
User U3: ['P26', 'P35', 'P7']
User U4: ['P3', 'P34', 'P97']
User U5: ['P22', 'P78', 'P48']
User U6: ['P57', 'P48', 'P1']
User U7: ['P71', 'P76', 'P36']
User U8: ['P4', 'P99', 'P33']
User U9: ['P56', 'P30', 'P52']
User U10: ['P1', 'P17', 'P58']
User U11: ['P57', 'P48', 'P23']
User U12: ['P70', 'P92', 'P5']
User U13: ['P23', 'P14', 'P54']
User U14: ['P1', 'P17', 'P58']
User U15: ['P14', 'P63', 'P54']
User U16: ['P30', 'P29', 'P60']
User U17: ['P36', 'P11', 'P77']
User U18: ['P3', 'P34', 'P97']
User U19: ['P23', 'P76', 'P71']
User U20: ['P37', 'P43', 'P49']
User U21: ['P2', 'P76', 'P71']
User U22: ['P14', 'P63', 'P54']
User U23: ['P1', 'P17', 'P58']
User U24: ['P36', 'P11', 'P77']
User U25: ['P56', 'P30', 'P52']
User U26: ['P81', 'P40', 'P72']
User U27: ['P57', 'P48', 'P30']
User U28: ['P56', 'P1', 'P46']
User U29: ['P14', 'P63', 'P54']
User U30: ['P31', 'P27', 'P32']
User U31: ['P30', 'P29', 'P60']
User U32: ['P22', 'P78', 'P28']
User U33: ['P72', 'P40', 'P81']
User U34: ['P26', 'P35', 'P7']
User U35: ['P1', 'P17', 'P58']
User U36: ['P22', 'P78', 'P48']
User U37: ['P2', 'P80', 'P30']
User U38: ['P57', 'P48', 'P22']
User U39: ['P92', 'P70', 'P56']
User U40: ['P57', 'P48', 'P23']
User U41: ['P37', 'P14', 'P54']
User U42: ['P57', 'P48', 'P36']
User U43: ['P1', 'P17', 'P58']
User U44: ['P37', 'P30', 'P52']
User U45: ['P21', 'P61', 'P66']
User U46: ['P53', 'P41', 'P74']
User U47: ['P57', 'P48', 'P3']
User U48: ['P36', 'P11', 'P77']
User U49: ['P3', 'P34', 'P97']
User U50: ['P74', 'P26', 'P7']

The notebook outputs the top 3 recommendations for each user and the calculated evaluation metrics (Average Precision@3, Average Recall@3, and MAP).

**Mean Average Precision (MAP):** 0.0370

**Average Precision@3**: 0.1733
**Average Recall@3**: 0.0511

## Potential Extensions

Several potential extensions could be explored to improve the recommendation system:

*   Incorporating more features (user demographics, content type, time of engagement, creator info).
*   Exploring advanced collaborative filtering techniques (Matrix Factorization, Deep Learning models).
*   Implementing different hybrid strategies (weighted ranking, switching, model-based).
*   Addressing the cold start problem for new users and items.
*   Conducting online evaluation (A/B testing).
*   Adding explainability to the recommendations.

## Dependencies

The project requires the following Python libraries:

*   pandas
*   numpy
*   sklearn
*   scipy
*   matplotlib
*   seaborn

These dependencies can typically be installed using pip:
