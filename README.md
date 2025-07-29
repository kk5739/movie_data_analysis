# Movie Ratings Analysis: Hypothesis Testing & Machine Learning

This repository contains a comprehensive analysis of a movie ratings dataset. The project is divided into two main parts:

1.  **Hypothesis Testing:** To answer specific questions about movie ratings and viewer demographics.
2.  **Machine Learning:** To build predictive models for movie ratings.

This work was completed as part of two data analysis projects.

---

## 📋 Table of Contents

- [Project Description](#-project-description)
- [Dataset](#-dataset)
- [Part 1: Hypothesis Testing](#-part-1-hypothesis-testing)
  - [Questions Explored](#questions-explored)
  - [Methods](#methods)
  - [Key Findings](#key-findings)
- [Part 2: Machine Learning](#-part-2-machine-learning)
  - [Objectives](#objectives)
  - [Models Used](#models-used)
- [Files in this Repository](#-files-in-this-repository)

---

## 📝 Project Description

This project explores a dataset of 400 movies rated by 1097 participants. The analysis investigates various factors influencing movie ratings, such as movie popularity, release year, and viewer demographics (gender, sibling status, social viewing preferences).

The first part of the project uses statistical hypothesis testing to draw inferences, while the second part applies machine learning techniques to predict movie ratings based on different features.

---

## 💾 Dataset

The dataset contains ratings for 400 movies from 1097 participants. The data includes:

* **Movie Ratings:** Columns 1-400 (Scale: 0-4, with missing values).
* **Sensation Seeking Behaviors:** Columns 401-421 (Scale: 1-5).
* **Personality Questions:** Columns 422-464 (Scale: 1-5).
* **Movie Experience Ratings:** Columns 465-474 (Scale: 1-5).
* **Demographics:**
    * `Gender identity`: Column 475 (1=female, 2=male, 3=self-described).
    * `Only child`: Column 476 (1=yes, 0=no, -1=no response).
    * `Movies are best enjoyed alone`: Column 477 (1=yes, 0=no, -1=no response).

---

## 📊 Part 1: Hypothesis Testing

### Questions Explored

This part of the analysis sought to answer the following questions:

1.  Are more popular movies (i.e., those with more ratings) rated higher?
2.  Are newer movies rated differently than older movies?
3.  Is the enjoyment of 'Shrek (2001)' different between male and female viewers?
4.  What proportion of movies are rated differently by male and female viewers?
5.  Do only children enjoy 'The Lion King (1994)' more than people with siblings?
6.  What proportion of movies show an "only child effect"?
7.  Do social viewers enjoy 'The Wolf of Wall Street (2013)' more than those who watch alone?
8.  What proportion of movies exhibit a "social watching" effect?
9.  Is the ratings distribution of 'Home Alone (1990)' different from 'Finding Nemo (2003)'?
10. How many major movie franchises show inconsistent quality in viewer ratings?

### Methods

* Non-parametric tests like the **Mann-Whitney U test** were used for comparing two groups (due to the ordinal nature of rating data).
* The **Kolmogorov-Smirnov test** was used to compare the rating distributions of two movies.
* The **Kruskal-Wallis test** was used to compare ratings across multiple movies within a franchise.
* A significance level (alpha) of **0.005** was used to reduce the chance of false positives.

### Key Findings

* More popular movies are rated significantly higher than less popular movies.
* There is a significant difference in ratings between older and newer movies.
* No significant gendered difference was found for the enjoyment of 'Shrek (2001)'.
* About 12.5% of movies were rated differently by male and female viewers.
* No significant evidence was found that only children enjoy 'The Lion King (1994)' more than those with siblings.
* Franchises like 'Star Wars', 'The Matrix', and 'Batman' showed significant inconsistencies in quality, while 'Harry Potter' did not.

---

## 🤖 Part 2: Machine Learning

### Objectives

The second part of the project focused on building models to predict movie ratings. This involved:

1.  Using simple linear regression to predict a movie's rating based on the rating of another single movie.
2.  Building multiple regression models by adding demographic predictors (gender, sibship, social viewing).
3.  Implementing regularized regression (Ridge and LASSO) to predict ratings using a subset of other movies as features.
4.  Using logistic regression to classify whether a movie was "enjoyed" (rating above median) or not.

### Models Used

* **Simple and Multiple Linear Regression:** To predict ratings and evaluate the impact of additional predictors.
* **Ridge and LASSO Regression:** To handle potential multicollinearity and for feature selection when predicting ratings from other movies.
* **Logistic Regression:** For binary classification of movie enjoyment.

The machine learning analysis required handling missing data, for which an imputation method (a blend of user and movie average ratings) was suggested.

---

## 📁 Files in this Repository

* `[Report] Intro to Data Science - Project Analysis_.pdf`: A detailed report on the hypothesis testing phase (Part 1).
* `Data analysis project 1 specSheet.pdf`: The specification sheet outlining the requirements for the hypothesis testing project.
* `Data analysis project 2 spec sheet.pdf`: The specification sheet outlining the requirements for the machine learning project.
* `analysis/`: (Assumed) This directory likely contains the Python scripts (`.py` or `.ipynb`) used to perform the analyses described in the reports.
* `movieRatings.db`: (Assumed) A SQLite database that may contain the raw or processed data.
