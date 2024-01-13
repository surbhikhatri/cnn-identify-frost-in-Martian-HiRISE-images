Identification of Frost in Martian HiRISE Images

In this problem, we are trying to build a classifier that distinguishes images of
Martian terrain with frost. You can find the dataset in
https://dataverse.jpl.nasa.gov/dataset.xhtml?persistentId=doi:10.48577/jpl.QJ9PYA.

This dataset was created to study Mars’ seasonal frost cycle and its role in the
planet’s climate and surface evolution over the past 2 billion years. The data helps
in identifying low-latitude frosted microclimates and their impact on climate

i. Images (png files) and labels (json files) are organized in the data directory
by “subframes.” Subframes are individual 5120x5120 pixel images which are
crops of the original HiRISE images (often on the order of 50k x 10k pixels).
Individual subframes were annotated by the contributors and then sliced into
299x299 “tiles.” Each tile has an associated label for use in training ML
algorithms. 

ii. There are 214 subframes and a total of 119920 tiles. Each tile has annotations
which have been used to assign labels to the tiles ‘frost’ or ‘background.’
Each JSON file contains all the annotation information collected from human
annotators. 

iii. The following are relevant to the assignment:
Image tiles are organized into folders of ‘background’ and ‘frost’ classes (bi-
nary). For the purpose of the final project, individual tiles shall serve as the
data points which need to be classified using binary classification.

**Problem Statement**: 
1. Train a three-layer CNN followed by a dense layer on the data. Choose the
size of the kernels and depth of the layers and the number of neurons in
the dense layer (MLP) on your own. Use ReLU’s in all of the layers. Use
the softmax function, batch normalization 3 and a dropout rate of 30%, L2
regularization, as well as ADAM optimizer. Use cross entropy loss. Train
for at least 20 epochs and perform early stopping using the validation set.
Keep the network parameters that have the lowest validation error. Plot the
training and validation errors vs. epochs.


2. Transfer Learning:
   1. EfficientNetB0
   2. ResNet50
   3. VGG16


3. Compare the results of all the four classifiers.
