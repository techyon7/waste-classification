# Waste Classification

The issue of waste classification can be addressed through social and environmental awareness, labelled dustbins or dumping areas for categorized wastes, educating citizens to be responsible and aware about waste categorization. The CNNs can be otherwise used with little effort in promoting awareness and incorporating people to follow a certain custom into dumping objects in the right dustbin.

Project Document: https://docs.google.com/document/d/1xKJG0Gkxy-5qf1hX6r2TByoMeEH-zllJR6Ein8RTO9w/edit?usp=sharing

## Usage

Download the models from (900mb): https://drive.google.com/file/d/1YTJ8Af8BrC809GSjj31PYl0E5_66uYeU/view?usp=sharing

Make sure the required models are present in the `/models` folder in root directory and run the whole notebook. 

Change the file paths in the notebook for importing/exporting files if required. 

## Model and Dataset Specifications

The CompostNet dataset, extended by the TrashNet dataset forms a total of 7 categories of waste, namely, Paper, Cardboard, Metal, Glass, Compost, Trash and Plastic. The TrashNet dataset consists of 2527 images with 6 categories:  paper, cardboard, metal, glass, plastic and trash. Each image has dimensions of 512x384 pixels and is taken against a white poster board background.

The CompostNet dataset consists of an additional 175 photos in the food waste and 49 photos of landfill waste, forming a total of 2751 images in all 7 categories. The CompostNet dataset has two versions: version-A and version-B.

The version-A of the dataset consists of images of sizes 300x400 pixels and the version-B on the other hand consists of images of shape 224x224 pixels. Images are then reshaped to images for waste classification technique to the dimensions of 512x384 pixels according to TrashNet dataset opted by Gary Thung and Mindy Yang.

## Transfer Learning

Transfer Learning is a method used to leverage weights from a pre-trained model to get better accuracy on a related but different task with a different dataset. Transfer Learning has proven to provide better results when there is a lack of dataset availability. In this case, 2751 images in total are available in the dataset. The lack of dataset size might lead to a model which might have low accuracy. For that very reason, it was opted to look for better results on waste classification through transfer learning.

## Training & Learning Rate Specifications

In order to find a suitable learning rate for the model to train on, the logarithmic learning rate against the training loss for the 1st epoch was plotted with the pretrained model. The minimum and maximum values chosen for the search of learning rate were 1e-6 and 1e1 respectively. 

## Data Augmentation

Data Augmentation was used to add data points to the training dataset and to introduce variation to the dataset which was limited in size. 

