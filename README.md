# MovieLens Feature Engineering & Rating Behaviour Analysis

## Project Overview

This project explores the MovieLens dataset to understand movie rating behaviour, audience preferences, and patterns across different movie characteristics.

The analysis goes beyond basic exploratory analysis by combining multiple datasets, performing feature engineering, and investigating how factors such as movie age, genre, and release period relate to audience ratings.

The goal of this project was to demonstrate a complete data analytics workflow:
- Data preparation
- Feature engineering
- Exploratory Data Analysis
- Pattern discovery
- Insight generation

---

# Objectives

The main objectives of this project were:

- Integrate movie metadata, ratings, and tag information
- Clean and preprocess raw datasets
- Engineer meaningful analytical features
- Analyze rating trends across genres and time periods
- Investigate the relationship between movie characteristics and audience ratings

---

# Dataset Description

The project uses the MovieLens dataset containing:

- Movie information
- User ratings
- Movie genres
- User-generated tags
- Metadata links

The datasets were merged to create a comprehensive analytical dataset containing movie information alongside user rating behaviour.

After merging the datasets, the final analytical dataset contained over **12 million records**, providing a larger-scale environment for exploration and feature analysis.

---

# Tools & Technologies

## Programming & Analysis

- Python
- Pandas
- NumPy

## Data Visualization

- Matplotlib
- Seaborn

## Development Environment

- Jupyter Notebook

---

# Data Preparation & Cleaning

The following preprocessing steps were performed:

- Loaded and inspected multiple MovieLens datasets
- Checked for missing values and duplicate records
- Removed unnecessary columns
- Converted timestamp fields into meaningful date formats
- Merged movie metadata with rating information

---

# Feature Engineering

New analytical features were created to improve understanding of movie behaviour.

### Features Created:

### Release Year
Extracted from movie titles to analyze trends across different periods.

### Number of Genres (`num_genres`)
Calculated the number of genres associated with each movie to understand genre diversity.

### Main Genre (`main_genre`)
Created a simplified genre classification for easier comparison.

### Rating Year (`rating_year`)
Extracted from timestamps to analyze changes in rating behaviour over time.

### Movie Age (`movie_age`)
Calculated the difference between the movie release year and the year it received ratings.

### Classic Movie Classification (`is_classic`)
Movies were categorized as classic movies based on their age to compare audience ratings between older and newer films.

---

# Exploratory Data Analysis

The analysis explored:

## Genre Analysis

- Most common movie genres
- Average ratings across different genres
- Genre popularity patterns

## Time-Based Analysis

- Rating activity trends over the years
- Changes in audience engagement over time

## Movie Age Analysis

- Distribution of movie ages
- Relationship between movie age and ratings
- Comparison between classic and modern movies

---

# Key Insights

The analysis revealed patterns in:

- Genre popularity and audience preferences
- Rating behaviour across different time periods
- The distribution of classic and modern movies
- How movie characteristics influence audience perception

---

# Uncommon Remark

## Movie Age Does Not Necessarily Determine Movie Quality

One interesting observation from this analysis was that a movie's age alone does not appear to be a reliable predictor of audience rating performance.

To investigate this, a new feature called `movie_age` was engineered by calculating the difference between the movie release year and the year ratings were recorded. Movies were also classified as "classic" (`movie_age > 20 years`) to compare rating behaviour between older and newer movies.

**Technical perspective:**

Feature engineering was used to transform raw movie metadata and timestamp information into meaningful analytical variables. The relationship between `movie_age` and ratings was explored to test whether older movies consistently receive different audience ratings compared to newer releases.

**Plain English:**

It is easy to assume that older movies become less valuable or less appreciated with time. However, the analysis suggests that age alone does not determine how viewers rate a movie. A well-received movie can continue to maintain strong audience appreciation many years after its release.

This highlights an important analytical principle:

> A feature is not valuable because it exists in a dataset; it is valuable because it helps answer meaningful questions about real-world behaviour.

---

# Project Structure
