[![Matplotlib](https://img.shields.io/badge/TensorFlow-2.0-important.svg)]()
[![Matplotlib](https://img.shields.io/badge/Keras-important.svg)]()
[![Python](https://img.shields.io/badge/Python-3-red.svg)]()
[![Numpy](https://img.shields.io/badge/Numpy-1.11.0-informational.svg)](https://pypi.org/project/numpy/)
[![Matplotlib](https://img.shields.io/badge/Matplotlib-2.0-important.svg)](https://matplotlib.org/)

# Fish-detection
Create a deep learning model to predict that an image contains a fish or not.
## Dataset:

Data collection for CNN is the most important and difficult part of building an ML model.

Fish detection is a binary(one class) classification problem, it needs to **positive(fish)** and **negative(non-fish)** dataset.
- for fish images (the positive one) there are a very limited number of datasets. some of it for fish recognition for a limited number of fishes and one of them has images only underwater inside power generation unite. 
the data set that I have chosen include images for a variety types of fishes and under different environments(underwater, outside water, fixed background).

![](https://github.com/Ahmad-AlShalabi/Fish-detection/blob/master/images/dataset.PNG?raw=true "Dataset")

It has around **4000 images only**, and all images in one mode (head left, tail right), 
this number and kinds of images is very small to train CNN model. because the less data you have, the less chance you have of getting accurate predictions for data that your model hasn't yet seen.
So that I decide to use **Image Augmentation**.

***Image Augmentation:*** amends the images on-the-fly while training using transforms like rotation, shifting. and it is a way to avoid overfitting the data.

- for Nom fish (negative) class, I collected 4000 images, all of them are non-fish.


## Model:
- There are a lot of choices to build CNN model.
At this point, I relied on a ResNet Network. Why?
The main benefit of a very deep network(normal) is that it can learn features at many different levels of abstraction but a huge barrier for using and training them is vanishing gradients.
- Deep Residual Network modified the CNN structure ( added a "shortcut" or a "skip connection" between layers) to address the Vanishing Gradient problem and became arguably the most groundbreaking work in the computer vision/deep learning community in the last few years.
>ResNet makes it possible to train up to hundreds or even thousands of layers and still achieves compelling performance.
This Network won the 1st place on the ILSVRC 2015 classification task. 

![](https://github.com/Ahmad-AlShalabi/Fish-detection/blob/master/images/skip_connection.png?raw=true "Shortcut")
- In addition, at this point, I used the **transfer learning** technique How? and Way?
It is about reused a pre-trained model(transfer of knowledge ) as the starting point (weights) for another related model.
it allows rapid progress when modelling related problem.
**I used a pre-trained ResNet model with ImageNet weights and considered it as initial weights to my model.




## References

Used dataset for positive images [Dataset](https://wiki.qut.edu.au/display/cyphy/Fish+Dataset)
###### Dataset Authors
- ZongYuan Ge              z.ge@outlook.com or gzy555555@gmail.com

- Dr Chris Mccool           chris.mccool@nicta.com.au

- Prof Peter Corke          peter.corke at qut.edu.au


ResNet - Kaiming He, Xiangyu Zhang, Shaoqing Ren, Jian Sun - [Deep Residual Learning for Image Recognition](https://arxiv.org/abs/1512.03385)







