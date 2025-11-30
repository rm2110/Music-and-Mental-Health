# Music & Mental Health — Predictive Analysis Using Machine Learning  
*A data-driven study exploring how music listening behaviors correlate with mental health.*

---

## Project Overview  
This project analyzes how **music listening habits** relate to **mental health indicators** such as Depression, Anxiety, Insomnia, and OCD. Using a real-world survey dataset, it performs detailed **EDA**, feature preprocessing, and builds machine learning models — **Logistic Regression** and **Decision Tree Classifier** — to predict **depression levels** from users’ musical behaviors, song attributes, and demographic information.

The goal is to uncover meaningful insights about how listening preferences and patterns can influence or correlate with mood and psychological well-being.

---

## Objectives  
- Understand user listening patterns across genres, time spent, and habits.  
- Explore relationships between music features and mental-health scores.  
- Clean, preprocess, and encode mixed-type survey data.  
- Predict **high vs low depression** using machine learning models.  
- Evaluate models using accuracy, F1-score, and ROC–AUC.  
- Identify which music-related features most influence depression levels.

---

## Dataset Description  

The dataset contains **736 entries** and **33 features**, including:

### Demographic Features
- Age  
- Primary Streaming Service  

### Music Listening Habits
- Hours per day  
- Listening while working/studying  
- Instrumentalist / Composer status  
- Favorite genre  
- Genre frequency ratings (Classical, Rock, Hip-Hop, EDM, Pop, etc.)  
- Foreign-language music exposure  

### Song Attributes
- BPM (average tempo of preferred songs)  

### Mental Health Scores
Self-reported values (0 = none, 10 = extreme):  
- Anxiety  
- Depression  
- Insomnia  
- OCD  
- *Music Effects* (improvement/worsening/no effect)

---

## Data Preprocessing  

### Missing Values  
- Numerical columns → **Median Imputation**  
- Categorical columns → **Most Frequent Category Imputation**  

### Encoding  
- Categorical features encoded using **One-Hot Encoding**  

### Scaling  
- Numerical features scaled using **StandardScaler**

### Target Variable  
`Depression` converted to **binary classes**:  
- **1 = High Depression** (score ≥ dataset median)  
- **0 = Low Depression**

---

## Exploratory Data Analysis (EDA)

Performed detailed analysis to understand trends, patterns, and relationships:  
- Distribution plots for age, BPM, and listening hours  
- Genre popularity and frequency visualization  
- Correlation analysis between mental health scores  
- Boxplots, bar charts, and interactive Plotly visualizations  
- Comparison of depression levels across genres and listening habits  

### Key Insights  
- Certain genres show higher associations with depression scores.  
- Higher BPM preferences sometimes correlate with elevated anxiety/depression levels.  
- Heavy music listeners (4+ hours/day) display higher mental-health variability.  
- Instrumentalists/composers report different emotional reactions compared to general listeners.

---

## Machine Learning Models

### 1) Logistic Regression  
- Simple, interpretable model  
- Models probability of high depression  
- Uses sigmoid function and MLE for optimization  
- Good generalization and balanced performance  

### 2) Decision Tree Classifier  
- Handles non-linear relationships  
- Creates human-readable decision rules  
- Depth limited to **5** to reduce overfitting

---

## Model Evaluation  

### **Metrics Used**
- **Accuracy**  
- **Precision**  
- **Recall**  
- **F1 Score**  
- **Confusion Matrix**  
- **ROC Curve**  
- **AUC Score**  
- **5-Fold Cross-Validation Accuracy**

### **Results Summary**

#### Logistic Regression  
- **Accuracy:** 68.9%  
- **Precision:** 0.713  
- **Recall:** 0.713  
- **F1 Score:** 0.713  
- **ROC–AUC:** 0.760  
- **Cross-Validation:** 69.6%

#### Decision Tree  
- **Accuracy:** 66.9%  
- **Precision:** 0.670  
- **Recall:** 0.763  
- **F1 Score:** 0.713  
- **ROC–AUC:** 0.745  
- **Cross-Validation:** 69.4%

### Interpretation  
- Logistic Regression performed slightly better and generalized well.  
- Decision Tree achieved higher recall, helping detect high-depression cases more effectively.  
- AUC > 0.7 for both models indicates strong predictive ability.

---

## Key Insights  
- Musical behavior contains measurable signals related to mental health.  
- Listening time, favorite genres, BPM, and habits show significant patterns.  
- Behavioral data can support early detection of mental-health trends.  

---

## Future Enhancements  
- Experiment with ensemble models (Random Forest, XGBoost)  
- Add time-series/music streaming behavior  
- Use SHAP/LIME for interpretability  
- Build a dashboard for real-time prediction  
- Expand dataset for stronger generalization  

---

## Tech Stack  
- **Python**  
- Pandas  
- NumPy  
- Scikit-learn  
- Matplotlib  
- Seaborn  
- Plotly  

---

## Conclusion  
This project demonstrates how **machine learning and behavioral data** can be used to understand mental health patterns. Through structured EDA, preprocessing, and predictive modeling, we show that music listening habits hold meaningful relationships with depression levels — opening opportunities for personalized wellness tools and early intervention systems.
