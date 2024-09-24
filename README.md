
# MNIST Digits Project

The goal of this project was to apply both supervised and unsupervised learning techniques to the MNIST digits dataset and explore the feasibility of reducing the high-dimensional (784-feature) images into lower-dimensional objects for classification. The project's focus was to compare these methods with traditional neural networks.

## 1. Data Preprocessing

- **Dataset Acquisition**: Loaded MNIST using `tensorflow.keras.datasets`.
- **Data Preparation**: Reshaped 28x28 images into 1D arrays of 784 features. 
- **Visualization**: Examined the distribution of 6000 samples and displayed digit images.

## 2. PCA and Clustering

- **Principal Component Analysis**: PCA was applied to reduce dimensions, but 2D embeddings did not distinctly scatter digits, limiting classification performance.
- **Clustering**: KMeans and spectral clustering were attempted on 3, 4, and 10-dimensional embeddings. 10D showed slightly more separability, hinting that KNN could work well for higher dimensions.

## 3. KNN on the Embeddings

- **Grid Search for Hyperparameters**: Used custom grid search for optimal KNN parameters. The model achieved 90.6% validation accuracy on 15 principal components.
- **Test Results**: Achieved 89.5% accuracy on the test set using KNN.
- **Comparison to CNNs**: CNNs, which are commonly used for this problem, perform much better, reaching accuracies up to 98.4%.

