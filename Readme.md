# Student Alcohol Consumption
**Author:** Eon Slemp and Lhamu Tsering

## Overview 
This Datascience project attempts to identify students at risk of alcohol abuse. Identifying the factors that influence youth alcohol abuse, can help
* Prioritize resources 
* Develop new interventions
* Reduce likelihood of dropout
* Improve life outcomes for NYC students

## Business Problem
Alcohol is the most prevalent and commonly used substance among the youth in most countries around the world today. According to the cdc website on [Underage Drinking](https://www.cdc.gov/alcohol/fact-sheets/underage-drinking.htm) "Underage drinking is a significant public health problem in the U.S. Excessive drinking is responsible for more than 3,500 deaths and 210,000 years of potential life lost among people under age 21 each year.1 Underage drinking cost the U.S. $24 billion in 2010.2 There were approximately 119,000 emergency rooms visits by persons aged 12 to 21 for injuries and other conditions linked to alcohol in 2013." Therefore, Alcohol Consumption among students is a most necessary and important subject to be researched.  There are several negative effects of adolescent alcohol abuse like memory difficulties, brain develoopment, higher chances of having alcohol related issues as an adult
We say that the children and youth are the pillars of the future. So, to be able to protect and prevent young students from becoming heavy alcohol drinkers becomes very important. One of the way to do this, is to first identify what factors or condition in a student or teenager's life makes them take decisions that lead them to become heavy drinkers. 

## Data 

This dataset is sourced from the UCI Machine Learning Repository, ["Student Performance Data Set"](http://archive.ics.uci.edu/ml/datasets/Student+Performance), donated to UCI ML Repo by Prof. Paulo Cortez of University Minho. His original work on the dataset, "USING DATA MINING TO PREDICT SECONDARY SCHOOL STUDENT PERFORMANCE, can be found [here](http://www3.dsi.uminho.pt/pcortez/student.pdf)

For this project we only used the dataset containing students who take the portueguese language course. There are 649 observations and 33 attributes in total.

**Variables Information:**

1. school - student's school (binary: 'GP' - Gabriel Pereira or 'MS' - Mousinho da Silveira)
2. sex - student's sex (binary: 'F' - female or 'M' - male)
3. age - student's age (numeric: from 15 to 22)
4. address - student's home address type (binary: 'U' - urban or 'R' - rural)
5. famsize - family size (binary: 'LE3' - less or equal to 3 or 'GT3' - greater than 3)
6. Pstatus - parent's cohabitation status (binary: 'T' - living together or 'A' - apart)
7. Medu - mother's education (numeric: 0 - none, 1 - primary education (4th grade), 2 - 5th to 9th grade, 3 - secondary education or 4 - higher education)
8. Fedu - father's education (numeric: 0 - none, 1 - primary education (4th grade), 2 - 5th to 9th grade, 3 - secondary education or 4 - higher education)
9. Mjob - mother's job (nominal: 'teacher', 'health' care related, civil 'services' (e.g. administrative or police), 'at_home' or 'other')
10. Fjob - father's job (nominal: 'teacher', 'health' care related, civil 'services' (e.g. administrative or police), 'at_home' or 'other')
11. reason - reason to choose this school (nominal: close to 'home', school 'reputation', 'course' preference or 'other')
12. guardian - student's guardian (nominal: 'mother', 'father' or 'other')
13. traveltime - home to school travel time (numeric: 1 - <15 min., 2 - 15 to 30 min., 3 - 30 min. to 1 hour, or 4 - >1 hour)
14. studytime - weekly study time (numeric: 1 - <2 hours, 2 - 2 to 5 hours, 3 - 5 to 10 hours, or 4 - >10 hours)
15. failures - number of past class failures (numeric: n if 1<=n<3, else 4)
16. schoolsup - extra educational support (binary: yes or no)
17. famsup - family educational support (binary: yes or no)
18. paid - extra paid classes within the course subject (Math or Portuguese) (binary: yes or no)
19. activities - extra-curricular activities (binary: yes or no)
20. nursery - attended nursery school (binary: yes or no)
21. higher - wants to take higher education (binary: yes or no)
22. internet - Internet access at home (binary: yes or no)
23. romantic - with a romantic relationship (binary: yes or no)
24. famrel - quality of family relationships (numeric: from 1 - very bad to 5 - excellent)
25. freetime - free time after school (numeric: from 1 - very low to 5 - very high)
26. goout - going out with friends (numeric: from 1 - very low to 5 - very high)
27. Dalc - workday alcohol consumption (numeric: from 1 - very low to 5 - very high)
28. Walc - weekend alcohol consumption (numeric: from 1 - very low to 5 - very high)
29. health - current health status (numeric: from 1 - very bad to 5 - very good)
30. absences - number of school absences (numeric: from 0 to 93)
31. G1 - first period grade (numeric: from 0 to 20)
32. G2 - second period grade (numeric: from 0 to 20)
33. G3 - final grade (numeric: from 0 to 20, output target)

## Methods
The Cross-industry standard process for data mining, known as CRISP-DM of process model was followed
1. Business Understanding
2. Data Sourced
3. Data Understanding - Data Cleaning and EDA
4. Data Preparation - Feature Engineering and Feature Selection
5. Modeling - Logistic Regression, KNN, Decision Tree
6. Finding 
7. Recommendations

## Results

The Final Model was a Logistic Regression model with the following metrics:
Test Accuracy score:  0.82
Test F1 score:  0.59
Test Recall score:  0.65 (Focusing on Minimizing False Negatives)

![Confusion Matrix](images/Confusion_matrix.png)

## Conclusions
The features that were selected and produced the best interpretable model are (also showing relation to the target variable based on the model):

1. sex = negative relation to student alcohol consumption behavior
2. absences = positive relation to student alcohol consumption behavior
3. G1= negative relation to student alcohol consumption behavior
4. G2 = negative relation to student alcohol consumption behavior
5. G3 = negative relation to student alcohol consumption behavior
6. idle = negative relation to student alcohol consumption behavior
7. grade_avg = negative relation to student alcohol consumption behavior
8. goout_2 =negative relation to student alcohol consumption behavior
9. goout_3 =negative relation to student alcohol consumption behavior
10.goout_5 = positive relation to student alcohol consumption behavior

Signals that might indicate high level of alcohol use can be lots of absences from classroom, falling grades, too much time spent going out. For guardians and authorities who supervise students, these monitoring these factors might help in identifying problems with alcohol early on. With this, incentives to not use alcohol may be put in place during school hours and at home. 


## Further Steps

Although this dataset was very limited had a lot of beef in terms of information collected on the attributes, it lacked in the mainly number and diversity of observations, to truly generalize on the population. Further steps towards this business problem will be to source data that is reflective of the population of students here in the US.

## For More Information

See the full analysis in the [Jupyter Notebook](Student_Alcohol_Consumption.ipynb) or review this [presentation](https://docs.google.com/presentation/d/1CcGmXfrhjVGh73J-wIGiYFqX3ekrncastnPEJldWL3o/edit#slide=id.ga9d7b3f7fa_0_37)

For additional info, contact :

Lhamu Tsering
Email: boutlhamu@gmail.com 

Eon Slemp 
Email: eonslemp@gmail.com

## Repository Structure

* `Readme.md` : Readme file giving and overview of project
* `Student_Alcohol_Consumption.ipynb` : Main Notebook showing model process
* `EDA.ipynb` : Notebook showing Exploratory Data Analysis
* `student-por.csv` : Data Set csv file
* `images`: Folder containing saved images
