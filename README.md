# **Project 4: Building a Content-Based Movie Recommendation System**

Tye Elliott

Kacy Samples

Mallorie Daubenspeck

Jonathan Gutierrez-Lozano 

Kirby Smith

# **Project Description**

## **Objective:**
Develop a recommendation system that suggests movies based on their metadata (genres, keywords, taglines, etc.) by employing a content-based filtering approach.


## Data Preparation and Cleaning:
Datasets Used: movies_metadata.csv, credits.csv, keywords.csv, each containing various pieces of information about movies.
Loading Data: Read CSV files into pandas DataFrames, ensuring id columns are treated as strings for consistent merging.
Data Cleaning:Drop unnecessary columns from movies_metadata.csv to simplify the dataset.
Convert numeric columns to appropriate data types and date columns to datetime.
Clean id columns across datasets, converting them to integers for consistency.
Merging Datasets:Merge movies_metadata.csv, credits.csv, and keywords.csv on the id column using inner joins to ensure data integrity.
Further clean the merged dataset by removing rows with missing or irrelevant information.


## **Feature Engineering:**
Text Features Aggregation: Aggregate text features from overview, genres, keywords, cast, and crew columns into a single combined_features column by concatenating text data.
TF-IDF Vectorization: Convert combined_features into numerical vectors using TF-IDF vectorization to quantify the importance of words in the movie descriptions.
Dimensionality Reduction: Apply Truncated SVD to the TF-IDF matrix to reduce its dimensionality, preparing it for similarity computation.


## **Similarity Computation:**
Calculate the cosine similarity between movies based on the reduced TF-IDF matrix to identify how similar they are to each other based on their metadata.


## **Recommendation Function:**
Define a function get_recommendations that fetches and displays the top 10 movies most similar to a given movie title, leveraging the computed cosine similarity scores.


## **Interactive User Input:**
Implement a dropdown menu using ipywidgets for selecting a movie title, enhancing the user experience by providing automatic recommendations for the chosen movie.


## **Challenges and Solutions:**
Addressed specific errors encountered during data merging by ensuring consistent data types and provided solutions for improving user interaction with the system.


## **Testing and Evaluation:**
Programmatically select a diverse set of test movies to generate and evaluate recommendations, assessing the effectiveness of the recommendation system.


## **Key Considerations:**
Data Consistency: Ensure id fields are consistent and of the same data type across all files for accurate merging.
Merging Strategy: Use inner joins to merge datasets based on id to ensure completeness and relevance of the records in the final dataset.
Saving Processed Data: Save the cleaned and merged dataset into a new CSV file for ease of access in future analysis or modeling efforts.


This comprehensive approach encapsulates the entire pipeline from data preparation to feature engineering, similarity computation, and finally, the deployment of an interactive content-based movie recommendation system. This structured process ensures the development of an effective and user-friendly recommendation system leveraging movie metadata.

## **Table of Contents**
Code utilized for this analysis can be found in the file titled "pythonANDbeyond_Project4.ipynb" within the main branch on our GitHub "Project4" repo. Data visualizations can be found in the "Graph_PNGS" directory. Data utilized for this analysis can be found in the files titled "movies_metadata.csv", "credits.csv", and "keywords.csv" within the "Data" directory. Our presentation slides, titled "Content Based Movie Recommendation System", can be located within the main branch of the repo.

## **Installation Instructions**
Code utilized for this analysis can be found in the file titled "pythonANDbeyond_Project4.ipynb" within the main branch on our GitHub "Project4" repo.

## **Usage**
Can Git Clone all files from the 'Project4' repo.

## **Credits**
For this analysis we utilized Google, Canva, Tableau, ChatGPT, course TA's, fellow students, Stack Overflow, and educational resources provided by UT's Data Analytics Bootcamp.

## **License**
License data for this analysis came from "The Movie Database (TMDB)" via Kaggle.com.
