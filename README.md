# TEXT2IMAGE_GANs
The goal is to train a GAN to understand and interpret the details described in the text and generate corresponding images that accurately reflect those descriptions.

Implementation of the Research Paper titled " StackGAN: Text to Photo-realistic Image Synthesis with Stacked Generative Adversarial Networks"
Link : https://arxiv.org/abs/1612.03242

 ##                                                                        Architecture of StackedGAN
<img width="459" alt="image" src="https://github.com/pAbhit007/TEXT2IMAGE_GANs/assets/111629488/1a496c1d-cedc-42b8-85c5-7bd1ef755a93">


## Dataset Description

###                                                                       CUB_200 Dataset Description:

####  1. Number of Classes:

CUB_200 contains 200 bird species classes.

#### 2. Number of Images:

It consists of 11,788 images in total.

#### 3. Image Resolution:

The images are typically of varying resolutions but are often resized to a standard size (e.g., 64x64 pixels) for processing in models like StackGAN.

#### 4. Annotations:

Each image in CUB_200 is annotated with bounding boxes and part annotations for fine-grained localization and recognition tasks.

#### 5. Dataset Split:

The dataset is split into training and test sets, with predefined train-test splits commonly used for benchmarking models.

#### 6. Challenges:

CUB_200 poses several challenges such as fine-grained classification due to subtle differences between bird species, varying poses, and background clutter.
