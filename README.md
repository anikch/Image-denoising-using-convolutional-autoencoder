# Image denoising using convolutional autoencoder

**Problem Statement:**

The dataset is similar to MNIST but includes images of specific clothing and accessory. The objective is to add some noise to the images and then use an Autoencoder to denoise them.

Dataset Description:

MNIST Fashion Dataset

•Total Images: 70,000

•Train Images: 60,000

•Test Images: 10,000

•Image Size:28 x 28

•Classes:‘T-Shirt/top’, ‘Trouser’, ‘Pullover’, ‘Dress’, ‘Coat’, ‘Sandal’, ‘Shirt’, ‘Sneaker’, ‘Bag’, ‘Ankle Boot’


**Steps Performed**
- We have first Loaded the data nad vizualized it.
- Normalized the data and added salt and pepper noise.
- Vizualized the noisy image.
- Created out encoder and decoder architectures and created autoencoder model.
- Our input data shape is ( 28 x 28 x 1). I have used 2 Conv2D layers and 2 MaxPool2D in encoder. 2 Conv2DTranspose layers and 1 Conv2D layer in decoder.
- From model summary it can be seen that output shape for input and output is same (28, 28, 1)
- Compiled the model with 'Adam' as optimizer and binary_crossentropy as loss function.
- Trained the model with epochs= 100 and earlystopping (monitor= 'val_loss', min_delta= .001) callback.
- Our model trained for 24 epochs and stopped by early stopping.
- Created a function to see random 10 noisy images and autoencoder output of those noisy images.
- Checked random images from testing and testing dataset and denoising versions of those images from autoencoder.
- Autoencoder has done pretty good job.
