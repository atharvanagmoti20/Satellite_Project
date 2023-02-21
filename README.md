Satellite Image Segmentation

This Repository focus on ROAD DETECTION from satellite images.

This approach can be applied to four classes mainly :-
1. Building Detection
2. Road Detection
3. Vegetation Detection
4. Water Detection

The steps followed in performing the given program:-
Downloaded the dataset from https://www.cs.toronto.edu/~vmnih/data/

Here is the shortcut link for downloaded dataset https://drive.google.com/drive/folders/1Cg393dBkLi_D-CCztsp2NO-nyIzttcbI?usp=sharing
The dataset contains satellite images as well as its masked images.

First step is to import all the required libraries.
Initially all the images were resized to 1024 by 1024.
Then each image was segmented into equal number of patches. (In this case 16 patches per image.)

49 satellite images and its masked images were taken as input images and after patchifying we got dataset of 784 patches as an individual image.

Using tensorflow and keras library we split the dataset into 80% training and 20% testing images.
Passed the dataset to U-Net model.

The U-Net model is a convolutional neural network (CNN) architecture used for image segmentation tasks. It was originally proposed in 2015 by Ronneberger et al. and has since become a popular choice for medical image segmentation.

The U-Net architecture consists of two parts: an encoding path and a decoding path. The encoding path is similar to a typical CNN architecture, where multiple convolutional and pooling layers are used to extract features from the input image. The decoding path, on the other hand, is designed to upsample the feature maps back to the original input image size while also adding skip connections from the encoding path to help preserve high-resolution information.

The skip connections in U-Net allow the model to use both high-level and low-level features in the image segmentation process, leading to better performance in many cases. Additionally, U-Net also includes data augmentation techniques, such as random rotations and flips, to help increase the amount of training data and prevent overfitting.

U-Net has been used for a variety of image segmentation tasks, such as cell segmentation in microscopy images, lung segmentation in CT scans, and road segmentation in satellite images.

The weight of the model is stored and the results are visualized using matplotlib.



