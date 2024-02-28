# Dataset
Dataset source: https://www.kaggle.com/datasets/asaniczka/mammals-image-classification-dataset-45-animals

# About models
In the project Xception, VGG16, ResNet50, InceptionV3, DenseNet121 and MobileNetV2 models were train for image classification. Most promising model is Xception because it has the highest accuracy. ResNet was the worst model for this task. The biggest surprise for me was speed of the MobileNet - this model learned fastest and accuracy is comparable with Xception and Inception's accuracy.

# Best model's performance:
Accuracy on test dataset is about 97.58% and weighted F1 score is about 97.59%.

# What could be done better?
There are many options to improve accuracy but I couldn't afford to do this due to lack of RAM. There is possibility to regularize Xception model (check which optimizer will be the best one, experiment with learning rate, momentum and decay). There is also possibility to concatenate two or three best models into one ensemble model.

The reason why models haven't higher accuracy is that input shapes of images in training dataset were different than expected ones (DenseNet, MobileNet, ResNet and VGG expect size = (224, 224), Inception and Xception - (299, 299)). I couldn't perform training of such a image sizes because of lack of RAM for such a calculations. Also preprocess_input function should be performed on the images for every model but again, lack of RAM made it impossible.

When I get access to better device, I will improve this project.
