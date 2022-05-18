# CPSC392_Project1
Project 1
This dataset is adapted from the World Health Organization on Strokes (it's based on real data but is NOT REAL). Use this dataset to answer the following questions and perform the following tasks. Feel free to add extra cells as needed, but clearly identify where each question is answered, both the code and Markdown cells. Please remove any superflous code. Please put any written/typed responses in MARKDOWN CELLS.
Data Information
reg_to_vote: 0 if no, 1 if yes.
age: age of the patient in years.
hypertension: 0 if the patient doesn't have hypertension, 1 if the patient has hypertension.
heart_disease: 0 if the patient doesn't have any heart diseases, 1 if the patient has a heart disease.
ever_married: 0 if no, 1 if yes.
Residence_type: 0 for Rural, 1 for Urban.
avg_glucose_level: average glucose level in blood.
bmi: body mass index.
smoking_status_smokes, smoking_status_formerly: Whether or not the person smokes, or formerly smoked. If a person has 0's for both these columns, they never smoked.
stroke: 1 if the patient had a stroke or 0 if not.
dog_owner: 0 if no, 1 if yes.
income_in_k: income in thousands
er_visits: number of recorded Emergency Room visits in lifetime.
raccoons_to_fight: number of racoons the patient belives they could fight off at once.
fast_food_budget_month: amount (in US dollars) spent on fast food per month.
Part I: Logistic Regression
Build a logistic regression model to predict whether or not someone had a stroke based on all the other variables in the dataset.
Count the missing data per column, and remove rows with missing data (if any).
Use 10 fold cross validation for your model validation. Z-score your continuous/interval variables only. Store both the train and test accuracies to check for overfitting. Is the model overfit? How can you tell?
After completing steps 1-2, fit another logistic regression model on ALL of the data (no model validation; but do z score) using the same predictors as before, and put the coefficients into a dataframe called coef.
print out a confusion matrix for the model you made in part 3. What does this confusion matrix tell you about your model? How can you tell?
Part II: Data Exploration
The WHO has asked the following five questions, create at least 1 ggplot graph per question (using the above data + model when needed) to help answer each question, and explicitly answer the question in a Markdown cell below your graph. You may use other calculations to help support your answer but MUST pair it with a graph. Write your answer as if you were explaining it to a non-data scientist. You will be graded on the effectiveness and clarity of your graph, as well as the completeness, clarity, and correctness of your responses and justifications.
In this specific data set, do dog-owners over 50 have a higher average probability of stoke than non-dog owners who currently smoke? How can you tell? (Do not use the model for this question, it's asking you to compare the observed probability of having a stroke in the two groups described).
What is the relationship between average blood glucose and BMI? Is the relationship between those two variables different for people who are and are not registered to vote? How can you tell?
Is your logistic regression model most accurate for people who make less than 30k, between 30-90k, or over 90k? Discuss the potential accuracy and ethical implications if your model were more accurate for different groups (you can use the full model from part I-3 to check accuracy for each of these groups; DO NOT create/fit new models for each income range, use the model from part I-3 to calculate the accuracy for each of these groups.)
Which of the following variables is the strongest predictor of having a stroke (owning a dog, residence type, marriage, being registered to vote)? How were you able to tell?
Create a variable er_visits_per_year that calculates the # of visits to the ER that a person has had per year of life. Store this variable in your data frame (no need to include this variable in the previous logistic regression model). Is the # of ER visits per year different for stroke and non-stroke patients? How can you tell?
