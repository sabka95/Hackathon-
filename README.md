# 🎬 Hackathon Project: Streaming Platforms Movie Analysis

## 📌 Objective
This project focuses on analyzing movies and series across multiple streaming platforms. The goal is to clean the dataset, enrich it with missing information (such as genres), and extract insights about content distribution, ratings, and trends.

## 📁 Dataset Description
The dataset used combines information on titles available on platforms like Netflix, Hulu, Prime Video, and Disney+. Key columns include:
- **Title**: The name of the movie or show
- **Year**: Release year
- **Age**: Target audience age group
- **Ratings**: Rotten Tomatoes scores
- **Platform availability**
- **Genre**: Added through web scraping

## 🧹 Data Cleaning & Enrichment
- Added a new column in each dataset to distinguish between movies and series.
- Concatenated both datasets to unify the data.
- Used web scraping to retrieve the **genre**, which was missing from both datasets.
- Converted the genre column from string/object type to proper lists.
- Removed rows where genre was missing and dropped irrelevant or empty columns.
- Normalized Rotten Tomatoes ratings for further use.
- Applied **label encoding** to text columns and **one-hot encoding** to genres.

## 📊 Analysis & Visualizations
- Generated a **correlation matrix** to identify potential dependencies between features.
  - Most correlations were weak, except between related genres (e.g., Fantasy & Adventure).
  - Streaming platforms showed mostly exclusive content (negative correlation).
- Filtered high-rated content (score ≥ 0.8) and analyzed the most common genres.
  - Drama, Comedy, Adventure, and Action were the most frequent among top-rated titles.

## ✅ Key Findings
- **Drama** is the most prevalent genre among high-rated content.
- **Comedy**, **Adventure**, and **Action** follow closely.
- Family-oriented content tends to receive better ratings.
- Most platforms do not share content extensively.

## 🚀 Future Work
- Explore non-linear models (e.g., clustering, recommendation systems).
- Analyze platform-specific genre preferences.
- Extend the dataset with viewer statistics or country-level metadata.

