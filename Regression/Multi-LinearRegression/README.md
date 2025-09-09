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

## 🔹 Code Example

```python
import pandas as pd
from sklearn.linear_model import LinearRegression

# Dataset
data = {
    "Sugar":     [1, 2, 3, 4, 5, 2, 3, 4],
    "Milk":      [100, 150, 200, 250, 300, 180, 220, 260],
    "TeaLeaves": [1, 2, 2, 3, 3, 2, 3, 4],
    "Water":     [200, 220, 250, 300, 350, 230, 260, 320],
}
taste = [40, 55, 65, 75, 85, 60, 70, 80]

df = pd.DataFrame(data)
df["Taste"] = taste

X = df[["Sugar", "Milk", "TeaLeaves", "Water"]]
y = df["Taste"]

# Train Model
model = LinearRegression()
model.fit(X, y)

print("Slopes (m1,m2,m3,m4)", model.coef_)
print("Intercept(C)", model.intercept_)

# Prediction
print("Predicted Taste for Sugar=3, Milk=200, TeaLeaves=3, Water=250:",
      model.predict([[3, 200, 3, 250]]))

plt.scatter(df["Sugar"], y, color="red", label="Actual taste")
plt.plot(df["Sugar"], model.predict(X), color="blue", label="Model predictions")
plt.xlabel("Sugar (spoons)")
plt.ylabel("Taste Score")
plt.title("Effect of Sugar on Tea Taste (with other factors)")
plt.legend()
plt.show()
```