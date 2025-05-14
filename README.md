# E-Commerce Customer Review Prediction (Nile Project)

This project was developed by group 28 as part of the "Analytics in Practice" module for the MSc Business Analytics program at the University of Warwick. It involves building a machine learning model to predict which customers are likely to leave **positive reviews** on a fictional South American e-commerce platform named **Nile**, based on behavioral and transactional data.

---

## Objective

To assist Nile in improving customer satisfaction strategies by identifying likely promoters and minimizing wasted marketing resources on unlikely reviewers.

---

## Methodology

We followed the **CRISP-DM** process to guide our data science workflow:

- **Business Understanding**: Define key drivers behind positive reviews
- **Data Understanding**: Evaluate dataset coverage and gaps
- **Data Preparation**: Clean, merge, and engineer key features
- **Modeling**: Compare XGBDT, GBDT, and Random Forest
- **Evaluation**: Use Precision, Recall, and F1-score to assess performance
- **Deployment**: Recommend actionable insights for marketing and logistics

---

## Data

The data was sourced from the [Brazilian E-Commerce Public Dataset](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce). Due to licensing, we do not share the original dataset. However, the script demonstrates the merging, cleaning, and transformation process.

---

## Key Features Engineered

- `total_price` (item + freight)
- `delivery_time` and `early_late_delivery`
- Aggregated scores for category, seller, and customer state
- `reviews` converted to binary: 1 (positive) if 4–5 stars, else 0

---

## Models Compared

| Model          | Precision | Recall | F1 Score |
|----------------|-----------|--------|----------|
| Random Forest  | 0.99      | 0.99   | 0.99     |
| GBDT           | 0.814     | 0.611  | 0.63     |
| **XGBDT**      | **0.906** | **0.716** | **0.762** |

XGBDT was chosen for its balance between **precision and generalization**, avoiding overfitting while outperforming GBDT in all key metrics.


