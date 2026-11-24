# E-Commerce Customer Behavior Analysis and Prediction

## Project Overview

This project focuses on analyzing and predicting customer behavior in an online store using Python and Machine Learning techniques.

The main objective is to explore customer interactions with products and develop predictive models to determine whether a customer session will result in a purchase.

The project is developed as part of the Machine Learning course at the University of Craiova.

## Dataset

**Source:** [eCommerce behavior data from multi category store – Kaggle](https://www.kaggle.com/datasets/mkechinov/ecommerce-behavior-data-from-multi-category-store)

The data used in this project contains customer interactions recorded during October and November 2019.

It includes 9 columns:

- `event_time` – date and time of the interaction
- `event_type` – view, cart or purchase
- `product_id` – product identifier
- `category_id` – product category identifier
- `category_code` – product category description
- `brand` – product brand
- `price` – product price
- `user_id` – user identifier
- `user_session` – browsing session identifier

For the exploratory analysis, a working sample of **100,000 events** was created using 50,000 records from each month.

## Technologies

- Python
- Pandas
- NumPy
- Matplotlib
- Scikit-learn
- Kaggle Notebooks
- Weights & Biases
- GitHub

## Current Progress

### S2 – Topic and Dataset Selection

Selected the project topic, identified the dataset and described the main objectives.

### S4 – Exploratory Data Analysis (EDA)

Completed the initial data exploration, including:

- Dataset structure and missing-value analysis
- Distribution of customer interaction types
- Data visualizations
- Comparison between estimates from a smaller sample and actual counts

**Event distribution in the 100,000-record sample:**

| Event Type | Count |
|---|---:|
| View | 95,045 |
| Cart | 3,372 |
| Purchase | 1,583 |

Product views are considerably more frequent than cart additions and purchases.

### S6 – First Machine Learning Model

Developed the first Machine Learning model using **Logistic Regression** to predict whether a customer session would result in a purchase.

The dataset was prepared at session level, with **47,646 examples**, divided into 38,116 training examples (80%) and 9,530 testing examples (20%).

The model used features related to the session start time and the first product viewed. It was trained using `class_weight="balanced"` to account for the imbalance between purchase and non-purchase sessions.

**Model evaluation:**

- Accuracy: 40.41%
- Precision: 6.81%
- Recall: 64.77%
- F1-score: 12.32%

The model identified approximately 65% of the sessions containing purchases, but it also produced many false positive predictions. These results provided a baseline for further improvements.

The experiment was recorded in Weights & Biases under the name `S6-Primul-Model`.

### S9 – Model Improvements and Performance Comparison

In this stage, the initial approach was improved by introducing additional features, preprocessing the data and evaluating multiple classification algorithms.

Three Machine Learning models were evaluated:

- Logistic Regression
- Decision Tree
- Random Forest

The results were compared with the baseline model developed in S6.

**Model performance comparison:**

| Model | Accuracy | Precision | Recall | F1-score |
|---|---:|---:|---:|---:|
| Logistic Regression (S6) | 40.41% | 6.81% | 64.77% | 12.32% |
| Logistic Regression (S9) | 59.07% | 9.25% | 60.55% | 16.05% |
| Decision Tree (S9) | 66.75% | 9.39% | 47.89% | 15.70% |
| Random Forest (S9) | 75.63% | 11.05% | 39.29% | 17.25% |

Random Forest achieved the highest accuracy, precision and F1-score among the evaluated models.

Compared with the initial S6 model, Random Forest improved accuracy by 35.22 percentage points and F1-score by 4.93 percentage points.

However, recall decreased, and precision remains relatively low. The class imbalance continues to represent an important challenge for purchase prediction.

The notebook includes graphical comparisons of model performance and experiment tracking using Weights & Biases.

## Project Files

- **Project documentation (PDF):** Documentation of the completed project stages.
- **`ecommerce_eda_invatare-automata.ipynb`:** Python notebook containing exploratory data analysis, model implementation, evaluation and performance comparisons for S6 and S9.
- **README.md:** Project overview, methodology, progress and results.

## Project Resources

- [Kaggle Dataset](https://www.kaggle.com/datasets/mkechinov/ecommerce-behavior-data-from-multi-category-store)
- [Kaggle Notebook](https://www.kaggle.com/code/teodorasarahpeanc/ecommerce-eda-invatare-automata)
- [Weights & Biases Project](https://wandb.ai/teodorapeanca-university-of-craiova/ECommerce-Customer-Behavior-ML)
- [S6 Experiment](https://wandb.ai/teodorapeanca-university-of-craiova/ECommerce-Customer-Behavior-ML/runs/8js4w5y8)

## Project Status

- [x] S2 – Topic and Dataset Selection
- [x] S4 – Exploratory Data Analysis
- [x] S6 – First Machine Learning Model
- [x] S9 – Model Improvements and Performance Comparison
- [ ] S12 – Final Version

## Next Steps

### S12 – Final Version

- Complete the final model evaluation.
- Analyze model limitations and possible improvements.
- Summarize and interpret the experimental results.
- Complete the final project documentation.

The repository will be updated as the project progresses.
