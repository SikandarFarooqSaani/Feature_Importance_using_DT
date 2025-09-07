# 🔢 Feature Importance on MNIST using Decision Trees  

---

## 📌 Project Overview  
This project explores **feature importance** in the **MNIST dataset**.  
Since each digit image has **784 pixel features (28x28)**, many of them are just blank space around the digit.  
We use **Decision Trees & Random Forests** to identify which pixels are truly important for classification.  

This helps improve **model efficiency** by focusing only on the relevant features (digit area) and ignoring the unimportant blank areas.  

---

## 📂 Dataset  
- 📊 **MNIST Dataset**  
- Shape → `28x28 = 784` features per image  
- Labels → Digits `0–9`  
- Example heatmap of a single digit image is attached 🔥  
link : https://www.kaggle.com/datasets/pratikyuvrajchougule/health-and-lifestyle-data-for-regression
---

## ⚙️ Tech Stack & Libraries  
- **Python** 🐍  
- **NumPy, Pandas** → Data handling  
- **Scikit-learn** → Decision Tree, Random Forest, Feature Importance  
- **Matplotlib / Seaborn** → Heatmaps & Visualization  

---

## 🚀 Workflow  

1. **Data Preparation**  
   - Loaded MNIST dataset (28x28 pixel images).  
   - Flattened into `784 features`.  
<img width="519" height="413" alt="rfi-`" src="https://github.com/user-attachments/assets/e56500ee-66fc-4613-8345-84f9a3c6fcc7" />

2. **Feature Importance with Random Forest**  
   - Fitted `(X, y)` on **Random Forest Classifier**.  
   - Calculated **feature importances**.  
   - Visualized using a **heatmap** → clearly showed that only the **center pixels** (where digits lie) are important, while the **outer black border pixels** are irrelevant.  
<img width="533" height="413" alt="rfi-2" src="https://github.com/user-attachments/assets/202aaff6-b1ea-41a6-b381-29c2c9ebf476" />

   ✅ This means we can **skip unimportant pixels** → better efficiency, faster training.  

3. **Decision Tree Classifier**  
   - Used a **Decision Tree** on sample data.  
   - Plotted the **tree structure** 🪵 (image attached).  
   - Showed how feature importance is calculated.  
   - Confirmed that **importance scores sum to 1**.  
<img width="515" height="389" alt="rfi-4" src="https://github.com/user-attachments/assets/d78a25c4-dea0-48ef-b064-2e30c0bbd9d7" />

---

## 📊 Results  

- **Feature Importance Heatmap (Random Forest)**  
  - Highlighted central pixels as most important.  
  - Black border regions = negligible importance.  
<img width="533" height="413" alt="rfi-2" src="https://github.com/user-attachments/assets/c310ea32-0dcb-4fa6-8246-e7d7cb9eaec8" />


- **Decision Tree Visualizations**  
  - Small sample dataset of 5 → plotted tree with clear splits.  
  - Showed decision-making process and importance distribution.  

- **Key Takeaway**  
  - Only a **fraction of the 784 features** carry useful information.  
  - Eliminating irrelevant pixels → **smaller, faster models without losing accuracy**.  

---

## 🎯 Conclusion  
This project demonstrated how **feature importance analysis** helps in:  
- Identifying **useful vs. useless features**.  
- Improving **training efficiency** by dropping irrelevant features.  
- Understanding **how decision trees and random forests "see" the data**.  

> A crucial step before applying more complex models to high-dimensional datasets like MNIST. 🚀  

---
