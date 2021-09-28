# **Food Vision Using an EffecientNetX and Tensorflow**

[link to an article version of the project](https://realnihal.github.io/2021/08/11/food-vision.html)

[The main notebook with all the details](https://github.com/realnihal/Food-Vision-Using-Tensorflow/blob/main/Food_Vision_Using_Tensorflow.ipynb)

We are using the **Food101** standard database to create a deep learning model that can tell the difference and make predictions between 101 classes of food. using all 75,750 training images and 25,250 testing images. We will also use mixed learning to increase the speed of the training process.

Our goal is to beat the original [DeepFood ](https://arxiv.org/ftp/arxiv/papers/1606/1606.05675.pdf) paper. they have an accuracy of 77.4%.

We will use the power of transfer learning by incorporating the EfficientNetX architecture.

**Check out the notebook for a complete detailed explanation of the code**

**You can find the models in this github repository.**

1. [The full Fine-Tuned model that was trained](https://github.com/realnihal/Food-Vision-Using-Tensorflow/tree/main/efficientnetb0_fine_tuned_101_classes_mixed_precision)
2. [Just the Feature Extraction model](https://github.com/realnihal/Food-Vision-Using-Tensorflow/tree/main/101_food_feature_extract_mixedpred_model)

## Conclusions

We acheived an accuracy of about 78.3%. With this we beat the score set by the original [DeepFood](https://arxiv.org/ftp/arxiv/papers/1606/1606.05675.pdf) paper.

It feels great that we achieved our goal. But for those who were keen, our training accuracy was very high compared to our test accuracy. This is probably due to over fitting. On investigation I found out that the [EfficientNet](https://www.tensorflow.org/api_docs/python/tf/keras/applications/efficientnet) model was trainied upon the [ImageNet](https://www.image-net.org/index.php) dataset. These images closely resemble our images. due to this our model ended up slightly overfitting.

**Nevertheless, we acheived our objective and that's all that matters.**

I have trid using more complex versions of EffiecientNet and got the following results:

1. EfficientNetB3 - 81.85%
