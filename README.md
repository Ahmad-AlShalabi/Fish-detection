# Fish-detection

Dataset:

Data collection for CNN is the most important and dificult part of building and ML model.

Fish detection is a binary(one class) classification problem, it needs to positive(fish) and negative(non-fish) dataset
for  fish images (positive one) there are a very limited number of datasets. some it for fish recognition for a limited number of fishs
and one of them has images only underwater inside power generation unite. 
the data set that i have chosen include images for varity types of fishes and under different environments(underwater, outside water , fixed background)
it has around 4000 images only, and all images in one mode (head left, tail right), 
this number and kinde of images is very small to train CNN modle. because the less data you have, the less chance you have of getting accurate predictions for data that your model hasn't yet seen.
so that I decide to use Image Augmentation.
Image Augmentation amends the images on-the-fly while training using transforms like rotation, shifting.. 
and it is way to avoid overfitting the data.

for negative class, I collect 4000 images, all of them are non-fish.


Model:
there are a lot of chooises to build CNN model.
in this point, i relied on a ResNet Network. Why?
The main benefit of a very deep network(normal) is that it can learn features at many different levels of abstraction but a huge barrier for using and training them is vanishing gradients.
deep Residual Network modifided the CNN( added a "shortcut" or a "skip connection" between layers) to address the Vanishing Gradient problem, and became arguably the most groundbreaking work in the computer vision/deep learning community in the last few years.
ResNet makes it possible to train up to hundreds or even thousands of layers and still achieves compelling performance.
This Network won the 1st place on the ILSVRC 2015 classification task. 

in addtion, in this point I used transfare learning technique How?Way?
reused a pre-trained model(transfer of knowledge ) as the starting point for another related model.
it allows rapid progress when modeling related problem.
I used pre-trained ResNet Network with ImageNet weights, and considered it as initial weights to my model.












