# energy_recovery_naive
# Global Pollution Classification Project

## Overview
This project classifies countries based on pollution severity (Low, Medium, High) using three machine learning models:
- **Multinomial Naïve Bayes (MNB)**
- **K-Nearest Neighbors (KNN)**
- **Decision Tree (DT)**

We evaluate the models based on **accuracy, precision, recall, and F1-score**.

---

## Dataset
- **Input Features:** Air Pollution, Water Pollution, Soil Pollution, Industrial Waste
- **Target Variable:** Pollution Severity (Low, Medium, High)
- **Data Preprocessing:** Missing values handled, features normalized, categorical variables encoded.

---

## Model Performance

### **1️⃣ Multinomial Naïve Bayes**
- **Accuracy:** 72%
- **Weakness:** Fails to classify the "High" pollution category (precision = 0.00)
- **Best at:** Classifying "Medium" pollution cases (100% recall)

| Class      | Precision | Recall | F1-Score |
|------------|----------|--------|----------|
| High       | 0.00     | 0.00   | 0.00     |
| Medium     | 0.72     | 1.00   | 0.84     |

---

### **2️⃣ K-Nearest Neighbors (KNN)**
- **Accuracy:** 75%
- **Strength:** Best overall performance with balanced classification.
- **Weakness:** Struggles with "High" pollution cases (27% recall)

| Class      | Precision | Recall | F1-Score |
|------------|----------|--------|----------|
| High       | 0.60     | 0.27   | 0.38     |
| Medium     | 0.77     | 0.93   | 0.84     |

---

### **3️⃣ Decision Tree**
- **Accuracy:** 70%
- **Strength:** Captures non-linear patterns well.
- **Weakness:** Poor precision for "High" pollution cases (33%)

| Class      | Precision | Recall | F1-Score |
|------------|----------|--------|----------|
| High       | 0.33     | 0.09   | 0.14     |
| Medium     | 0.73     | 0.93   | 0.82     |

---

## Key Insights
📊 **Trend Observations:**
- "High Pollution" cases are **harder to classify** accurately.
- KNN performed the best overall but still struggled with "High" severity cases.
- Industrial waste and air pollution were the strongest predictors.

💡 **Policy Recommendations:**
1. **Stricter Regulations on Industrial Waste** 📜
   - Limit waste disposal and encourage recycling.
2. **Incentives for Clean Energy Adoption** 🌱
   - Introduce subsidies for renewable energy.
3. **Investment in Public Transport** 🚌
   - Reduce reliance on private vehicles.
4. **Afforestation & Green Policies** 🌳
   - Implement urban tree planting programs.

---

## Future Improvements
🔹 **Improve "High Pollution" classification** using **ensemble models**.
🔹 **Feature Engineering:** Add more environmental factors (e.g., temperature, deforestation rate).
🔹 **Hyperparameter Tuning:** Optimize KNN (best `K` value) and Decision Tree (`max_depth`).

---

## How to Run
1. Install dependencies:
   ```sh
   pip install pandas numpy scikit-learn seaborn matplotlib
   ```
2. Run the script:
   ```sh
   python pollution_classification.py
   ```
3. Check results in console and confusion matrix plots.

---

## Conclusion
KNN provides the best overall classification, but improvements are needed for "High Pollution" detection. Stricter pollution control policies and further model optimizations are recommended.

