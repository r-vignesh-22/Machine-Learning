## Student Marks Prediction using Linear Regression

This project predicts students’ marks based on the number of hours they study.

It demonstrates both:            
✔ Manual calculation of linear regression    
✔ Python implementation with visualization

## What is Linear Regression?

Linear regression is a method to find the relationship between two variables:

    1.  Independent variable (X): Study Hours
    2.  Dependent variable (y): Marks

It fits a straight line to the data, called the regression line, which best represents the trend.

    Formula:-   y=m⋅x+b

    m → slope (how much marks increase for each extra study hour)   
    b → intercept (marks when study hours = 0)

## Dataset

We use a dataset of 100 students (student_dataset_capped.csv) that contains:

    Study_Hours → Number of hours studied   
    Marks → Marks scored

## Project Workflow
### 1. Load Data

We first load the dataset into Python for analysis.

### 2. Manual Linear Regression

We calculate the slope (m) and intercept (b) using statistical formulas.

Final regression equation obtained:

    Marks=5.12×Study Hours+29.45



### 3. Predict Marks

Using the regression equation, we predict marks for new study hours:

Study Hours	Predicted Marks
6	~60
7.5	~68
9	~76

### 4. Visualization

We visualize the results using a graph:

    Blue dots → Actual student marks from dataset  
    Red line → Regression line (best fit line)   
    Green crosses → Predicted marks for new study hours

This clearly shows how well the regression line fits the actual data.

## Results

The project successfully establishes a relationship between study hours and marks.

The regression equation can be used to predict marks for any given study time.

Visualization confirms that students who study more hours generally score higher.