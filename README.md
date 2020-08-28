
Women Who Code - Mission: Predictable
A Virtual Machine Learning Hackathon to Battle Covid-19

<IMG SRC="./Blacks_Covid19_sm.png" ALT="Blacks_Covid19">


_CDC / GETTY / THE ATLANTIC_
Project Submission
TEAM: #34
Student name: Sharonda Pettiett-Warner and Omega Markos
Submission Date: Friday, August 14, 2020
Your mission, should you choose to accept it, involves forming a team and putting your newfound skills to use in the battle against COVID-19.

Problem Statement
COVID-19 is a global crisis impacting millions of people world-wide. Specifically in the US, the disparities between the size of the black population and the percentage of black people infected with, hospitalized with, or dead from COVID-19 appear to be the most severe.

To battle this inequality our team has chosen to build an unsupervised machine learning model using K-means clustering to perform population segmentation and use dimensionality reduction techniques like PCA to evaluate a large number of features. These features, include US Census Data; US COVID-19 cases, deaths and policies to help us discover new trends and patterns in solving this crisis impacting the black communities in the US.

COVID-19 Death Rates Higher in Blacks

Blacks are dying at a rate higher than all others races in America

The share of the Black population is 13%, while the deaths for Blacks is 22% (as of July 22, 2020)

Population

31% of the States in America are above the National average for Black Deaths (of 22% ).

States

The Dataset
Our team analyzed COVID-19 policies, cases and deaths by state and race using the most recent U.S. Census data and the latest information we could gather on COVID-19 events and news articles.

We mined the following datasets to gain insights into this pandemic affecting Black America:

Policy Datasets: https://docs.google.com/spreadsheets/d/1zu9qEWI8PsOI_i8nI_S29HDGHlIp2lfVMsGxpQ5tvAQ/edit?ts=5f16268f#gid=973655443 https://www.dropbox.com/sh/z8mhrb0r1t4rlqu/AAB3Ykn2uxzffKDnjWJEayz4a/Essential%20businesses?dl=0&subfolder_nav_tracking=1

State of Emergency - The date the state declared state of emergency.
Physical Distance Closures
Stay at Home Policies
Reopening businesses dates & policies
Second Closures
Face Masks
Quarantine Rules
Alcohol and Firearms
Housing
Unemployment Insurance
Food Security
Healthcare Delivery
Racial Disparities
Incarcerated Individuals
Substance Use Disorder Policies
Pre-Covid Policies
State Characteristics
Deaths & Population Distributions by Race Dataset: https://data.cdc.gov/NCHS/Distribution-of-COVID-19-deaths-and-populations-by/jwta-jxbg/

Cases and Deaths by Race Dataset: https://docs.google.com/spreadsheets/d/e/2PACX-1vR_xmYt4ACPDZCDJcY12kCiMiH0ODyx3E1ZvgOHB8ae1tRcjXbs_yWBOA4j4uoCEADVfC1PS2jYO68B/pub?gid=43720681&single=true&output=csv

Computer & Internet Use Dataset: https://covid19.census.gov/datasets/computer-and-internet-use-counties/data?geometry=138.304%2C-16.868%2C-137.673%2C72.108

Health insurance Dataset: https://covid19.census.gov/datasets/health-insurance-coverage-states?geometry=138.304%2C-16.868%2C-137.673%2C72.108

Language Spoken at Home Dataset: https://covid19.census.gov/datasets/language-spoken-at-home-counties/data?geometry=138.304%2C-16.868%2C-137.673%2C72.108

Population Poverty Rates Dataset: https://covid19.census.gov/datasets/population-and-poverty-states?geometry=138.304%2C-16.868%2C-137.673%2C72.108

Dataset Notes:

After merging these datasets we arrived at a total of 246 features by state.
All of the datasets were collected as of July 22 2020.
Acknowledgements
Women Who Code, Non-profit organization
Amazon Web Services, IT service management company (providing the AWS credits)
Kesha Williams, A Cloud Guru (Our Guru, for getting us excited about this project, Thanks!)
How to Navigate Jupyter Notebooks
Order of Navigation:

Part I : Jupyter Notebook: Battle Covid-19 Project - Data Mining .ipynb
Part II : Jupyter Notebook: Battle Covid-19 Project - Data Visualization .ipynb
Part III : Jupyter Notebook: Battle Covid-19 Project - Machine Learning.ipynb
Learning Concepts and Tools
Data Science Concepts Used:

Machine Learning (ML)
Data Visualization
Data Cleaning
Data Exploration
Feature Engineering
Tools Used:

AWS Sagemaker for developing, training and deploying model via the cloud infrastructure.
Plotly's Python graphing library makes interactive, publication-quality graphs.
Machine Learning Models Used:

PCA
K-means Clustering
Project Summary
Project Motivation
Our team spent several days discussing what potential factors were impacting the Black communities in America during this pandemic. We read that factors such as pre-existing conditions and being a front-line worker were some of the key factors in understanding why Blacks were more infected and more susceptible to dying from the virus. What we wanted to accomplish in this WWC Battle Covid-19 Hackathon was to use machine learning to uncover more insights into the .... Why?... And find out, if ... Disasters do Discriminate.

