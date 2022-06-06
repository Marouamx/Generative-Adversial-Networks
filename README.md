# Generative-Adversial-Networks
This Project is divided into 3 sections, a CNN classifier with data augmentation, a Generative Adversarial Network to generate more images from a dataset and increase the discriminator powerfulness and a Neural style transfer application.

## 1. CNN CLASSIFIER
  A classifier for Cats Vs Dogs was implemented.
First of all data was extracted from google about
(just 2000 pictures), then multiple data
augmentation techniques were implemented such
as: width and height shift, rotation, zooming,
flipping …etc.
This allowed us to augment our data for the neural
network to get better accuracy.

![image](https://user-images.githubusercontent.com/62667666/172136874-0bb70434-1a3d-4def-85f3-1de322221c2b.png)
![image](https://user-images.githubusercontent.com/62667666/172136417-1c2db8e7-b330-47a3-b943-65671ee49b93.png)

## 2. GAN model 
![image](https://user-images.githubusercontent.com/62667666/172136674-dcb6fc2d-0efb-4f2a-bf99-5ad0887d94bf.png)

 After building the discriminator and generator
models, images first got resized to 70*70px due to
limitations in computational resources and time
constraints. Images were organized in batches of 15
and loaded by .from_tensor_slices to be fed the
training loop.

### Generated Images: 
![image](https://user-images.githubusercontent.com/62667666/172136915-63d66e4f-e774-48af-abc8-07e386c335ba.png)
![image](https://user-images.githubusercontent.com/62667666/172136997-899c471d-c3b4-4a8f-bee4-1c1beda04a72.png)
![image](https://user-images.githubusercontent.com/62667666/172137030-ec850a25-99da-4d64-a444-deb3fd45603f.png)

## 3. NEURAL STYLE TRANSFER using VGG model
![image](https://user-images.githubusercontent.com/62667666/172137238-ca918267-3c6c-4ae8-8b37-5b23a07fc88a.png)

The VGG-19 is a convolutional neural
network that is 19 layers deep, trained on the
imagenet dataset. Using the intermediate layers of
this model to get the content and style
representations of the image. Starting from the
network's input layer, the first few layer activations
represent low-level features like edges and textures.
As we step through the network, the final few
layers represent higher-level features. So For an
input image, we try to match the corresponding
style and content target representations at these
intermediate layers.

Extract style from horse and content from cow

![image](https://user-images.githubusercontent.com/62667666/172137605-808b3541-e051-42ef-b18f-30714c299a0f.png)

and the generated image is: 

![image](https://user-images.githubusercontent.com/62667666/172137835-3b5136de-db1e-4a03-9e59-88e2e8f8bc39.png)
