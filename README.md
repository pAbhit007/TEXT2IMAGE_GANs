# TEXT2IMAGE_GANs
The goal is to train a GAN to understand and interpret the details described in the text and generate corresponding images that accurately reflect those descriptions.

Implementation of the Research Paper titled " StackGAN: Text to Photo-realistic Image Synthesis with Stacked Generative Adversarial Networks"
Link : https://arxiv.org/abs/1612.03242

## ARCHITECTURE:
StackGAN consists of two stages, each designed to progressively generate higher-resolution images based on textual descriptions. Here’s a brief overview of Stage 1 and Stage 2 in StackGAN:

## Stage 1:

#### Purpose:

1. **Low-Resolution Generation:** Stage 1 focuses on generating low-resolution (e.g., 64x64) images from textual descriptions.
2. **Global Structure:** It captures the overall structure and basic features of the image based on the text embedding.

#### Components:

1. **Text Embedding Processing:** Text descriptions are processed through a Conditioning Augmentation (CA) model to generate a latent vector 𝑐.
2. **Conditional GAN**: A generator takes 𝑐 and random noise as inputs to generate low-resolution images.
3. **Discriminator:** Evaluates the realism of the generated images against real low-resolution images from the dataset.
4. **Training:** The generator and discriminator are trained adversarially to improve the quality and realism of the generated images.

#### Output:

The output of Stage 1 is a set of low-resolution images that roughly match the input text descriptions in terms of global structure and basic features.

## Stage 2:

**Purpose:**

**High-Resolution Refinement:** Stage 2 refines the low-resolution images generated in Stage 1 into higher-resolution (e.g., 256x256) images.
**Details and Realism:** It focuses on adding finer details, textures, and realism to the generated images.

#### Components:

**Conditional GAN with Conditioning Augmentation:** Similar to Stage 1, but operates at a higher resolution.
**Global and Local Features:** The generator in Stage 2 takes the low-resolution image from Stage 1, text embedding 𝑐, and noise as inputs to synthesize detailed images.
**Discriminator:** Evaluates the realism of the higher-resolution images against real high-resolution images from the dataset.
**Training:** The generator and discriminator are trained further to enhance the fidelity and quality of the generated images, focusing on details and local features.

#### Output:
The output of Stage 2 is a set of high-resolution images that closely match the input text descriptions, with improved details, textures, and overall realism compared to Stage 1.


 ##                                                                        Architecture of StackedGAN
<img width="459" alt="image" src="https://github.com/pAbhit007/TEXT2IMAGE_GANs/assets/111629488/1a496c1d-cedc-42b8-85c5-7bd1ef755a93">


## Dataset Description : https://data.caltech.edu/records/65de6-vp158

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
