# CIFAR 10 -- HOMEWORK 2
Ot Gabaldon Torrents  
CAP 5610
## CNN 
#### (1.1) Original
| Metric| Value |
|-------|-------|
|Epochs|30|
|Number of Layers| **9** (3 Conv, 3 Pooling, 2 Dense, 1 Flattening)| 
|Accuracy - Training| 10.05% |
|Accuracy - Validation| 9.8% |  
|Accuracy - Test| 10% |  
#### Thoughts 
The model is not learning. The final pooling layer might push the convolutions to too small of an dimension to detect meaningful weights between pixels
#### (1.2) Increase Filters (layer 2 : 32 -> 64, layer 3 : 32 -> 128), Changed optimizer from adam to rmsprop (lr=0.001) 
| Metric| Value |
|-------|-------|
|Epochs|30|
|Number of Layers| **8** (3 Conv, 2 Pooling, 2 Dense, 1 Flattening) | 
|Accuracy - Training| 9.80% |
|Accuracy - Validation| 9.67% |  
|Accuracy - Test| 9.43% |  
#### (1.3) Doubled Convolutional Layers, Added batch_size -> 64
| Metric| Value |
|-------|-------|
|Epochs|30|
|Number of Layers| **11** (6 Conv, 2 Pooling, 2 Dense, 1 Flattening) | 
|Accuracy - Training| 9.96% |
|Accuracy - Validation| 9.77% |  
|Accuracy - Test| 10.71% |  
#### Thoughts
Maybe try going straight to the final Dense classification layer. 
Increase the number of neurons in the First Dense Layer.  
Add Padding and then add an extra pooling layer.
#### (1.4) Added Padding, Added Final Pooling Layer
| Metric| Value |
|-------|-------|
|Epochs|30|
|Number of Layers| **12** (6 Conv, 3 Pooling, 2 Dense, 1 Flattening) | 
|Accuracy - Training| |
|Accuracy - Validation| |  
|Accuracy - Test|| 
Padding allowed a large enough area for the final layer to still have enough relation between pixels to produce relevant weights.
Allowed for the layers with small area to observe very basic feature detection.

## Vanilla CNN with data augmentation
?? Number of Layers  
?? Number of Convolutions  
?? Accuracy - Train  
?? Accuracy - Test  

## Dropout CNN with data augmentation
?? Number of Layers  
?? Number of Convolutions  
?? Accuracy - Train  
?? Accuracy - Test  

## Fine Tuned Dropout CNN with data augmentation
?? Number of Layers  
?? Number of Convolutions  
?? Accuracy - Train  
?? Accuracy - Test  
