# IBM Applied Data Science Capstone Project

## Executive Summary
In this capstone project, we predict if the SpaceX Falcon 9 first stage will land successfully using several machine learning classification algorithms.

The main steps in this project include:
- Data collection, wrangling, and formatting
- Exploratory data analysis
- Interactive data visualization
- Machine learning prediction

Our analysis shows that some features of the rocket launches have a correlation with the outcome of the launches. The Decision Tree classifier performed best among the models tested.

---

## Introduction
SpaceX advertises Falcon 9 rocket launches with a cost of 62 million dollars; other providers cost upward of 165 million dollars each. Much of the savings comes from reusing the first stage.  
If we can determine whether the first stage will land, we can estimate launch cost. This is useful if an alternate company wants to bid against SpaceX.

Most unsuccessful landings are planned. Sometimes, SpaceX will perform a controlled landing in the ocean.  
The main question: given features such as payload mass, orbit type, and launch site, will the first stage of the rocket land successfully?

---

## Methodology
The overall methodology includes:

1. **Data collection**
   - SpaceX API  
   - Web scraping (Wikipedia)

2. **Exploratory data analysis (EDA)**
   - Using Pandas and NumPy  
   - SQL queries

3. **Data visualization**
   - Matplotlib, Seaborn  
   - Folium interactive maps  
   - Dash dashboard

4. **Machine learning prediction**
   - Logistic Regression  
   - Support Vector Machine (SVM)  
   - Decision Tree  
   - K-Nearest Neighbors (KNN)

---

## EDA with Pandas, NumPy, and SQL
- Derived statistics such as launch count by site, orbit frequency, and mission outcomes.  
- SQL queries answered questions like:  
  - Unique launch sites  
  - Total payload mass carried by NASA (CRS)  
  - Average payload mass for specific booster versions  

---

## Data Visualization
- Scatterplots, bar charts, and line charts explored relationships such as:  
  - Flight number vs. launch site  
  - Payload mass vs. launch site  
  - Success rate vs. orbit type  

- Folium maps showed:  
  - Launch site locations  
  - Success vs. failure outcomes on maps  
  - Distances from launch sites to cities, railways, and highways  

- Dash interactive app allowed:  
  - Filtering by launch site  
  - Viewing payload mass correlation with mission outcomes  

---

## Machine Learning Prediction
- Data standardized and split into training and testing sets.  
- Models trained: Logistic Regression, SVM, Decision Tree, KNN.  
- Hyperparameters tuned with GridSearchCV.  
- Evaluated using accuracy scores and confusion matrices.  

**Result:**  
- Decision Tree performed best.  
- KNN and SVM tied for second.  
- Logistic Regression performed lowest.

---

## Discussion
Some features correlate with mission outcome.  
For example, heavy payloads with Polar, LEO, and ISS orbits tend to have higher landing success.  
However, GTO orbits show mixed outcomes.  

---

## Conclusion
This project demonstrates how data collection, analysis, visualization, and machine learning can be combined to solve a real-world problem.  
Among the models tested, the Decision Tree algorithm provided the most accurate predictions for Falcon 9 first-stage landings.

---

~ Project completed as part of IBM Applied Data Science Capstone ~
