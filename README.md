
# Flower-Image-Classification
Image classification for 5 types of flowers:
 1. Roses
 2. Daisy
 3. Dandelion
 4. Sunflowers
 5. Tulips

Performed while taking [Intro to TensorFlow for Deep Learning](https://www.udacity.com/course/intro-to-tensorflow-for-deep-learning--ud187) course from udemy.
Two different approaches used for image classification.
## CNN with data augmentation
Used convolutional neural network consisting of 3 convolutional with maxpooling and a flatten dense layer. Along with this used data augmentation to reduce overfitting and improve accuracy. ImageDataGenerator from tf.keras was used for data augmentation. Also used early stop to ensure the model doesnt overfit. With this, reached a validation accuracy of **~78%**.

## Using transfer learning
[Inception V3](https://tfhub.dev/google/tf2-preview/inception_v3/feature_vector/4) trained on [Image net](https://www.image-net.org/) was used for transfer learning. As this model was already trained on images of flowers present in the image net dataset, this was a perfect candidate for transfer learning. This gave an accuracy of **~90%** in just 5 epochs.
