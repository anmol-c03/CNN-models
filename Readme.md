# Project Title

These are the AI models that can be used for training image dataset.

## CNN_1DNN:
The CNN-1RNN type of networks also consists of the convolutional and pooling layers of VGG-16, followed by a FC layer of 4096 units. The 68 facial landmarks are concatenated with the features extracted from the last pooling layer of VGG-FACE and are fed to the FC layer. Low-, mid- and high-level features are extracted, concatenated and fed to a 2 layer DNN that predicts the valence and arousal values. Each DNN layer comprises 128 units. The CNN-1DNN networks are also provided with an input  of images (and the corresponding landmarks of each image), predicting, for each image,the valence Arousal Values.

In this network, the features extracted from  the second pooling layer (following the 4th convolutional), the last pooling layer (following the 13th convolutional and before being concatenated with the landmarks)  the FC layer are concatenated and fed to the DNN.

## CNN_3DNN:
The CNN-3RNN networks include, first, the convolutional and pooling layers of VGG-16, followed by a fully connected layer of 4096 units. The 68 facial landmarks are concatenated with the features extracted from the last pooling layer of VGG-FACE and are fed to this FC layer. Low-, mid- and high-level feature sets are extracted from this network and each set is fed to a 2-layer DNN  network that provides an estimate of the targeted valence and arousal values. Each DNN layer comprises 128  units. The CNN-DNN networks are provided with an inputs of images (and the corresponding landmarks of each image) and predict, for each image, estimates of the valence-arousal values. 
 In this network the features extracted from the FC layer are fed, as input, to a DNN network,  the features extracted from the last pooling layer (before being concatenated with the landmarks) are fed, as input, to a second DNN network, the features extracted from the second pooling layer (following the fourth convolutional layer) are fed, as input, to another DNN network, The CNN_3DNN.png in images folder depict the exact structure of the afore-mentioned network. All Dense networks have the same structure, i.e., a 2-layer DNN network, with each layer having 128 units. Next, the outputs of the 3 DNNs are concatenated and fed to the output layer that performs the valence-arousal prediction.

## MldrNet
This proposed model is a new deep network that learns multi-level deep representations for image emotion clas- sification (MldrNet). Image emotion can be recognized through image semantics, image aesthetics and low-level visual features from both global and local views
The proposed MldrNet combines deep representations of different levels, i.e. image semantics, image aesthetics and low-level visual features to effectively classify the emotion types of different kinds of images, such as abstract paintings and web images. 

## Table of Contents
- [Usage](#usage)
- [Refrences](#refrences)


## Usage

All these models can be used for image classification problems especially in the feild of emotion recognition. CNN_1DNN and CNN_3Dnn can be used for facial emotion detection while MldrNet can be used for sentiment anlysis of image(i.e it is not limited only to facial emotion rather it can analyze emotion of entire image).
Moreover, if you have sequence of frames of images for trainig purpose , i personally recommed replacing DNNs with RNN (GRU) networks.


## Refrences
Affect Analysis in-the-wild: Valence-Arousal, Expressions, Action Units and a Unified Framework(Dimitrios Kollias, Member,Stefanos Zafeiriou) 
https://arxiv.org/pdf/2103.15792.pdf
