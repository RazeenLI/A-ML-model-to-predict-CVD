# A-ML-model-to-predict-CVD
# 2020-MSA-content/AI & Advanced Analytics/
***
>#### NOTE!
>This project is completed at 7:20am 28/06/2020.
>[Profile URL](https://docs.microsoft.com/zh-cn/users/razeenrunzeli-5739/)
>[Project Home](https://github.com/AUMSA/2020-MSA-content/tree/master/AI%20%26%20Advanced%20Analytics)
 
Machine learning is one of the emerging technologies which has the power to change the world and we would like to enable everyone to harness it power. Hence, in this bootcamp, students from all background will be taught on how to get started with Machine Learning.
 
## Background
 
This is the Microsoft Student Accelerator Australia 2020 bootcamp on AI and Analytics. 
I hope  I can learn the fundamental ideas behind Machine Learning
 
 The goals for this repository are:
1. A well defined specification.
2. An example.
3. A final work for ML
4. A vector for learning Python and Jupyter Notebook
5. A quick process to understand ML
 
## Install
 
This project uses Jupyter Notebook. Go check them out if you don't have them locally installed.
Or, you can use Jupyter Notebook Online provided by Microsoft Azure
the data(.csv) have already included in this repository, I you want to find the original source, click [here](https://www.kaggle.com/cdc/national-health-and-nutrition-examination-survey?select=questionnaire.csv)
 
## Idea
 
At first, I was clueless, but while I was browsing various data, I was suddenly attracted by a daily push of news. This news recounted that CVD is one of the most serious diseases that currently affect people’s deaths, and even many people I don't know if I have this disease.

Then I started to browse various information about CVD and found that the disease was caused by various reasons.

Because the body can be seen as a rigorous machine, this means that any disease will be reflected in certain aspects of the person. Afterwards, I used this logic in reverse. Can these manifestations be regarded as an illness?

Afterwards, I realized that this was a good idea for Ml. I started to look up a lot of data and spent the longest time in each project to filter useful information and complete the project.
 
## Project

This project is based on National Center for Disease Control and Prevention 2013-2014 survey data, National Health and Nutrition Examination Survey.

This data contains at least one thousand survey questions, most of which are missing. But after screening, there are still nearly 5000 data can be used to train the ML.

In various projects,'Gender','Age','Pregnancy','Systolic Blood Pressure','Diastolic Blood Pressure','Cholesterol','Smoke Age','Smoking Frequency','Hypertensive Age','Heredity ','Diabetic Age','Depression','Weight' can all be used as basic data to provide ML,'CVD' is the final reflection.

CVD includes a variety of different CVD.

The same project can partly make up for the problems I have caused by self-learning Python
than - quiting time to get the real somking year(delate unnormal infomation)

## How To Train

1. Select useful data ( 54 factors)
2. import most important thing: import pandas as pd
3. read all information(.csv) I need
4. Put all usefull infomation together to df
5. check whether something lost or not -- Ture
6. collect all part togrther fo unnecessary information 
7. fill in 0 or 1 for with unecessary no NaN)

RIDEXPRG: Pregnancy status for females between 20 and 44 years of age at the time of MEC exam. 
DPQ010~090: NaN meams do not have this problem
BPXDI1~4/BPXSY1~4: mean the different times for checking the blood pressures, 
if donot have any data in 2~4, make it become 0, same with BPXDI1~4
SMD030 means the year of smoking, NAN means nevery smoke
SMQ050Q means time of quit smoking, NAN means nevery smoke or do not quit smoke
SMD057 how many cigarettes did {you/SP} usually smoke per day, NAN means nevery smoke
BPD035 the year of high blood pressure, NAN meanns no
PAD means sport NAN means do not has any sport
NaN means no pregnancy, which means 0 mounth

check other NAN data
delate NaN information
delate unnormal information
Consolidate data
find the average Systolic Blood Pressure, Diastolic Blood Pressure
deal with the most important part, it has MCQ(1) or not(0)
12 there are lotd of unimportant information, just choose useful imformation

## How To Run
deal with smorking and high blood pressure and hypertension
reorder the index

RIDAGEYR is age, SMD030 is start year for smoking, SMD050Q is the time for quiting smoking to now
RIDAGEYR - SMD030 means the year for smoking to now
than - quiting time to get the real somking year(delate unnormal infomation)
f never smok, smokeage = 0

RIDAGEYR is age, DID040 is start year for diabetes
RIDAGEYR - DID040 means the year for diabetes to now

RIDAGEYR is age, BPD035 is start year for hypertension
RIDAGEYR - BPD035 means the year for hypertension to now

redelate useless information, just choose useful imformation
rename this information to better understanding and read
chek the infomation right or not


## How To Tset

data -> attributes(!= CVD, target -> CVD)
x = scaler.fit_transform(data)
80% for training, 20% for testing
check the number of train and test
train it by calling the fit method.
predicted the result 
it already get nearly 100% right, generate an ROC AUC score from the probabilities using scikit-learn's roc_auc_score method
produce a confusion matrix for the model
quantify the precision of the model
measure the model's recall
configures Seaborn to enhance the output from Matplotlib.



## Maintainers
[RazeenLI](https://github.com/RazeenLI)
