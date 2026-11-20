# COMP_3705
Container for COMP 3705 projects and assignments

Assignment 6: T-SNE

Group 3
Instructions

Objective:
To determine whether a dataset is suitable for classification and identify potential challenges that may affect model performance. 

Data:
Dataset obtained from Arabic Handwritten Digits Dataset | Kaggle, Original source unknown. The dataset file is attached below for download. 

Problem Statement:
Continuing with your work on a team developing a mobile app for hand calculations in Arabic (begun on Assignment 5), you will now perform a clustering analysis to determine how well you can expect a classification model to work on this data. The app will require a neural network to classify hand-drawn digits in order to correctly complete the calculations. Using clustering, we can determine whether the classes are well separated and identify where a classification model may struggle. Using a dataset of hand-drawn Arabic digits, where each image corresponds to a point in a 784-dimensional space, you are to complete a clustering analysis and visualize the results in a two-dimensional plot. 

Arabic Digits:
Arabic digits correspond to Roman digits as described in N. Das, A. Mollah, S. Saha, S. Haque, 2010 (https://arxiv.org/abs/1003.1891). 

Steps to Completion:
Create a Jupyter notebook and complete the following steps:

    Data – Copy the relevant section from your notebook for Assignment 5. These steps are included for reference only and are not worth marks. 
        Each row of csvImages 10k x 784.csv contains the grayscale values of a 28×28 image. Load this data into a pandas DataFrame and convert it to a NumPy array using pandas.values. Print the shape of the data.
        Normalize the values by dividing by 255. To display the images, reshape each array to 28×28 using numpy.ndarray.reshape. Use matplotlib.pyplot.imshow and matplotlib.pyplot.subplot to plot the first five images using the 'gray' colormap.
        Reshape each image back to a one-dimensional array of size 784 for clustering. 

    Clustering
        Use sklearn.decomposition.PCA.fit_transform to perform PCA with n_components = 40. This reduces the dimension of each image to a size that is more manageable, while keeping the most important aspects of the data. 
        Create at least 8 clustering models using K-Means, Hierarchical, and DBSCAN, experimenting with different hyperparameters. 
        Calculate the silhouette score for each model and tabulate the results.
        Select the best model for this use case and justify your choice in Markdown. 

    t-SNE
        Use sklearn.manifold.TSNE to perform dimensional reduction on the dataset using t-SNE with n_components = 2. Try at least 8 different runs using different choices for perplexity, n_iter, and metric.
        Provide a scatter plot using the t-SNE components as coordinates, coloring the points according to cluster membership.
        Print the Roman digit corresponding to each cluster at its centroid. 
        In Markdown, explain which plot provides the best visualization. You may revisit the clustering models in step 2 to improve your results. 

    Conclusions
        Display your best t-SNE plot of your best model and restate the hyperparameter choices.
        In Markdown, discuss how well suited this dataset is for classification. Identify any digit classes that may be confused by a classification model.
        In Markdown, explain why using PCA-reduced data is preferred over the original high-dimensional data as input for clustering and t-SNE visualization in some cases, and describe how to determine whether PCA-reduced data is appropriate to use and, if so, how to decide on the number of principal components to retain. 

Note:
Analyze whether the chosen model produces meaningful and well-separated clusters. If the results are not satisfactory, revisit the model run by adjusting hyperparameters and trying again. This cycle of refining, re-running, and re-evaluating is part of the iterative process. Document all iterations and observations in Markdown. Remember, t-SNE can be used as a visualization technique to help compare model performances, but it should be considered a supporting visualization rather than a definitive measure of cluster quality. 

File Naming Convention:
Name your assignment file as follows:
Asg#_Group#_FirstnameLastname1_FirstnameLastname2_FirstnameLastname3
Example: Asg01_Group01_NajmehSaffar_JonZiprick_HosnaSafiarian

Acknowledgment of Group Contributions:
Include a final cell in your notebook titled “Acknowledgment of Contributions.” Clearly list all group members, and have each member indicate whether they are aware of and understand all parts of the work completed, including those they did not personally carry out. Specify the parts of the project each member contributed to, such as data preprocessing, modeling, visualization, or documentation, and highlight any collaborative efforts like reviewing results or interpreting outputs. Be transparent and fair, as grades may be affected if participation was not equitable. Keep the acknowledgment concise while providing enough detail to show each member’s contributions and understanding. 