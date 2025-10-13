# pill-sorter

Machine learning model that sorts pills

Trained a 1,199,686 parameter convolution neural network that classifies a pill based on a picture. This was built for a science fair project at Port Credit Secondary School. Which we won :).

Can be seen here:  https://github.com/amanda-ucc/pill-sorter/blob/main/cnn-pill-sorter.ipynb

Originally we were going build a device that could take that picture, classify the pill and sort it however we ran out of time for the device work. The model however functions exactly as I intended. We thought this could provide a valuable benefit for seniors as their vision deteriorates with age to ensure that they are getting the correct medication. Maybe in the future we can take this back up :)

It uses:

- tensorflow
- keras
- pandas
- numpy
- matplotlib

The training accuracy looks like this 

I used:
- 534 files belonging to 6 classes for training
- 60 files belonging to 6 classes for testing

<img width="547" height="433" alt="image" src="https://github.com/user-attachments/assets/508e3518-70ab-4cbf-bbf3-64da2d92e0d0" />


Validation loss likes this

<img width="547" height="433" alt="image" src="https://github.com/user-attachments/assets/f63b60dc-773c-494e-a27f-8fe30936275d" />

```
Model: "model_1"
_________________________________________________________________
 Layer (type)                Output Shape              Param #   
=================================================================
 input_2 (InputLayer)        [(None, 256, 256, 3)]     0         
                                                                 
 rescaling_1 (Rescaling)     (None, 256, 256, 3)       0         
                                                                 
 conv2d_5 (Conv2D)           (None, 254, 254, 32)      896       
                                                                 
 max_pooling2d_4 (MaxPoolin  (None, 127, 127, 32)      0         
 g2D)                                                            
                                                                 
 conv2d_6 (Conv2D)           (None, 125, 125, 64)      18496     
                                                                 
 max_pooling2d_5 (MaxPoolin  (None, 62, 62, 64)        0         
 g2D)                                                            
                                                                 
 conv2d_7 (Conv2D)           (None, 60, 60, 128)       73856     
                                                                 
 max_pooling2d_6 (MaxPoolin  (None, 30, 30, 128)       0         
 g2D)                                                            
                                                                 
 conv2d_8 (Conv2D)           (None, 28, 28, 256)       295168    
                                                                 
 max_pooling2d_7 (MaxPoolin  (None, 14, 14, 256)       0         
 g2D)                                                            
                                                                 
 conv2d_9 (Conv2D)           (None, 12, 12, 256)       590080    
                                                                 
 flatten_1 (Flatten)         (None, 36864)             0         
                                                                 
 dense_1 (Dense)             (None, 6)                 221190    
                                                                 
=================================================================
Total params: 1199686 (4.58 MB)
Trainable params: 1199686 (4.58 MB)
Non-trainable params: 0 (0.00 Byte)
```


