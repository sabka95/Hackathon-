# 📘 Hackathon Streaming Analysis Project

## 📝 Project Overview
This notebook explores and analyzes a dataset containing information about movies and series available across different streaming platforms. The main objective is to clean, process, and explore the dataset in order to extract insights such as the most common genres, rating distributions, and correlations between features.

## 📂 Dataset
The dataset contains features such as title, year, rating, availability on platforms (Netflix, Hulu, Prime Video, Disney+), and genre.

## 🔧 Process Summary
## **Étape 1 : Exploration et Premier Diagnostic** **texte en gras**

### 📊 Load Dataset
We read the CSV files that contains information about movies and tv shows on streaming platforms.

We added a column to each DataFrame to specify whether the content is a movie or a series, and then concatenated the two DataFrames.

We have a total of 14 883 movies and tv shows

Using web scraping, we retrieved a missing column from both datasets: the genre of the movie or series. This information was then added to the previously concatenated DataFrame, as it will be useful for future analyses.

# **Étape 2 : Nettoyage et Préparation des Données**

We converted the 'genre' column, which was initially of type object, into a proper list format.

We removed the rows where the genre was not specified, resulting in a final dataset of 11,693 movies.

We removed columns that contained no useful information for our analysis, as well as any remaining null values.

We normalized the Rotten Tomatoes scores to make them suitable for analysis.

We applied label encoding to the textual data and one-hot encoding to the movie genres in order to use a confusion matrix and identify dependencies between features.

The correlation matrix shows weak linear relationships overall. Some related genres like Adventure, Fantasy, and Animation are moderately correlated, and family movies tend to have higher ratings. Platform availability is mostly exclusive, with a slight negative correlation between Netflix and Prime Video. These insights suggest limited linear dependencies.

# **Étape 3 : Analysis**

## **What are the most common genres for top-rated shows and movies across platforms?**

The bar chart and data reveal that among top-rated content (rating ≥ 0.8), the most common genres across platforms are:

Drama (208 titles)

Comedy (137 titles)

Adventure (109 titles)

Action (106 titles)

These genres dominate the top-rated segment, suggesting they are consistently well-received by audiences. Drama, in particular, stands out as the leading genre among highly rated shows and movies

## **How do the release years of shows and movies relate to their average ratings?**

The years between 1950 and 2000 show a stable trend in average ratings, often around 0.55 to 0.60.

The early years of cinema (before 1940) display more variable averages, likely due to a limited number of titles.

Since the 2010s, there has been a slight decline in average ratings, driven by lower scores for both films and series. This may reflect stricter critical standards or a drop in content quality.

## **How does the availability of movies and shows differ across platforms like Netflix, Hulu, and Disney+?**

Netflix clearly leads in terms of the number of available titles.
It is followed by Prime Video and then Hulu.
Disney+ comes last, likely due to its more focused and franchise-driven catalog.

## 📊 Results Highlights
- Drama is the most frequent genre among top-rated titles (rating ≥ 0.8).
- Comedy, Adventure, and Action also appear frequently.
- Genres such as Family and Fantasy tend to receive higher ratings.
- Streaming platforms mostly feature exclusive content (low cross-platform overlap).

## 📌 Notes
- The notebook includes data cleaning, type conversion, genre extraction via web scraping, encoding, and correlation analysis.
- Final output includes a genre-based frequency chart filtered by high ratings.