Problem Description
Our analysis found that COVID-19 impacting Black Deaths in 36 states, is higher than their population share.

Distribution 2

Machine Learning Modeling
To better understand the impact of Black Deaths in the US related to COVID-19, our team analyzed COVID-19 policies, cases and deaths by state and race using the most recent U.S. Census data. Equipped with more insightful information we chose to use unsupervised machine learning and dimensionality reduction techniques to identify clusters within the datasets to learn, from the properties of the data.

Our machine learning approach included performing the following key tasks:

Demonstrating how to build PCA and K-means clustering training models using Sklearn libraries
Demonstrating how to build and deploy PCA and K-means clustering training models using AWS Sagemaker
In our evaluation of building PCA model in AWS Sagemaker, we examined the makeup of each PCA component based on the weightings of the original features that are included in the component. For example, the following image shows PCA Component Makeup: #3. This component describes attributes of states that have high poverty, high Black deaths and cases, high indicators for ending stay at home policies and initiating re-opening mandates. These insights proved to be very valuable for us in the population segmentation process using K-means clustering.

PCA Component Makeup: #3

PCA_3

K-means is a clustering algorithm that identifies clusters of similar states based on their attributes. Since we had 228 attributes in our original dataset, the large feature space may have made it difficult to cluster the states effectively. Instead, we reduced the feature space to 5 PCA components and implemented K-means algorithm to create (4) clusters.

K-means | 4 Clusters

Cluster_Size

In order to draw conclusions from our model, we evaluated the cluster centers. These centers helped to describe which features were characterize in each cluster. By combining PCA and K-means clustering, the information contained in the model attributes within the trained model, enabled us to gain more insights on the data.

Combining PCA and K-means

Centoids

Using unsupervised learning, we clustered a dataset using K-means after reducing the dimensionality using PCA. By accessing the underlying models created within Amazon SageMaker, we were able to improve the explainability of our modelling and draw actionable conclusions. Using these techniques, we have been able to better understand the characteristics of different states in the US and segment them into groupings accordingly.

Based on our analysis we found Cluster 2, had a high correlation with the PCA component for BelowPoverty/DeathBlackPercent.

Analysis of Cluster 2

Cluster_2_States_Data

In our analysis of the all of the clusters, we found that Cluster 2 best described how blacks in these states were being impacted by COVID-19. This process revealed new features strongly associated with this segmentation, such as, high poverty, high Black deaths and cases, high indicators for ending stay at home policies and initiating re-opening mandates.

Cluster 2 Data Visualization Insights:

Cluster 2: Has the highest Percent living under the federal poverty line (2018) (16%)
Cluster 2: Has the second most PercentofPopulationwithNoHealthInsuranceCoverage (11%)
Cluster 2: Relaxed the the Stay at home policy earlier than the rest of the states based on the number of days after the date of emergency was issued for that state.
Cluster 2: Less social distancing.
Cluster 2: Has the most Percent Unemployed (2018) (6%)
Cluster 2: With the lowest (almost none) - This cluster may not be encourged to stay at home when sick because they do not have paid sick leave.
Cluster 2: Re-open with face masks.
Cluster 2: Has the lowest percent of housholds with Internet at Home.
Cluster 2: Less likely to work and learn from home.
Cluster 2: Re-open businesses earlier than the other states.
Cluster 2: Did not take advantage of the extra stimulus provided with the Weekly unemployment insurance.
Battle COVID-19 | Conclusions
This study, now answers our original question - Do Disasters Discriminate? YES.

Key Findings

41.4% At Risk for serious illness due to COVID-19 (highest)
15.47% Households: Income Below Poverty Level (highest)
32.39% Deaths_Black (highest)
18.4% Cases_Black (highest)
15.6% Living under federal poverty line as of 2018 (highest)
Did not stay at home; Had to participate in the reopenings
Has high Black Death Percent
Below Poverty
Living under Federal Poverty Line
Battle COVID-19 | Recommendations
The data and our analysis on how COVID-19 is impacting the black communities disproportionately in the United States reveals a link that’s hard to ignore between race, poverty, cases and deaths in America.

Our analysis demonstrates the following features that are impacted:

by Government Policies

Relaxing stay at home measures
Initiating early business re-opening
Obtaining health insurance
Obtaining paid sick leave
by Socioeconomic Issues

Living under Federal Poverty Line
Unemployment
Access to Internet
These factors also indicate an infrastructure issue in America and the need for having a National Policy on Health Care and Income Inequities.

Our recommendations involve having meaningful actions to support these communities and protect public health could include protective policies for workers, including paid sick leave and provision of health insurance. For high poverty and unemployment policymakers should work to address minimizing the income inequality gap.

During the pandemic to address poverty and unemployment we need to identify the black populations which need additional access to resources such as testing, personal protective equipment, education, and support to implement recommended social distancing practices; support food pantries and meal delivery services for food assistance; and relief funds are available to the communities most in need by streamlining application processes and allowing for extensions of subsidies when the crisis begins to subside.

Team_34
