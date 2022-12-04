<h1 align="center"> Brain Tumor Classification Model</h1>

This project recollects a deep neural network model to detect tumor in mri brain images. The dataset of training and testing images can be downloaded on Kaggle at: [Brain Tumor Classification (MRI)](https://www.kaggle.com/datasets/sartajbhuvaji/brain-tumor-classification-mri/code?resource=download). 

The dataset considers four different classes: no tumor, glioma tumor, meningioma tumor and pituitary tumor. 

## Model
After downloading the dataset, the file model.ipynb can be run. The training data is augmented, a validation set is considered as the 25% of the training set and the VGG16 model is used as a pretrained model to further modification and training.

The program was run on Colab for the use of GPU. Version of Tensorflow used is 2.9.2.

## Data Visualization
In file model.ipynb, the training data can be visualised in a grid of images eith the function visualize_data. 

In file evaluate_model.ipynb, the testing data with guessed and true classes is shown in grids where the images are picked randowmly. An example of such grid is the following:

![guess-true-plot-figures_02](https://user-images.githubusercontent.com/112558042/205520901-85301848-c21e-4f42-bbbb-068e3a90009b.jpg)

Other grids generated can be find in the folder plots.

## Evaluation 
The model can be evaluated on the testing set by running the file evaluate_model.ipynb. Here, the accuracy reached on the testing set is 75.38%.
The computation of the confusion matrix on the testing set is also present in file evaluate_model.ipynb, and it is the following:
![confusion_matrix](https://user-images.githubusercontent.com/112558042/205520961-cc491473-f34c-43e4-a4c5-a2c6bee38e53.jpg)

In the matrix, it is evident that the model still has difficulties in recognizing the glioma tumor, in particular by considering it as a meningioma tumor.



### Further TODO improvements:
In future, the idea is to increase the testing accuracy by adding further regularization in the structure of the model. Also, I intend of adding some hyperparameters tuning.
