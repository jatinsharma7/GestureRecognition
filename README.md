# Gesture Recognition Case Study

## Problem Statement:
You are working as a data scientist at a home electronics company which manufactures state of the art **smart televisions**. You want to develop a cool feature in the smart-TV that can **recognize five different gestures** performed by the user which will help users control the TV without using a remote. 
The gestures are continuously monitored by the webcam mounted on the TV. Each gesture corresponds to a specific command:
•	**Thumbs up:  Increase the volume**
•	**Thumbs down: Decrease the volume**
•	**Left swipe: 'Jump' backwards 10 seconds**
•	**Right swipe: 'Jump' forward 10 seconds**
•	**Stop: Pause the movie**

## Experiments/Output:
We will go ahead with Conv3D architecture instead of CNN+LSTM as the number of parameters would be 4 times in case of CNN +LSTM or 3 times in case of CNN+ GRU in comparison to a Conv3D architecture.

3D convolutions are a natural extension to the 2D convolutions. Just like in 2D conv, you move the filter in two directions (x and y), in 3D conv, you move the filter in three directions (x, y and z). In this case, the input to a 3D conv is a video (which is a sequence of 30 RGB images).

## Hyperparameter Tuning 
Please find below hyper tuning parameters that we experimented with:
  - Batch sizes: 30, 40, 50, 64
  - Epochs: 10, 20, 30
  - Activation functions: RELU and ELU
  - Optimizers: SGD, Adam
  - Learning rates: .001, .0001, .005 
  - Network Size: 3-layer Conv3D and 4-layer Conv3D  
  - Sequence length: 12,15,18
  - Image size: 120*160, 120*120, 100*100, 90*90

The final model we arrived at was based on the factors like;
1.	**Less training times.**
2.	**Lowest possible parameters which helps make this model less resource intense **
3.	**Better suited for a TV based applications**

## Best Model parameters
  - Batch sizes: 30 
  - Epochs: 30
  - Activation functions: RELU 
  - Optimizers: SGD 
  - Learning rates: .001 
  - Network Size: 4-layer Conv3D  
  - Sequence length: 18
  - Image size: 90*90
  - Total parameters: 2,806,149
  - Total time: 11.12 min
  - Validation accuracy: 76%


