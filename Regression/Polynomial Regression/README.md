## Polynomial Regression
We aim to predict height (y) based on an independent variable (x) using Linear Regression and Polynomial Regression.

### Linear Regression

    Equation:y=m⋅x+c

Where:  
x = independent variable (Age)    
y = dependent variable (Height)     
m = slope (coefficient)  
c = intercept

What we did:

Used LinearRegression from scikit-learn.

Fitted the model with    
x as the independent variable and   
y as the dependent variable.

Predicted heights using the fitted model.

Plotted the linear regression line against actual data.
## Polynomial Regression

Original Polynomial Regression Formula (general form):

    𝑦=𝑚0+𝑚1⋅𝑥+𝑚2⋅𝑥2+𝑚3⋅𝑥3+⋯+𝑚𝑛⋅𝑥𝑛

Where:

𝑚0 = intercept

𝑚1,𝑚2,..,𝑚𝑛 = coefficients for each degree term

n = degree of the polynomial

What we did:

Used PolynomialFeatures from scikit-learn to generate polynomial terms of 𝑥



Fitted a LinearRegression model on these transformed features.

Predicted heights and visualized the polynomial curve.

This allows the model to capture non-linear growth patterns, such as faster growth during childhood and slower growth in adulthood.

## Dataset
    x (years)	y (Height cm)   
        5	            105
        7	            115

## Visualization

Black dots: actual data points

Blue line: linear regression prediction

Red curve: polynomial regression prediction

## Key Insights

Linear regression captures the general trend but may miss finer details.

Polynomial regression fits non-linear growth more accurately.

Using polynomial regression is particularly helpful in childhood and teenage years, where growth is faster and less linear.