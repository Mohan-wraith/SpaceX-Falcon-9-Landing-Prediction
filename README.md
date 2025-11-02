# SpaceX Falcon 9 Landing Prediction

![Python](https://img.shields.io/badge/Python-3.9-blue?logo=python)
![Pandas](https://img.shields.io/badge/Pandas-blue?logo=pandas)
![Plotly](https://img.shields.io/badge/Plotly-blue?logo=plotly)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-orange?logo=scikit-learn)

## Project Overview

This is an end-to-end data science capstone project. The goal is to predict the success of a SpaceX Falcon 9 first-stage landing. A successful landing significantly reduces launch costs (from over $160M to $62M), so this model can help a competitor company determine a more accurate bidding price against SpaceX.

The project involves data collection via API and web scraping, data wrangling, exploratory data analysis (EDA), and the creation of an interactive dashboard. Finally, I built and evaluated several machine learning models to find the best-performing classifier for this task.

## Key Features
* **Data Collection Pipeline:** Scraped data from the SpaceX API and Wikipedia.
* **In-Depth EDA:** Analyzed data using SQL, Pandas, Matplotlib, and Seaborn.
* **Interactive Mapping:** Built interactive maps with Folium to visualize launch site success rates.
* **Predictive Dashboard:** Created a fully interactive dashboard with Plotly Dash to explore the relationship between launch variables and success.
* **Machine Learning:** Trained and evaluated 4 classification models, achieving **88.9%** validation accuracy with a Decision Tree.

---

## Interactive Dashboard (Plotly Dash)

The final product is an interactive dashboard where a user can select a launch site and payload range to see the success rates and correlations in real-time.

<p align="center">
  <img width="748" alt="Dashboard Scatter Plot" src="https://user-images.githubusercontent.com/46462603/152729009-c2cdaba4-674c-4103-b540-e77ad3544a99.png">
</p>
<p align="center">
  <img width="692" alt="Dashboard Pie Chart" src="https://user-images.githubusercontent.com/46462603/152729002-f731499b-aab8-46a1-b1c3-583c24ae909e.png">
</p>

---

## Project Workflow

The project is broken down into several notebooks, each covering a specific part of the data science pipeline.

### 1. Data Collection
* **SpaceX API:** Queried the SpaceX REST API to get Falcon 9 launch data. Filtered for Falcon 9 launches, handled missing values, and saved the initial dataset.
    * *Notebook: `1_Data_Collection_API.ipynb`*
* **Web Scraping:** Scraped a Wikipedia table for Falcon 9 launch records to gather additional data not present in the API.
    * *Notebook: `2_Data_Collection_with_Web_Scraping.ipynb`*

### 2. Data Wrangling & Exploratory Data Analysis (EDA)
* **Pandas & SQL:** Cleaned and merged the datasets. Performed EDA using Pandas and SQL to understand the data, find the number of launches per site, and analyze mission outcomes.
    * *Notebook: `3_EDA.ipynb`*
    * *Notebook: `4_EDA_with_SQL.ipynb`*

### 3. Interactive Visualization
* **Matplotlib & Seaborn:** Created static plots to visualize the relationship between features like `PayloadMass`, `LaunchSite`, and success rate.
    * *Notebook: `5_EDA_Visualization.ipynb`*
* **Folium (Interactive Maps):** Plotted launch sites on an interactive map and color-coded launch outcomes (success/failure) for each site.
    * *Notebook: `6_Interactive_Visual_Analytics_with_Folium_lab.ipynb`*
* **Plotly Dash (Dashboard):** Built the final interactive dashboard (shown above) to analyze success rates based on user-selected inputs for launch site and payload mass.
    * *Script: `7_spacex_dash_app.py`*

<p align="center">
<img width="670" alt="Folium Map Example" src="https://user-images.githubusercontent.com/46462603/152728830-e7a4d921-706e-4040-af27-b4b27361f8c1.png">
</p>

### 4. Machine Learning Prediction
* **Preprocessing:** Standardized the feature data using `StandardScaler` and split the dataset into training and testing sets.
* **Model Training:** Trained four different classification models to predict the `Class` (landing success) of a launch:
    1.  Logistic Regression
    2.  Support Vector Machine (SVM)
    3.  Decision Tree
    4.  K-Nearest Neighbors (KNN)
* **Hyperparameter Tuning:** Used `GridSearchCV` to find the best hyperparameters for each model.
* **Evaluation:** Compared the models based on their validation accuracy and confusion matrices.
    * *Notebook: `8_Machine_Learning_Prediction.ipynb`*

---

## Results & Conclusion

The Decision Tree classifier was the most effective model for this problem. After tuning, the models were ranked as follows based on their `GridSearchCV` best validation score:

| Model | Best Score (Accuracy) |
| :--- | :--- |
| **Decision Tree** | **0.8893** |
| K-Nearest Neighbors (KNN) | 0.8482 |
| Support Vector Machine (SVM) | 0.8482 |
| Logistic Regression | 0.8464 |

<br>
The Decision Tree model provides a strong predictive tool for determining launch success. This project successfully demonstrates an end-to-end data science workflow, from data collection and cleaning to building an interactive dashboard and a predictive machine learning model.

### Acknowledgments
This is a portfolio project completed as the final capstone for the **IBM Data Science Professional Certificate** on Coursera.
