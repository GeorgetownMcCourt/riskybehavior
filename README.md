# riskybehavior
Can Risky Behaviors Predict Academic Achievement?
## Synopsis/Overview

For several decades, the academic performance of students has been a major concern. Many studies have discovered that academic success has been strongly linked with health-related factors. According to the Centers for Disease Control and the 2009 National Youth Risk Behavior Survey (YRBS), there is a negative association between health-risk behaviors and academic achievement among high school students. In other words, students with higher grades are less likely to engage in health-risk behaviors than students with lower grades. Similarly, students who do not engage in health-risk behaviors are more likely to receive higher grades than students who engage in health-risk behaviors. It should be noted these associations do not prove causation.

The objective of this study is to build upon the CDC research in order to better understand how certain behaviors may impact or be associated with student grades. These results can encourage schools to promote health and safety among students, which would in turn enable students to establish lifelong healthy behaviors.

## Usage

First, we recoded categorical variables within the dataset into dummy variables. The survey asks students how many times they have engaged in a risky behaviors over the past 30 days.  For example, the variable "cig_30" examines how many days a student has smoked a cigarette in the past 30 days. Respondents had the option to choose 0 days, 1 or 2 days, 3 to 5 days, 6 to 9 days, 10 to 19 days, 20 to 29 days or All 30 days.  In this example, we recoded cig_30 as a binary variable, in that respondents who have never smoked a cigarette would be coded as a 0, while who respondents have smoked a cigarette at least once would be coded as a 1. 

Our dependent variable, skl_gra, which examines the grades of students, was also recoded on a scale from 1-5, in which a 5 corresponds to “mostly A’s”, while a 1 corresponds to “mostly E’s/F’s.”

Second, we divided the data into a 70-15-15 partition. We employed methodologies such as Decision Trees, Random Forest, and Ordered Logistic Regression to assess whether any of the independent variables can predict student grades. Diagnostics include the Mean-F1 and the AUC value. 

The optimal method will tell us the extent to which various risky behaviors may play a role in students’ academic outcomes.
                
## Data

The City of Somerville’s Youth Risk Behavior Survey is an annual student survey conducted at Somerville High School. Students at Somerville High School were surveyed every two years, from 2002 to 2014. The dataset includes a total of 8,003 student survey responses. An important attribution of the data is that the survey responses are self-reported. Furthermore, the dataset only examines one high school in Massachusetts, and thus, we cannot generalize the results to other high schools and/or other cities. 

The dataset can be accessed here: http://bit.ly/2nRvJYa.

## Progress Log

*We reviewed the Centers for Disease Control (CDC)’s report (http://bit.ly/2p5mSni) on the relationship between between health-risk behaviors and academic achievement. The report discussed how students with higher grades are significantly less likely to engage in tobacco use, alcohol consumption, and violence-related activities. It should be noted these associations do not prove causation.
Conducted some exploratory analysis of the data (e.g. describing the data, summary statistics).

*We identified variables of interest, which we wish to use in our analysis: grade (skl_gra), gang membership (gang), physical altercation in school (fit_skl), physical altercation outside of school (fit_out), carried weapon in school (weap_skl), carried weapon outside of school (weap_out), self-infliction (hurtself), cigarette use in the past 30 days (cig_30), tobacco chewing in the past 30 days (chew_30), alcohol consumption in the past 30 days (alc_30), marijuana use in the past 30 days (pot_30), cocaine use in the past 30 days (coc_30), heroin in the past 30 days (her_30), meth use in the past 30 days (meth_30), ecstasy use in the past 30 days (x_30), painkiller use without a prescription in the past 30 days (oxy_30), other drugs (oth_30), participation in sexual intercourse (sex_ever), and teen pregnancy (pregnant).  

*We  partitioned the data: 70 percent of the dataset is in training set, 15 percent of the dataset is in the test set, and 15 percent of the dataset is in the validation set.

*We used the following techniques: Ordered Logistic Regression, Decision Trees, and Random Forest. 

## Results 

Gender and marijuana use were identified as important variables across all three methods. Cigarette use, sexual activity, alcohol consumption, pregancy, age and race were also identified as important variables in more than one method. However, given the limitations of our methods, we remain cautious in further interpreting these results.

Overall, random forest is the preferred method; however, there is low predictability power. This may be attributed to the limitations of the data. Other factors not contained within the YRBS dataset may better predict grades, such as household type, family stability, and the income of parents. Furthermore, issues associated with self-reported data, including missing data and measurement error, may diminish model predictability. Given the limitations of this analysis, more research should be conducted in this area to better inform schools and policymakers.

## Contributors 
Janani Shankaran,
Andrea Chamorro, and
Mariam Khan
