# E-Commerce Customer Behavior Analysis and Prediction

## Project Overview

This project focuses on analyzing customer behavior in an online store using Python and Machine Learning techniques.

The main objective is to explore customer interactions with products and, in later stages, develop predictive models to better understand purchasing behavior.

The project is developed as part of the Machine Learning course at the University of Craiova.

## Dataset

**Source:** [eCommerce behavior data from multi category store – Kaggle](https://www.kaggle.com/datasets/mkechinov/ecommerce-behavior-data-from-multi-category-store)

The original dataset contains customer interactions recorded during October and November 2019.

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
- Kaggle Notebooks
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

## Project Files

- **Project documentation (PDF):** Contains the completed S2 and S4 stages.
- **`ecommerce-eda-invatare-automata.ipynb`:** Python notebook containing the exploratory analysis.

[View the Kaggle Notebook](https://www.kaggle.com/code/teodorasarahpeanc/ecommerce-eda-invatare-automata)

## Next Steps

- **S6 – Version 1:** Implement the first Machine Learning model.
- **S9 – Version 2:** Improve the approach and compare model performance.
- **S12 – Final Version:** Complete the project, evaluate the results and prepare the final documentation.

The repository will be updated as the project progresses.
