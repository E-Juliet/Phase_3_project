# H1n1 Vaccine Prediction

![Picture of a vaccine](https://github.com/E-Juliet/Phase_3_project/blob/main/vaccine.jpg)

## Problem Statement

In 2009, influenza A virus subtype H1N1 (A/H1N1) emerged and spread globally, causing a global pandemic. It contributed to an estimated 151,000 to 575,000 deaths worldwide, or 24% of the global population during the first year it circulated. Till date, the virus continues to circulate seasonally, resulting in 3 to 5 million cases of severe illness and about 290,000 to 650,000 respiratory deaths. 

Vaccines are a key public health measure used to fight infectious diseases like COVID-19. They provide immunization for individuals, and enough immunization in a community can further reduce the spread of diseases through "herd immunity." However, the successes of immunisation programmes are moderated by the level of vaccine uptake in the population. 

The Ministry of Health realised there is a low vaccine uptake in the population,they seek to understand some of the factors that influence the uptake of vaccines,and how they can improve vaccine uptake in future vaccine campaigns.

Vaccines for H1N1 were first publicly available in the United States in October 2009, when the United States government began a vaccination campaign. We will look at data from the National 2009 H1N1 Flu Survey collected to monitor vaccination rates during that campaign. This phone survey asked people whether they had received H1N1 and seasonal flu vaccines, in conjunction with information they shared about their lives, opinions, and behaviors. A better understanding of how these characteristics have been associated with personal vaccination patterns may provide guidance for the Ministry of Health for future vaccination campaigns.

This project will only focus on the H1N1 vaccine,thus the aim is to build a classification model to predict how likely individuals are to receive the H1N1 vaccine.

## Components

__Data__

Data for this project was downloaded from https://www.drivendata.org/competitions/66/flu-shot-learning/

To datasets were used,which were

* Training features 

* Training labels

Description of the columns in the data sets:
The first column __respondent_id__ is a unique and random identifier. The remaining 35 features are described below.

For all binary variables: 0 = No; 1 = Yes.

* h1n1_concern - Level of concern about the H1N1 flu.
0 = Not at all concerned; 1 = Not very concerned; 2 = Somewhat concerned; 3 = Very concerned.

* h1n1_knowledge - Level of knowledge about H1N1 flu.
0 = No knowledge; 1 = A little knowledge; 2 = A lot of knowledge.

* behavioral_antiviral_meds - Has taken antiviral medications. (binary)

* behavioral_avoidance - Has avoided close contact with others with flu-like symptoms. (binary)

* behavioral_face_mask - Has bought a face mask. (binary)

* behavioral_wash_hands - Has frequently washed hands or used hand sanitizer. (binary)

* behavioral_large_gatherings - Has reduced time at large gatherings. (binary)

* behavioral_outside_home - Has reduced contact with people outside of own household. (binary)

* behavioral_touch_face - Has avoided touching eyes, nose, or mouth. (binary)

* doctor_recc_h1n1 - H1N1 flu vaccine was recommended by doctor. (binary)

* doctor_recc_seasonal - Seasonal flu vaccine was recommended by doctor. (binary)

* chronic_med_condition - Has any of the following chronic medical conditions: asthma or an other lung condition, diabetes, a heart condition, a kidney condition, sickle cell anemia or other anemia, a neurological or neuromuscular condition, a liver condition, or a weakened immune system caused by a chronic illness or by medicines taken for a chronic illness. (binary)

* child_under_6_months - Has regular close contact with a child under the age of six months. (binary)

* health_worker - Is a healthcare worker. (binary)

* health_insurance - Has health insurance. (binary)

* opinion_h1n1_vacc_effective - Respondent's opinion about H1N1 vaccine effectiveness.
1 = Not at all effective; 2 = Not very effective; 3 = Don't know; 4 = Somewhat effective; 5 = Very effective.

* opinion_h1n1_risk - Respondent's opinion about risk of getting sick with H1N1 flu without vaccine.
1 = Very Low; 2 = Somewhat low; 3 = Don't know; 4 = Somewhat high; 5 = Very high.

* opinion_h1n1_sick_from_vacc - Respondent's worry of getting sick from taking H1N1 vaccine.
1 = Not at all worried; 2 = Not very worried; 3 = Don't know; 4 = Somewhat worried; 5 = Very worried.

* opinion_seas_vacc_effective - Respondent's opinion about seasonal flu vaccine effectiveness.
1 = Not at all effective; 2 = Not very effective; 3 = Don't know; 4 = Somewhat effective; 5 = Very effective.

* opinion_seas_risk - Respondent's opinion about risk of getting sick with seasonal flu without vaccine.
1 = Very Low; 2 = Somewhat low; 3 = Don't know; 4 = Somewhat high; 5 = Very high.

* opinion_seas_sick_from_vacc - Respondent's worry of getting sick from taking seasonal flu vaccine.
1 = Not at all worried; 2 = Not very worried; 3 = Don't know; 4 = Somewhat worried; 5 = Very worried.

* age_group - Age group of respondent.

* education - Self-reported education level.

* race - Race of respondent.

* sex - Sex of respondent.

* income_poverty - Household annual income of respondent with respect to 2008 Census poverty thresholds.

* marital_status - Marital status of respondent.

* rent_or_own - Housing situation of respondent.

* employment_status - Employment status of respondent.

* hhs_geo_region - Respondent's residence using a 10-region geographic classification defined by the U.S. Dept. of Health and Human Services. Values are represented as short random character strings.

__Jupyter Notebook__

The Jupyter Notebook is our key deliverable and contains details of our approach and methodology, data mining and cleaning, visualisations, conclusions and recommendations.

__Non Technical Presantation__

An overview of the project's objectives,analysis,conclusion and recomendations

## Technologies used

* Python

* Pandas

* Matplotlib

* Seaborn

* Visual Studio Code

## Objectives

* Identify which factors influence the uptake of vaccines

* Build a classification model to predict how likely individuals are to receive the H1N1 vaccine

## Key Findings
![h1n1 knowledge](https://github.com/E-Juliet/Phase_3_project/blob/main/h1n1_knowledge.png))

* Most people had a little knowledge about the h1n1 flu

![seasonal vaccine](https://github.com/E-Juliet/Phase_3_project/blob/main/Seasonal%20Vaccine.png)

* Most people who received the seasonal vaccine also received the h1n1 vaccine

![health insurance](https://github.com/E-Juliet/Phase_3_project/blob/main/Health_Insurance.png)

* Most people who had health insurance took the h1n1 vaccine

![Docctors reccommendation](https://github.com/E-Juliet/Phase_3_project/blob/main/Doctors%20Reccommendation.png)

## Model Evaluation
The best classifier was XGboost with tuned paramters.

Top ten feature importance for the model were:
* Seasonal vaccine

* Doctor recommendation

* health_insurance	

* opinion_h1n1_risk

* opinion_h1n1_vacc_effective	

* doctor_recc_seasonal	

* health_worker	

* h1n1_knowledge	

* opinion_seas_vacc_effective	

* behavioral_wash_hands	

![Model feature importance](https://github.com/E-Juliet/Phase_3_project/blob/main/feature%20importance.png)

__ROC Curve for baseline and final model__

![Roc curves](https://github.com/E-Juliet/Phase_3_project/blob/main/ROC%20curve.png)


## Limitations

* Some columns(employment occupation,employment industry) had more than 50% of the data missing leading to droping the columns,data collection process can improved to see that we dont have large percentage of missing values

* Some columns(employment occupation,employment industry,hhs_geo_region) had values that were not understandable,since they were represented with random character strings which were had to understand the meaning

* Supplementary data analysis.We can explore the motivation for and against seasonal vaccination and make an inference on the variable which have greatest influence. This is because seasonal vaccination is a good predictor of H1N1 vaccination, and data would be more readily available,

## Recomendations

* The minstry of health should invest in ensuring that people have good understanding of a disease and why they need to be vaccinated.Since those who even had a little knowledge on the flu took the vaccine

* They should also not only talk about the disease but also ensure they explain how efective the vaccine is,and how it works to clear any doubts

* Doctors should encourage the uptake of vaccine as patients visit them.

* The ministry of health should also emphasize on the importance of taking health insurance and put in policies to make it affordable for people to get.


