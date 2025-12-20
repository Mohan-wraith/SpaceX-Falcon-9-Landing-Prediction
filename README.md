# 🚀 SpaceX Falcon 9 Landing Prediction

[![Python](https://img.shields.io/badge/Python-3.9%2B-blue?logo=python&logoColor=white)](https://www.python.org/)
[![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-150458?logo=pandas&logoColor=white)](https://pandas.pydata.org/)
[![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-Machine%20Learning-F7931E?logo=scikit-learn&logoColor=white)](https://scikit-learn.org/)
[![Plotly Dash](https://img.shields.io/badge/Plotly%20Dash-Interactive%20Dashboard-00416A?logo=plotly&logoColor=white)](https://dash.plotly.com/)
[![Render](https://img.shields.io/badge/Render-Deployed-46E3B7?logo=render&logoColor=white)](https://spacex-falcon-9-landing-prediction-2.onrender.com/)

> **Live Dashboard:** [Click here to view the deployed app](https://spacex-falcon-9-landing-prediction-2.onrender.com/)

---

## 📖 Project Overview

This end-to-end data science capstone project aims to predict the successful landing of the SpaceX Falcon 9 first stage. A successful landing significantly reduces launch costs (from ~$160M to ~$62M). By accurately predicting landing outcomes, competitor firms can optimize their bidding strategies against SpaceX.

This project demonstrates a complete Data Science pipeline:
1.  **Data Extraction:** REST API queries and Web Scraping.
2.  **Data Wrangling:** Cleaning, filtering, and SQL analysis.
3.  **Visualization:** Interactive maps (Folium) and dynamic dashboards (Dash).
4.  **Machine Learning:** Training and hyperparameter tuning of classification models to achieve **88.9% accuracy**.

---

## 📊 Interactive Dashboard

I developed a fully interactive web application using **Plotly Dash** to visualize launch success rates based on site selection and payload mass.

| **Scatter Correlation Analysis** | **Launch Site Success Rates** |
|:---:|:---:|
| <img src="https://user-images.githubusercontent.com/46462603/152729009-c2cdaba4-674c-4103-b540-e77ad3544a99.png" width="100%"> | <img src="https://user-images.githubusercontent.com/46462603/152729002-f731499b-aab8-46a1-b1c3-583c24ae909e.png" width="100%"> |

---

## 🛠 Project Workflow

The project follows a structured pipeline across multiple notebooks:

### 1. Data Collection
* **API Extraction:** Automated extraction from the [SpaceX REST API](https://api.spacexdata.com/v4) to gather core launch data.
* **Web Scraping:** Utilized `BeautifulSoup` to scrape historical launch records from Wikipedia.
    * 📂 *Notebooks: `1_Data_Collection_API.ipynb`, `2_Data_Collection_with_Web_Scraping.ipynb`*

### 2. Exploratory Data Analysis (EDA)
* **SQL & Pandas:** Performed rigorous data cleaning and SQL queries to identify trends in mission outcomes and payload distributions.
* **Visualization:** Generated static plots (Seaborn/Matplotlib) and geospatial visualizations (Folium) to map launch site success probability.
    * 📂 *Notebooks: `3_EDA.ipynb`, `4_EDA_with_SQL.ipynb`, `5_EDA_Visualization.ipynb`, `6_Interactive_Visual_Analytics_with_Folium_lab.ipynb`*

### 3. Machine Learning & Prediction
* **Preprocessing:** Applied `StandardScaler` and split data for training/testing.
* **Model Selection:** Trained and evaluated four classifiers:
    * Logistic Regression
    * Support Vector Machines (SVM)
    * Decision Tree Classifier
    * K-Nearest Neighbors (KNN)
* **Optimization:** Utilized `GridSearchCV` for hyperparameter tuning.
    * 📂 *Notebook: `8_Machine_Learning_Prediction.ipynb`*

---

## 🏆 Model Results

The **Decision Tree Classifier** outperformed other models, achieving the highest validation accuracy after hyperparameter tuning.

| Rank | Model | Accuracy (Validation) |
| :--- | :--- | :--- |
| 🥇 | **Decision Tree** | **88.93%** |
| 🥈 | K-Nearest Neighbors (KNN) | 84.82% |
| 🥉 | Support Vector Machine (SVM) | 84.82% |
| 4 | Logistic Regression | 84.64% |

---

## 🚀 How to Run the Project

### Prerequisites
* Python 3.7+
* Libraries: `pandas`, `numpy`, `scikit-learn`, `dash`, `plotly`, `folium`

### Installation
1.  **Clone the repo:**
    ```bash
    git clone [https://github.com/Mohan-wraith/SpaceX-Falcon-9-Landing-Prediction.git](https://github.com/Mohan-wraith/SpaceX-Falcon-9-Landing-Prediction.git)
    ```
2.  **Install dependencies:**
    ```bash
    pip install -r requirements.txt
    ```
3.  **Run the Dashboard:**
    ```bash
    python app.py
    ```
    *Open `http://127.0.0.1:8050` in your browser.*

---

## 👨‍💻 Author

**Mohan-wraith**
* [GitHub Profile](https://github.com/Mohan-wraith)
* [LinkedIn](https://linkedin.com/in/your-linkedin-url) *(Optional: Add your link here)*

---

### Acknowledgments
* Completed as part of the **IBM Data Science Professional Certificate** Capstone.
