# **A/B Testing of Vanguard UI - Data Analysis Project**

## **Project Overview**
This project analyzes an **A/B test** conducted on a new **Vanguard UI** to determine its impact on user behavior. The study compares a **Test** group (new UI) against a **Control** group (existing UI) to evaluate metrics such as error rates, return-to-start incidents, and session completion rates.

## **Objective**
The goal is to determine whether the new UI leads to a **better user experience**, measured by **error occurrences, session progression, and return-to-start incidents**. The analysis employs **statistical tests and data visualizations** to derive insights.

---

## **Data Cleaning & Preprocessing**
To ensure data consistency and accuracy, the following steps were performed:  

✅ **Removing Duplicates**: Filtered duplicate entries based on `ClientID`, `visit_id`, and `date_time`.  
✅ **Handling Missing Values**: Checked for null values and imputed or excluded them where necessary.  
✅ **Feature Engineering**: Created new columns such as `prev_step`, `error_flag`, and `same_step_errors` to track user behavior.  
✅ **Flagging Errors**: Defined errors as **backward navigation** and **repeated steps**.  
✅ **Categorizing Age Groups**: Segmented users into **age bins** for better analysis.  

---

## **Exploratory Data Analysis & Visualizations**  

📊 **Trend Analysis**  
- Used **polynomial regression models** to analyze trends in **session duration vs. age** and **accounts vs. tenure**.  
- Found **significant trends** (p < 0.05), though R-squared values suggested moderate explanatory power.  

📉 **Return-to-Start Incident Rate**  
- Compared return-to-start incidents across process steps in the **Control** and **Test** groups.  
- The **Test group showed a higher return rate**, particularly at Step 1 (~41%).  

📈 **Total Sessions Per Step**  
- **Drop-off rates** were visualized across process steps.  
- The Test group showed **faster drop-offs**, suggesting possible usability issues.  

📊 **Error Rate Comparison (T-Test Results)**  
- **Hypothesis**: The new UI **reduces errors** compared to the old UI.  
- **Result**: **p = 0.276**, meaning **no significant difference** in error rates between groups.  
- Conclusion: The new UI **did not significantly improve error rates**.  

---

## **Key Insights**  
📌 The new UI resulted in **higher return-to-start incidents**, particularly at Step 1.  
📌 No **significant reduction in errors** was observed (t-test failed to reject null hypothesis).  
📌 The **drop-off rate increased** in the Test group, suggesting **potential usability issues**.  
📌 Further refinements to the UI may be necessary before full rollout.  

---

## **Next Steps**  
🚀 Conduct **user surveys** to understand qualitative feedback on UI changes.  
📊 Perform **clickstream analysis** to detect specific pain points.  
🛠️ Iterate on UI design based on findings and re-run the A/B test.  

---

## **Repository Structure**  
```
/data               # Raw and cleaned datasets  
/notebooks         # Jupyter notebooks with analysis  
/visuals           # Tableau charts and key plots  
/scripts          # Python scripts for preprocessing & modeling  
README.md         # Project summary & findings  
```

---

## **Technologies Used**  
- **Python (Pandas, NumPy, SciPy, Matplotlib, Seaborn)** for data processing and analysis.  
- **Tableau** for visualization.  
- **Git/GitHub** for version control.  

---

## **Conclusion**  
While the **new Vanguard UI** introduced changes, **it did not significantly reduce errors** and led to **higher return-to-start incidents**. These findings suggest a need for **further optimizations** before a full-scale rollout.

