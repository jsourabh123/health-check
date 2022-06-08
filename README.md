# Plant-Medicasre

## problem Statment 
#### In the early days, the monitoring and diagnosis of plant disease were done by the expert person and was time taking and not reliable method so to overcome this drawback we develop an system for wellness detection and diagnosing purpose. In order to manage plant leaf diseases effectively, it is required to introduce an method of plant surveillance that can scrutinize plant condition and apply the knowledge-based solution to detect and classifying various diseases.

### Solution Summary

#### This is a classic example of Image Classification.So we got the data from kaggle which is divide into 13 different catogories such as Potato_late_Blight,tomato_Early_Blight,tomato_late_Blight,Patato_healthy, Tomato__Target_Spot etc.So,first we need to create BatchDataset of these images(256*256) in batches of 32.Then we will convert these images into array of (256*256*3) here 3 is colour channels i.e red,blue and green. Now we divide the dataset into 3 different datasets i.e training(.8),validation(.1) and testing(.1). Before we feed our images to network, we had shuffled, prefetch and cache these 3 datasets.Also, we had resized and resacle the images to desired size. Moreover, to improve model performance we need to do Data Augmentation as this boosts the accuracy of our model.In model creation we have used 4 different layering method(Conv2D, Maxpooling, Flatten and dense). we use relu as activation function for inner layer and softmax for output layer.To Compile the model, We use adam as Optimizer, SparseCategoricalCrossentropy for losses, accuracy as a metric.we got accuracy as 97% and below is garph of training and validation accuracy and loss against number of Epochs.

![image](https://user-images.githubusercontent.com/43174715/172567503-64397254-1752-4d1a-99d9-2480c6a3bf7d.png)

Below is sample test for evalution the model

![image](https://user-images.githubusercontent.com/43174715/172567973-cf1e548a-600c-4d89-ac80-f45e2b78e9f7.png)

we also develop a web page were user can come, upload image and use model to detect disease.

![image](https://user-images.githubusercontent.com/43174715/172568272-c1891f38-ca92-4f96-9e7c-098aa99b9c8d.png)

