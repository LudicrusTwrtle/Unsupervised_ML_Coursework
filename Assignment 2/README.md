# COMP_3705
Container for COMP 3705 projects and assignments


Assignment 1: k-means Clustering
Hide Folder Information
Group Category
	
Assignments
Group Name
	
Group 3
Instructions
	

Objective:
To categorize countries based on socio-economic and health factors that influence the overall development of the country.

Data:
Dataset obtained from Unsupervised Learning on Country Data | Kaggle, by Rohan Kokkula; the original source of the data is unknown. The dataset files are attached below for download.

Problem Statement:
HELP International has raised $100 million. The CEO wants to allocate this money strategically and effectively, focusing on funding programs in the countries most in need of aid. Your job is to categorize the countries using socio-economic and health factors that reflect their overall development. At the end of the analysis, you will need to suggest how to allocate the funds among these countries.

About the Organization:
HELP International aims to create a network of changemakers and social entrepreneurs who understand the complexities of poverty and actively contribute to improving the quality of life for some of the most vulnerable populations in the world.

Steps to Completion:
Create a Jupyter notebook and complete the following steps.

    Data
        Load Country-data.csv into a pandas DataFrame and print out the header. Use pandas.DataFrame.describe to summarize the data. In a Markdown cell, explain the meaning of each column, make observations based on these statistics, and discuss whether they provide useful insights. 
        Use pandas.DataFrame.info to check if the entries are the correct data types and if there are any missing values. Use pandas.DataFrame.duplicates to check for duplicate entries. Clean the dataset so there are no missing values, duplicate rows, or incorrect data types. Document the changes and cleaning process in Markdown. 
        Drop the 'country' column and store it in a separate Dataframe. Use seaborn.heatmap to display the correlation matrix of the features and seaborn.pairplot to generate scatter plots and histograms. Record your observations in Markdown and discuss the insights gained from these visualizations. 

    Modeling
        Use sklearn.preprocessing.StandardScaler to scale the data and print the transformed header. 
        Use sklearn.cluster.KMeans to cluster the data. Try n_cluster values in the range [2, 10] and calculate the silhouette score for each. Create a plot of silhouette score versus number of clusters.
        Choose the best model and, in a Markdown cell, justify the number of clusters selected for this use case. Save the corresponding model as your best model. Remember that the silhouette score is not always a fully reliable metric. It can provide guidance, but other criteria should also be considered when determining the best model. 

    Conclusion
        Based on your step 1 analysis, choose a pair of columns and generate a scatter plot of the data, coloring the points according to their assigned cluster. Comment on the plot in Markdown.
        Generate a histogram showing the number of countries in each cluster and provide observations in Markdown, noting whether the cluster sizes make sense.
        Print the country names in each cluster and comment on whether the results are logical. Rank the clusters from those needing the most aid to those needing the least. Use quick research to build domain knowledge and verify whether the clustering results aligns with real-world conditions, then summarize your findings.
        Describe which countries will receive funds and how much each will get, providing justification for your allocation strategy. 

Note:
Analyze whether the chosen model produces meaningful and well-separated clusters. If not, revisit your model run by adjusting hyperparameters and trying again. This process of refining, re-running, and re-evaluating the model is an iterative step. Document all iterations and observations in Markdown.

File Naming Convention:
Name your assignment file as follows:
Asg#_Group#_FirstnameLastname1_FirstnameLastname2_FirstnameLastname3
Example: Asg01_Group01_NajmehSaffar_JonZiprick_HosnaSafiarian

Acknowledgment of Group Contributions:
Include a final cell in your notebook titled “Acknowledgment of Contributions.” Clearly list all group members, and have each member indicate whether they are aware of and understand all parts of the work completed, including those they did not personally carry out. Specify the parts of the project each member contributed to, such as data preprocessing, modeling, visualization, or documentation, and highlight any collaborative efforts like reviewing results or interpreting outputs. Be transparent and fair, as grades may be affected if participation was not equitable. Keep the acknowledgment concise while providing enough detail to show each member’s contributions and understanding.