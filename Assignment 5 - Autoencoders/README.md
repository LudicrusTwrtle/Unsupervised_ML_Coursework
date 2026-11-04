# COMP_3705
Container for COMP 3705 projects and assignments

Assignment 5: Autoencoders

Group 3
Instructions

Objective:
To store a set of images using a minimal amount of data by training an autoencoder on handwritten Arabic digits. 

Data:
Dataset obtained from Arabic Handwritten Digits Dataset | Kaggle. Original source unknown. The dataset file is attached below for download. 

Problem Statement:
You are part of a team developing a mobile app for performing arithmetic with handwritten Arabic digits. The app will recognize digits in the user’s handwriting. Your task as a developer is to encode each hand-drawn digit using as little memory as possible while preserving the ability to reconstruct the images. Using the dataset of handwritten Arabic digits, you will train an autoencoder to encode and decode these images efficiently.

Arabic Digits:
Arabic digits correspond to Roman digits as described in N. Das, A. Mollah, S. Saha, S. Haque, 2010 (https://arxiv.org/abs/1003.1891).

Steps to Completion:
Create a Jupyter notebook and complete the following steps:

    Data
        Each row of csvImages 10k x 784.csv contains the grayscale values of a 28×28 image. Load this data into a pandas DataFrame and convert it to a NumPy array using pandas.values. Print the shape of the data.
        Normalize the values by dividing by 255. To display the images, reshape each array to 28×28 using numpy.ndarray.reshape. Use matplotlib.pyplot.imshow and matplotlib.pyplot.subplot to plot the first five images using the 'gray' colormap.
        To prepare the data for input to the neural network, reshape each image back into a one-dimensional array of size 784.

    Modeling
        Use keras.layers to create an input layer matching the dimensions of your data. 
        Use keras.layers to create an encoding stage with at least two layers that reduces the data size to 50% or less (smaller is better). Choose appropriate activation functions.
        Use keras.layers to create a decoding stage with at least two layers that restores the data to its original size. Choose appropriate activation functions. 
        Compile the complete autoencoder network, selecting a suitable loss function and optimizer, and train the network on the image data. 
        Compile the encoder network using your trained input layer and encoding stage. 

    Conclusions
        Use matplotlib.plot.imshow, matplotlib.plot.subplot, and your trained models to plot the first five original images along the top row, the encoded versions along the second row, and the decoded versions along the bottom row.
        Adjust the hyperparameters of your model as needed to produce decoded images that closely represent the originals while minimizing the encoding size. Record all adjustments in Markdown.
        Describe in Markdown how well the autoencoder is performing, referencing the plots.
        Calculate the amount of data needed to store a single image, assuming a floating-point number requires 4 bytes. Compute the percentage of memory saved using your encoding.

File Naming Convention:
Name your assignment file as follows:
Asg#_Group#_FirstnameLastname1_FirstnameLastname2_FirstnameLastname3
Example: Asg01_Group01_NajmehSaffar_JonZiprick_HosnaSafiarian

Acknowledgment of Group Contributions:
Include a final cell in your notebook titled “Acknowledgment of Contributions.” Clearly list all group members, and have each member indicate whether they are aware of and understand all parts of the work completed, including those they did not personally carry out. Specify the parts of the project each member contributed to, such as data preprocessing, modeling, visualization, or documentation, and highlight any collaborative efforts like reviewing results or interpreting outputs. Be transparent and fair, as grades may be affected if participation was not equitable. Keep the acknowledgment concise while providing enough detail to show each member’s contributions and understanding. 