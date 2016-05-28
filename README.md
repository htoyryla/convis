# convis
A tool to visualize convolutional layer activations on an input image.  

Creates images in which the input image is highlighted by each feature map in the given conv layer.

<img src="https://raw.githubusercontent.com/htoyryla/convis/master/tubingen-conv3_2-17.png" width="480">

Dependencies: Torch

###Usage:

 ```th convis.lua -image examples/inputs/tubingen.jpg -layer conv5_2 -output_dir convis```
 
###Parameters:
``` 
-image      the input image
-model      the caffemodel to be used
-proto      deploy prototxt
-output_dir the dir in which the output images are going to be placed
-layer      name of the conv layer
```
The output_dir must exist in advance. The output files will be named like convis/tubingen-conv3_2-69.png



