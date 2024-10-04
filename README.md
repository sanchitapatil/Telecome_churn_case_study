# Telecom Customer Churn Prediction

## Overview

This project aims to predict customer churn in a telecom company using machine learning models. Customer churn refers to customers discontinuing the use of a company's services, and predicting churn is crucial for retention strategies. By identifying high-risk customers, telecom companies can proactively offer tailored incentives to retain them.

The project also identifies key factors influencing churn behavior, allowing businesses to understand the drivers behind customer loss. These insights help in the design of targeted retention strategies and engagement efforts.

## Objectives

- **Predict Customer Churn**: Build machine learning models to predict whether a high-value customer will churn in the near future.
- **Identify Key Drivers**: Determine the important features that strongly predict churn, helping to understand the reasons why customers leave.
- **Model Evaluation**: Use various evaluation metrics (accuracy, precision, recall, F1 score, ROC AUC) to assess model performance, with a focus on identifying actual churners (recall) for business-driven retention efforts.
  
## Business Relevance

The model predictions can be used by the telecom company to:
- Offer targeted discounts or plans to prevent churn.
- Identify customer behavior patterns leading to churn.
- Improve product features or communication to enhance customer satisfaction.

## Dataset

The dataset is split into training and test datasets. The data includes customer behavior and usage statistics over a period of time, with features such as:
- Number of minutes used (on-net/off-net, local/roaming)
- Number of recharges and data usage
- Activity indicators like Facebook usage, night pack usage, and roaming details

These features will be used to predict churn and identify key variables.

## Models Used

1. **Random Forest**: A robust ensemble method that averages multiple decision trees to improve prediction accuracy and interpretability.
2. **Gradient Boosting Machine (GBM)**: A powerful ensemble method that sequentially builds trees to correct errors from previous trees, focusing on minimizing the error.

## Key Features for Churn Prediction

The following are some of the top features identified by the models that strongly predict churn:

| Feature                             | Description                                              |
|-------------------------------------|----------------------------------------------------------|
| `fb_user_8_1.0`                     | Indicates if the customer is a Facebook user in the 8th month. |
| `offnet_mou_8`                      | Total minutes of use for off-net calls in the 8th month.   |
| `roam_og_mou_8`                     | Outgoing roaming call minutes in the 8th month.            |
| `days_since_last_rech_8`            | Days since the last recharge in the 8th month.             |
| `total_rech_data_group_8_No_Recharge`| Indicates no data recharge in the 8th month.              |

## Evaluation Metrics

To ensure model effectiveness, the following metrics are used:

- **Accuracy**: Measures the overall correctness of predictions.
- **Precision**: Focuses on how many of the predicted churn cases are actual churners.
- **Recall**: Captures how many of the actual churners were correctly predicted. This is important as missing out on a churner can be costly.
- **F1 Score**: Balances precision and recall.
- **ROC AUC**: Measures the model's ability to distinguish between churners and non-churners.

**Business Focus**: Recall is prioritized to ensure that most actual churners are captured and proactive measures can be taken to retain them.

## Strategies for Churn Management

Based on the analysis and model outputs, the following strategies are recommended to manage customer churn:

1. **Targeted Discounts & Offers**: Use features like `fb_user_8_1.0` and `offnet_mou_8` to identify at-risk customers and provide them with special discounts or plans.
2. **Engagement Campaigns**: Customers who haven't recharged recently (`days_since_last_rech_8`) or frequently use roaming (`roam_og_mou_8`) are likely to churn. Engage them with personalized communication.
3. **Product Customization**: Improve or introduce new plans based on customer behavior like `night_pck_user_8_-1.0` and `total_rech_data_group_8_No_Recharge`.
4. **Improve Communication**: Use customer segmentation to tailor communication and retention efforts for different user groups.

## How to Run the Project

1. Clone the repository:
   ```bash
   git clone https://github.com/sanchitapatil/telecom-churn-prediction.git
