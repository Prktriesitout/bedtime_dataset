# 💤 Sleep Debt Analysis & Machine Learning Predictor

![Sleep Banner](https://images.unsplash.com/photo-1511295742364-92767fa62d9f?auto=format&fit=crop&w=1200&q=80)

An end-to-end data analysis and predictive modeling workspace investigating the interactions between demographics, evening behaviors (phone usage, caffeine intake, blue-light filter habits), and overall **Sleep Debt Severity** and **Next-Day Fatigue**.

---

## 📊 Key Analytical Insights

* **Sleep Duration is King:** 
  Sleep duration is the absolute strongest predictor of next-day fatigue. Each additional hour of sleep is associated with an average decrease of **1.6 points** on the next-day fatigue score.
* **Bedtime Phone Habits:**
  Heavy screen-time before bed is a prominent warning indicator. The median phone usage before sleep spikes from **30 minutes** (for those with optimal recovery) to **126 minutes** (for those in severe sleep debt).
* **The Evening Multiplier Effect:**
  Users combining highly optimized habits (≤30 minutes of bedtime phone use, zero caffeine after 5 PM, and active blue-light filters) averaged a mere **1.64 fatigue score**, compared to **4.95** for users who did not practice any of these.
* **Modest Blue-Light Filter Impacts:**
  Activating a blue-light filter provides helpful but relatively minor improvements—yielding about **7 extra minutes** of sleep, a **1.5-minute** reduction in sleep latency, and a **0.39-point** drop in fatigue.
* **Vulnerable Groups:**
  * **95.8%** of *Night Owls* experience moderate or severe sleep debt, compared to only **27.0%** of *Morning Larks*.
  * *Healthcare and Shift Workers* exhibit the highest severe sleep debt rate at **18.3%**—more than twice any other surveyed occupation.

---

## 🛠️ Machine Learning Model Suite & Performance

To predict the sleep debt category (`Optimal Recovery`, `Mild Deficit`, `Moderate Debt`, `Severe Sleep Debt`), we engineered the features and trained multiple machine learning models with excellent outcomes:

| Model Name | Key Features Utilized | Metrics (Test Set Accuracy) | Best Suited For |
| :--- | :--- | :---: | :--- |
| **Logistic Regression** | All Encoded Features | **98.7%** | Interpreting individual feature impacts (coefficients) |
| **Decision Tree Classifier** | `total_sleep_hours`, `is_severe` | **100.0%** | Ultra-fast rule-based predictions & deployment |
| **XGBoost Classifier** | `total_sleep_hours`, `is_severe` | **100.0%** | Production-grade ensemble gradient boosting |
| **K-Nearest Neighbors (KNN)** | `total_sleep_hours`, `is_severe` | **100.0%** | Distance-based similarity classification |
| **Random Forest Classifier** | `total_sleep_hours`, `is_severe` | **100.0%** | Highly robust, robust ensemble learning |

---

## 🚀 Interactive Deployment

The Decision Tree model is actively deployed using a **Gradio Web Application**. 

```python
# Launch Interface with your inputs
interface.launch(share=True)
```
👉 **Active live interface link:** [Gradio Demo App](https://2ae853e027e2672e0f.gradio.live)
