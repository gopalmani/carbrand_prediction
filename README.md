# carbrand_prediction
Classification of car models, to predict model of a car by an image.  
The enviournment configuration:
python = 3.6
Keras 2.0.1 using Tensorflow backend and cpu training.

1. Classification of Car models and preparation of data:
 The first is to decide how many types of models we are going to consider for classification. Here we take five classes(types) of car models for classification. We prepare approx 50 image set of each of the model for training.
 Folder dataset contains the data to be trained and 

2. Training of model :
#usage code
python train.py --dataset dataset --model brandNet.model --labelbin lb.pickles

We have used VGGNET The VGG network architecture was introduced by Simonyan and Zisserman in their 2014 paper, Very Deep Convolutional Networks for Large Scale Image Recognition.
This network is characterized by its simplicity, using only 3×3 convolutional layers stacked on top of each other in increasing depth. Reducing volume size is handled by max pooling. Two fully-connected layers, each with 4,096 nodes are then followed by a softmax classifier.
Trained model is saved as brandNet.model and VGGNET network is saved in cnnmodel folder.

3. We use classify.py 
#usage code
python classify.py --model brandNet.model --labelbin lb.pickles --image examples/bmw1.jpg

