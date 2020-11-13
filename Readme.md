
# Factors Predicting Alcohol Consumption in Teens
**Authors** Lhamu Tsering and Eon Slemp

## Overview and Objectives
The purpose of this analysis is to generate insight into factors predictive of teenage alcohol abuse for the New York City Department of Education.   Adolescence is a critical time of neurological development.  During adolescence the brain is fitting itself to the environment to support behaviors that, ideally promote long term thriving.   Patterns of behavior established before the age of 20 will often persist for a lifetime.  The stimulus alcohol, like all addictive substances, causes a kind of hijacking of the behavioral machinery critical to a good life.   Alcohol is the most widely used intoxicant by teenagers and adults.   This analysis will inform policy in ways that can convert to improved life outcomes for individuals served by the New York City Department of Education.

## Optimizing outcomes for New York City Students
The New York City Department of Education serves over one million students annually.  The costs associated with alcohol abuse are wide and deep.  This large public school system has the potential to be a powerful leverage point from which to affect the lives of millions of people.  By identifying high risk students and funneling appropriate resources and interventions in their direction, we can impact millions of individual lives and the character of New York City life in aggregate.  

## The Data
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
* Test Accuracy score:  0.82
* Test F1 score:  0.59
* Test Recall score:  0.65 (Focusing on Minimizing False Negatives)

![Confusion Matrix](images/Confusion_matrix.png)

The results of our effort confirms what most people would guess without a machine learning classification study of the data… that a more stable and harmonious home life, higher academic performance, and solid support structures around the student tend to predict lower alcohol consumption.  Less harmonious home life, lower academic performance, with lots of idle time and more active social life tend to predict higher alcohol consumption. 

## Conclusions
Based on the features that produced the best model, the main characteristics influencing alcohol use are listed below. Interventions should aim at several areas that suggest increased risk.
1.  Family life - Resources allocated at higher level than the Department of Education to promote healthy family structures.  Family planning resources and education, and improved access to mental health resources would be two such areas of investment.
2.  Academic support - tutoring, and mentoring, school
3.  Deterrent efforts - Police resources to target those that might provide alcohol to teenagers and enforcing underage drinking laws.
4.  Idle time - After school activities that can engage less motivated students may help to displace drinking as a recreational activity.

## Further Steps
A study designed to reveal the causal relationships among the features would give greater insight into how to prioritize interventions.  My instinct is to say that all of the other observed features derive somehow from the quality of the students’ family environment,  but only a properly designed study can support such a conclusion. 

Although this dataset was very limitedin size it had a lot of good information collected on the attributes, it lacked in mainly number and diversity of observations, to truly generalize on the population. Further steps towards this business problem will be to source data that is reflective of the population of students here in the US.

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
