# COMP_3705
Container for COMP 3705 projects and assignments


Assignment 2: DBSCAN

Group 3
Instructions
	

Objective:
To categorize patients based on their symptoms into groups that represent different levels of urgency, with special focus on identifying all patients who need immediate resuscitation. 

Data:
Dataset obtained from Patient Priority for Clustering | Kaggle, created by Hossam Ahmed Aly. Original source unknown. The dataset file is attached below for download. 

Problem Statement:
Triage is the process of prioritizing patient care (or disaster victims) based on severity, symptoms, prognosis, and resource availability. The goal is to identify patients requiring immediate resuscitation, assign patients to appropriate care areas, and initiate necessary diagnostic or therapeutic measures. As a data scientist, your task is to cluster the patients according to their symptoms and assign urgency levels to each group. It is critical that patients in need of immediate resuscitation are accurately identified. 

Steps to Completion:
Create a Jupyter notebook and complete the following steps. 

    Data
        Load patient_priority.csv into a pandas DataFrame. Drop the 'triage' column and print the header. Use pandas.DataFrame.describe to summarize the data. In a Markdown cell, explain the meaning of each column, make observations based on the summary statistics, and discuss whether they provide useful insights.
        Use pandas.DataFrame.info to check if the entries are the correct data types and if there are any missing values. Use pandas.DataFrame.duplicates to check for duplicate entries. Clean the dataset so there are no missing values, duplicate rows, or incorrect data types. Document the changes and cleaning process in Markdown. 
        Use pandas.get_dummies to one-hot-encode any categorical (string) columns.
        Use seaborn.heatmap to display the correlation matrix of the features. Use seaborn.pairplot to generate scatter plots and histograms. Record your observations and discuss the insights gained in Markdown. 

    Modeling
        Use sklearn.preprocessing.MinMaxScaler to scale the data and print the transformed header.
        Use sklearn.cluster.DBSCAN to cluster the data. Create at least 10 different models using various hyperparameter combinations (eps, min_samples, metric, p). Calculate the silhouette score for each model and tabulate the results. 
        Select the best model for this use case and justify your choice in Markdown. If initial models do not produce meaningful clusters, try additional hyperparameter settings and document any iterations and observations. 

    Conclusions
        Choose a pair of features and generate a scatter plot of the data, coloring points according to the clusters assigned by your best model. Comment on the plot in Markdown.
        Generate a histogram showing the number of customers in each cluster and provide observations in Markdown, noting whether cluster sizes make sense.
        Create a separate DataFrame for each cluster and use pandas.DataFrame.describe to describe each group.

        Provide a written conclusion summarizing the characteristics of each patient group and rank the urgency level for each cluster. Include actionable recommendations for how the clusters could be used in a triage system.

Note:
Analyze whether the chosen model produces meaningful and well-separated clusters. If not, revisit your model run by adjusting hyperparameters and trying again. This process of refining, re-running, and re-evaluating the model is an iterative step. Document all iterations and observations in Markdown.

File Naming Convention:
Name your assignment file as follows:
Asg#_Group#_FirstnameLastname1_FirstnameLastname2_FirstnameLastname3
Example: Asg01_Group01_NajmehSaffar_JonZiprick_HosnaSafiarian

Acknowledgment of Group Contributions:
Include a final cell in your notebook titled “Acknowledgment of Contributions.” Clearly list all group members, and have each member indicate whether they are aware of and understand all parts of the work completed, including those they did not personally carry out. Specify the parts of the project each member contributed to, such as data preprocessing, modeling, visualization, or documentation, and highlight any collaborative efforts like reviewing results or interpreting outputs. Be transparent and fair, as grades may be affected if participation was not equitable. Keep the acknowledgment concise while providing enough detail to show each member’s contributions and understanding. 