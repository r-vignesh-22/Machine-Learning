#  Multiple Linear Regression (MLR)
Multiple Linear Regression is an extension of simple linear regression.  
Instead of using **one input feature**, MLR uses **two or more features** to predict a target value.  

**Equation:**
\[
y = m_1X_1 + m_2X_2 + ... + m_nX_n + c
\]

Where:  
- \(X_1, X_2, ..., X_n\) = independent features  
- \(m_1, m_2, ..., m_n\) = coefficients (slopes)  
- \(c\) = intercept  

---

## 🔹 When to Use MLR
- When the target variable depends on **multiple factors**.  
- Example: predicting **house prices** (based on area, rooms, location, age).  
- Example (our case): predicting **tea taste** based on sugar, milk, tea leaves, and water.  

---

## 🔹 Tea Example 🍵
We want to predict the **taste score** of tea using multiple ingredients:  
- Sugar (spoons)  
- Milk (ml)  
- Tea Leaves (spoons)  
- Water (ml)  

Equation:
\[
Taste = m_1 \cdot Sugar + m_2 \cdot Milk + m_3 \cdot TeaLeaves + m_4 \cdot Water + c
\]

---