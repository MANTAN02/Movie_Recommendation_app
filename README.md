This project is a movie recommendation system that leverages user demographics (age and gender) to provide personalized movie suggestions. It uses several data science principles to generate relevant recommendations.
Data Science Concepts Used

Demographic Filtering:

The system uses demographic data (age and gender) to create tailored recommendations
Age-specific preferences are coded into different categories (kids, teens, young adults, middle-aged, seniors)
Gender-based preferences are encoded into genre preferences


Content-Based Filtering:

Recommendations are generated based on movie attributes (genres) rather than user ratings
This is a form of content-based recommendation that matches movie attributes to user preferences


Similarity Calculation:

The calculateSimilarity() function implements a cosine similarity-like metric
It measures overlap between user genre preferences and movie genres
The formula divides the intersection size by the square root of the product of set sizes


Hybrid Recommendation Approach:

The system combines demographic filtering with content-based recommendations
It implements special case handling for different demographics (e.g., kids get cartoon content, young adults get romance movies)
Different age groups receive customized genre weightings


Data Segmentation:

Movies are segmented by audience appropriateness (kids vs adult content)
Age brackets are used to create targeted recommendation pools


Ranking Algorithm:

Movies are scored based on similarity to user preferences
Results are sorted to present most relevant recommendations first
A limit parameter controls the number of recommendations returned
