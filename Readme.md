
# Factors Predicting Alcohol Consumption in Teens
**Authors** Lhamu Tsering and Eon Slemp

## Overview and Objectives
The purpose of this analysis is to generate insight into factors predictive of teenage alcohol abuse for the New York City Department of Education.   Adolescence is a critical time of neurological development.  During adolescence the brain is fitting itself to the environment to support behaviors that, ideally promote long term thriving.   Patterns of behavior established before the age of 20 will often persist for the life of the person.  The stimulus alcohol, like all addictive substances, causes a kind of hijacking of the behavioral machinery critical to a good life.   Alcohol is the most widely used intoxicant by teenagers and adults.   This analysis will inform policy in ways that can convert to improved life outcomes for individuals served by the New York City Department of Education.

## Optimizing outcomes for New York City Students
---
The New York City Department of Education serves over one million students annually.  The costs associated with alcohol abuse are wide and deep.  This large public school system has the potential to be a powerful leverage point from which to affect the lives of millions of people.  By identifying high risk students and funneling appropriate resources and interventions in their direction, we can impact millions of individual lives and the character of New York City life in aggregate.  

## The Data 
—
This study uses the Student Alcohol Consumption dataset was collected in 2005-2006.  There are two datasets associated with this study.  One one looks at performance in math classes and the other looks at performance on Portuguese language class.  These Classes were chosen because the researchers found those subjects to be most predictive of school success.  Our study only uses the Portuguese language class set because it is about 50% larger and there is a high number of duplicates among the two sets.   We sourced this dataset from the Kaggle data library.

For this project we only used the dataset containing students who take the Portueguese language course. There are 649 observations and 33 attributes in total.  These original features seem to be designed to provide information about several areas of the student’s life.  Our study grouped these areas as such:

 Academic performance
 Home life
 Support environment
 Social life
 Logistical considerations

To capture this organization with greater interpretability we designed features around these areas.  

## Methods
—
Our preparation of the data involved dummy variable creation, binning alcohol consumption score into high and low categories, and building features around the most important clusters of original features.  
The process of building the model involved extensive optimization of these features around logistic regression and K- nearest neighbors models. 

## Results
—
We used recall as our primary metric to bias efforts towards providing too much support instead of too little.  The final model had a recall score of 65%. The results of our effort confirms what most people would guess without a machine learning classification study of the data… that a more stable and harmonious home life, higher academic performance, and solid support structures around the student tend to predict lower alcohol consumption.  Less harmonious home life, lower academic performance, with lots of idle time and more active social life tend to predict higher alcohol consumption. 

## Conclusions
---
The relatively low recall score seems to point to the idea that identifying high risk students is difficult; in addition, this study does not have the power to identify the primary causes, so we recommend a multi-pronged approach. Interventions should aim several areas that suggest increased risk.  

1.  Family life - Resources allocated at higher level than the Department of Education to promote healthy family structures.  Family planning resources and education, and improved access to mental health resources would be two such areas of investment.
2.  Academic support - tutoring, and mentoring, school
3.  Deterrent efforts - Police resources to target those that might provide alcohol to teenagers and enforcing underage drinking laws.
4.  Idle time - After school activities that can engage less motivated students may help to displace drinking as a recreational activity.

## Further Steps
—
A study designed to reveal the causal relationships among the features would give greater insight into how to prioritize interventions.  My instinct is to say that all of the other observed features derive somehow from the quality of the students’ family environment,  but only a properly designed study can support such a conclusion.  A larger study cohort would be of benefit, and a cohort drawn from New York City Department of Education students would provide the best quality information for these purposes.

## For More Information
---
See the full analysis in the [Jupyter Notebook](___________) or review this [presentation](____________________)

For additional info, contact ___________ at __________________ and _______________ at _____________________


## Repository Structure
---
(Show repo map)
