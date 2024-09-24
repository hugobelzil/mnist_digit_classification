
# MNIST Digits Project

The goal of this project was to implement a few supervised and unsupervised learning techniques to the famous MNIST digits dataset to observe if the 784-dimensional (28x28) pictures could be reduced (or not!) into lower-dimensional objects for classification purposes. We wish to compare our results with accuracies obtained by "traditional" neural networks approaches.

Implementation on Python using Pandas, NumPy and Sci-Kit Learn, across 3 different notebooks (see [here](https://sites.google.com/view/hugobelzil/projects/mnist-project?authuser=0))


## Data Preprocessing

- **Dataset Acquisition**: Loaded MNIST using `tensorflow.keras.datasets`.
- **Data Preparation**: Reshaped 28x28 images into 1D arrays of 784 features. 
- **Visualization**: Examined the distribution of 6000 samples and displayed digit images.

## PCA and Clustering

- **Principal Component Analysis**: PCA was applied to reduce dimensions, but 2D embeddings did not distinctly scatter digits (see the graph in the notebooks), limiting classification performance.
- **Clustering**: KMeans and spectral clustering were attempted on 3, 4, and 10-dimensional embeddings. 10D showed slightly more separability, hinting that KNN could work well for higher dimensions, which we investigate in the next part of the project.

## KNN on the Embeddings

- **Grid Search for Hyperparameters**: Used custom grid search for optimal KNN parameters. The model achieved 90.6% validation accuracy on 15 principal components.
- **Test Results**: Achieved 89.5% accuracy on the test set using KNN.

## Conclusion

We finally obtain an 89.5% accuracy over our testing data. Note however that classifying MNIST digits is a famous problem and many techniques exist, including ones that perform much better. Traditionally, ML scientist have used convolutional neural networks (CNNs) for image classification, which turn out to produce classifications with much higher accuracies. Indeed, "small" networks can achieve up to 98.4% accuracy, and most likely even more for deeper networks. See [https://medium.com/analytics-vidhya/get-started-with-your-first-deep-learning-project-7d989cb13ae5](We finally obtain an 89.5% accuracy over our testing data. Note however that classifying MNIST digits is a famous problem and many techniques exist, including ones that perform much better. Traditionally, ML scientist have used convolutional neural networks (CNNs) for image classification, which turn out to produce classifications with much higher accuracies. Indeed, "small" networks can achieve up to 98.4% accuracy, and most likely even more for deeper networks. See https://medium.com/analytics-vidhya/get-started-with-your-first-deep-learning-project-7d989cb13ae5
)

