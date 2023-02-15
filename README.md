# Cryptocurrencies


The purpose of this project is to create a report that includes what cryptocurrencies are on the trading market and how they could be grouped to create a classification system for the new crypto investment. The original data had to be processed to fit into a machine learning model based on unsupervised learning. To group the cryptocurrencies, we used a clustering algorithm.


---


## Results


* Preprocessing the Data for PCA

We begin by processing the original data. For this, I used Python Pandas to create a data frame, and filter trading cryptos and where rows of data have coins that have been mined.

![1 1](https://user-images.githubusercontent.com/113866707/218630778-d50e983d-f012-48c9-81a1-f4dadd9c4155.png)

After the data was filtered, it was time to prepare the data into numbers for the model to be able to be prepared:

![1 2](https://user-images.githubusercontent.com/113866707/218630793-d723f8ff-a31b-40a2-ade8-66d595749927.png)

I used StandardScaler() to standardize the whole set of data.
![1 3](https://user-images.githubusercontent.com/113866707/218630802-60119150-df3f-42e2-ab33-674ff799eff1.png)


* Reducing Data Dimensions using PCA

For this challenge it was important to apply PCA to reduce the dimensions to 3 principal components:

![2 1](https://user-images.githubusercontent.com/113866707/218630811-25840a59-dbcd-4dae-a24b-4eb531288526.png)

The I created a new DataFrame to show the 3 principal components.

![2 2](https://user-images.githubusercontent.com/113866707/218630823-1f6fcab4-cc53-4f96-bfad-195a48f5ac85.png)



* Clustering Cryptocurrencies using K-means

The following elbow curve, identifies the best value for K at 4:

![3 1](https://user-images.githubusercontent.com/113866707/218630838-a9988d0d-7c19-45d0-a391-b815b1ba4d40.png)

The K-means model is initated considering the 4 clusters:

![3 2](https://user-images.githubusercontent.com/113866707/218630845-0583653e-c117-4f7e-a92c-bd20540e562d.png)

And we can finally present the DataFrame with the 3 Dimensions and the class assigned to each coin:
![3 3](https://user-images.githubusercontent.com/113866707/218630854-41cad18a-d55c-41dc-b529-156966c69e46.png)



* Visualizing Cryptocurrencies results

The following chart is a visualization of the 4 classes of the different coins clustered:

![4 1](https://user-images.githubusercontent.com/113866707/218630865-617eebee-3328-4a3a-9df7-f4ee9b382e57.png)

