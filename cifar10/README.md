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
- [x] Add Padding and then add an extra pooling layer.
#### (1.4) Added Padding, Added Final Pooling Layer
| Metric| Value |
|-------|-------|
|Epochs|30|
|Number of Layers| **12** (6 Conv, 3 Pooling, 2 Dense, 1 Flattening) | 
|Accuracy - Training| 96% |
|Accuracy - Validation| 76% |  
|Accuracy - Test| 60%| 
#### Thoughts
Padding allowed a large enough area for the final layer to still have enough relation between pixels to produce relevant weights.
Allowed for the layers with small area to observe very basic features.
Need to fix over fitting:
- [ ] Data Augmentation
- [ ] Dropout
- [ ] Normilization of inputs 
- [ ] Batch Normilization
- [ ] Kernal_regulizer

## Vanilla CNN with data augmentation
#### (2.1) Manually Split Training and Validation Data. Added rotation, zoom, and dimension shifts to data augmentation
| Metric| Value |
|-------|-------|
|Epochs|30|
|Number of Layers| **12** (6 Conv, 3 Pooling, 2 Dense, 1 Flattening) | 
|Accuracy - Training| 79.8%  |
|Accuracy - Validation|  77.23% |  
|Accuracy - Test| 49.8% | 
#### Thoughts
- [x] Double check that new validation style is not affecting results.
- [ ] Try increasing number of epochs, since there is now more training data
#### (2.2) Increased Epochs to 75
| Metric| Value |
|-------|-------|
|Epochs| 75 |
|Number of Layers| **12** (6 Conv, 3 Pooling, 2 Dense, 1 Flattening) | 
|Accuracy - Training| 75.7%  |
|Accuracy - Validation|  78.25% |  
|Accuracy - Test| 44.7% | 
#### Thoughts
The peak performance seems to happen around 35 epochs.  
![Training Acc](img/trainingAcc.png)

#### (2.3) Added Batch Normilization, Increased Nodes on classifier input layer 64 -> 128, Changes epochs to 40
| Metric| Value |
|-------|-------|
|Epochs| 75 |
|Number of Layers| **18** (6 Conv, 6 Normilization, 3 Pooling, 2 Dense, 1 Flattening) | 
|Accuracy - Training|  |
|Accuracy - Validation| |  
|Accuracy - Test| | 
#### Thoughts

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
