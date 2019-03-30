# CIFAR 10 -- HOMEWORK 2
Ot Gabaldon Torrents  
CAP 5610
## Design 1
### Vanilla Convolutional neural network  
#### Original
| Metric| Value |
|-------|-------|
|Epochs|30|
|Number of Layers| **9** (3 Conv, 3 Pooling, 2 Dense, 1 Flattening)| 
|Accuracy - Training| 10.05% |
|Accuracy - Validation| 9.8% |  
|Accuracy - Test| 10% |  
#### Thoughts
The model is not learning. The final pooling layer might push the convolutions to too small of an area to detect meaningful relations
#### Increase Batches (layer 2 : 32 -> 64, layer 3 : 32 -> 128), Changed optimizer from adam to rmsprop
| Metric| Value |
|-------|-------|
|Epochs|30|
|Number of Layers| **8** (3 Conv, 2 Pooling, 2 Dense, 1 Flattening) | 
|Accuracy - Training| 10.05% |
|Accuracy - Validation| 11.00% |  
|Accuracy - Test| 10.05% |  
#### Thoughts
The model is still not learning. Maybe doubling the convulutional layers will allow for more learning.
## Design 2
### Vanilla Convolutional neural network with data augmentation
?? Number of Layers  
?? Number of Convolutions  
?? Accuracy - Train  
?? Accuracy - Test  

## Design 3
### Convolutional neural network with data augmentation and dropout
?? Number of Layers  
?? Number of Convolutions  
?? Accuracy - Train  
?? Accuracy - Test  

## Design 4
### Fine Tuned Convolutional neural network with data augmentation and dropout
?? Number of Layers  
?? Number of Convolutions  
?? Accuracy - Train  
?? Accuracy - Test  
