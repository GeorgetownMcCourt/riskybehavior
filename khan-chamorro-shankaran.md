# Project Name: Can Risky Behaviors Predict Academic Achievement?

## Synopsis/Overview

The purpose of our project is to address how risky behaviors, such as illegal drug use, alcohol consumption, and sexual intercourse, impact the grades of students in Somerville High School in Massachusetts. More specifically, how do certain behaviors impact the grades of students? However, we recognize that it may be difficult to ascertain causal impacts. In addition, we would also be cautious in how we approached policy recommendations. 

Much of motivation for this project lies in the need for educational reform. We wish to provide insight on how schools can improve to ensure better student outcomes. For example, in order to address tobacco consumption, schools may to wish to increase funding in drug prevention programs. 

## Usage


First, the dataset is recorded from categorical variables into dummy variables. The survey asks students how many times they have engaged in a risky behaviors in the past 30 days.  For example, the variable, cig_30, examines how many days a student has smoked a cigarette in the past 30 days. Respondents had the option to choose 0 days, 1 or 2 days, 3 to 5 days, 6 to 9 days, 10 to 19 days, 20 to 29 days or All 30 days.  In this example, we would recode cig_30 as a binary variable, in that respondents who have never smoked a cigarette, would be coded as a 0, while who respondents have smoked a cigarette at least once, would be coded as a 1. 

In addition, our dependent variable, skl_gra, which examines the grades of students, is also recoded. The variable is recoded on a scale from 1-5, in which a 5 corresponds to “mostly A’s”, while a 1 corresponds to “mostly E’s/F’s.”

Second, the dataset is divided into a 70-15-15 partition. Decision Trees, Random Forest, and Ordered Probit will be considered. The Mean-F1 value, the AUC value, the MAPE value, will be taken into consideration, when determining the optimal technique. The optimal technique will help us to most accurately predict students’ actual grades.

After determining which technique is optimal, we will predict the grades for all the students in the dataset. The optimal model will tell us the extent to which various risky behaviors may play a role in students’ academic outcomes.
                
## Data

The City of Somerville’s Youth Risk Behavior Survey is an annual student survey conducted at Somerville High School. Students at Somerville High School were surveyed every two years, from 2002 to 2014. The dataset includes a total of 8,003 student survey responses. An important attribution of the data is that the survey responses are self-reported. Furthermore, the dataset only examines one high school in Massachusetts, and thus, we cannot generalize the results to other high schools and/or other cities. 

The dataset can be accessed here: http://bit.ly/2nRvJYa.

## Progress Log

*We reviewed the Center for Disease Control (CDC)’s report on the relationship between between health risk behaviors and academic achievement. The report discussed how students with higher grades are significantly less likely to engage in tobacco use, alcohol consumption, and violence-related activities. It should be noted these associations do not prove causation.
Conducted some exploratory analysis of the data (e.g. describing the data, summary statistics).

*We identified variables of interest, which we wish to use in our analysis: grade (skl_gra), gang membership (gang), physical altercation in school (fit_skl), physical altercation outside of school (fit_out), carried weapon in school (weap_skl), carried weapon outside of school (weap_out), self-infliction (hurtself), cigarette use in the past 30 days (cig_30), tobacco chewing in the past 30 days (chew_30), alcohol consumption in the past 30 days (alc_30), marijuana use in the past 30 days (pot_30), cocaine use in the past 30 days (coc_30), heroin in the past 30 days (her_30), meth use in the past 30 days (meth_30), ecstasy use in the past 30 days (x_30), painkiller use without a prescription in the past 30 days (oxy_30), other drugs (oth_30), participation in sexual intercourse (sex_ever), and teen pregnancy (pregnant).  

*We’ve started to clean the dataset and recode the variables. 

*We have also partitioned the data: 70 percent of the dataset is in training set, 15 percent of the dataset is in the testing set, and 15 percent of the dataset is in the validation set.

## Contributors 
Janani Shankaran
Andrea Chamorro
Mariam Khan
