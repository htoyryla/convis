# convis
A tool to visualize convolutional layer activations on an input image.  

Creates images in which the input image is highlighted by each filter in the given conv layer.

<img src="https://raw.githubusercontent.com/htoyryla/convis/master/tubingen-conv3_2-17.png" width="480">

Dependencies: Torch, loadcaffe

###Usage:

If you place convis.lua into your neural-style directory, you can simply:

 ```th convis.lua -image examples/inputs/tubingen.jpg -model models/VGG_ILSVRC_19_layers.caffemodel -proto models/VGG_ILSVRC_19_layers_deploy.prototxt -layer conv2_2 -output_dir convisimages```
 
Otherwise you need to supply correct paths to the model etc.
 
###Parameters:
``` 
-image      the input image
-model      the caffemodel to be used
-proto      deploy prototxt
-output_dir the dir in which the output images are going to be placed
-layer      name of the conv layer
```
The output_dir must exist in advance. The output files will be named like convisimages/tubingen-conv3_2-69.png



