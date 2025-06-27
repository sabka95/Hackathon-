
# 🎬 Streaming Platform Content Analysis

## 📌 Project Objective

This project focuses on exploring, cleaning, and analyzing data related to movies and TV shows available on major streaming platforms (Netflix, Prime Video, Hulu, and Disney+). The goal is to uncover trends regarding popular genres, content quality, and distribution across platforms.

---

## 🗂️ Data Overview

Two CSV files, one for movies and one for TV shows, were merged into a single dataset. A column was added to indicate the content type (movie or show) to facilitate comparison.

To enhance the dataset, web scraping was used to retrieve missing genre information for some titles.

---

## 🧹 Data Cleaning & Preprocessing

- Genres were converted into list format for analysis.
- Entries without genre data were removed, reducing the dataset to 11,693 titles.
- Irrelevant and empty columns were dropped.
- Rotten Tomatoes ratings were normalized.
- Textual and categorical data were encoded using label encoding and one-hot encoding.

A correlation matrix was generated to explore relationships between features. A few moderate correlations were observed between related genres, and family-friendly content tended to receive higher ratings. Overall, platform availability showed little overlap.

---

## 📊 Key Analyses

### 🎭 Most Common Genres Among Top-Rated Titles

Among highly rated titles (rating ≥ 0.8), the most frequent genres are:
- **Drama**
- **Comedy**
- **Adventure**
- **Action**

These genres consistently perform well across platforms, with drama leading in both movies and shows.

### 📅 Release Years vs. Ratings

- Average ratings remained fairly stable between 1950 and 2000.
- Early cinema (before 1940) showed more variation due to fewer titles.
- Since the 2010s, there's a slight downward trend in average ratings, possibly due to stricter critiques or content saturation.

### 📺 Content Distribution by Platform

- **Netflix** offers the largest content library.
- **Prime Video** and **Hulu** follow.
- **Disney+** has a smaller catalog, likely due to its franchise-focused model.

---

## 🔧 Technologies and Libraries

- `pandas` for data manipulation  
- `matplotlib` & `seaborn` for visualization  
- `scikit-learn` for data encoding  
- `requests` and `BeautifulSoup` for web scraping
