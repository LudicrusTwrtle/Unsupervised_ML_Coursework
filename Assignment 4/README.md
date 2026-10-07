# COMP_3705
Container for COMP 3705 projects and assignments


Assignment 4: PCA

Group 3
Instructions
	

Objective:
To use Principal Component Analysis (PCA) to enhance clustering and visualization, building on the work completed in Assignment 2. 

Data:
Dataset obtained from Credit Card Dataset for Clustering | Kaggle. Original source unknown. The dataset file is attached below for download. 

Problem Statement:
The marketing department of a credit card company wants to better understand the different types of customers they serve, in order to design marketing strategies that target each group more effectively. As a data scientist, your task is to investigate whether PCA can improve the clustering results and visualization. In the end, you will need to describe each customer group in a way that provides useful insights to the marketing team. 

Steps to Completion:
Create a Jupyter notebook and complete the following steps:

    Data – Copy the relevant section from your notebook for Assignment 2. These steps are included for reference only and are not worth marks.
        Load CC General.csv into a pandas DataFrame and print the header. Use pandas.DataFrame.describe to summarize the data. In a Markdown cell, explain the meaning of each column, make observations based on the summary statistics, and discuss whether they provide useful insights.
        Use pandas.DataFrame.info to check if the entries are the correct data types and if there are any missing values. Use pandas.DataFrame.duplicates to check for duplicate entries. Clean the dataset so there are no missing values, duplicate rows, or incorrect data types. Document the changes and cleaning process in Markdown.
        Drop the 'CUST_ID' column. Use seaborn.heatmap to display the correlation matrix of the features. Use seaborn.pairplot to generate scatter plots and histograms. Record your observations and discuss the insights gained in Markdown. 

    PCA
        Use sklearn.preprocessing.MinMaxScaler to scale the data and print the transformed header. 
        Use sklearn.decomposition.PCA.fit_transform to do a PCA transformation on the data without specifying the number of components. Print out the explained variance ratios and determine how many components are required to retain at least 95% of the explained variance.
        Perform PCA again with n_components set to retain 95% of the explained variance, and save the transformed data to a new DataFrame.

    Clustering
        Create at least 12 clustering models using K-Means, Hierarchical, and DBSCAN, experimenting with different hyperparameter choices.
        Calculate the silhouette score for each model and tabulate the results.
        Select the best model for this use case and justify your choice in Markdown. Compare its silhouette score with your best model from Assignment 2.

    Conclusions
        Generate a scatter plot of the first two principal components of the transformed data. Color the points by cluster assignment. Comment on the plot in Markdown and explain how it compares with your visualization from Assignment 2.
        Generate a histogram showing the number of customers in each cluster and provide observations in Markdown, noting whether cluster sizes make sense.
        For each cluster, create a separate DataFrame from the original (untransformed) data and use pandas.DataFrame.describe to describe customer characteristics.
        Provide a written conclusion summarizing each customer group for the marketing team, based on the summary statistics. Include actionable recommendations derived from the characteristics of each cluster.

Note:
Analyze whether the chosen model produces meaningful and well-separated clusters. If not, revisit your model run by adjusting hyperparameters and trying again. This process of refining, re-running, and re-evaluating the model is an iterative step. Document all iterations and observations in Markdown. Remember that visualizations such as scatter plots of the principal components can provide helpful insight into cluster separation and support the comparison of model performances, but they should be used alongside other evaluation metrics. 

File Naming Convention:
Name your assignment file as follows:
Asg#_Group#_FirstnameLastname1_FirstnameLastname2_FirstnameLastname3
Example: Asg01_Group01_NajmehSaffar_JonZiprick_HosnaSafiarian

Acknowledgment of Group Contributions:
Include a final cell in your notebook titled “Acknowledgment of Contributions.” Clearly list all group members, and have each member indicate whether they are aware of and understand all parts of the work completed, including those they did not personally carry out. Specify the parts of the project each member contributed to, such as data preprocessing, modeling, visualization, or documentation, and highlight any collaborative efforts like reviewing results or interpreting outputs. Be transparent and fair, as grades may be affected if participation was not equitable. Keep the acknowledgment concise while providing enough detail to show each member’s contributions and understanding. 
	
Due on Oct 25, 2026 11:59 PM