# convis
A tool to visualize convolutional layer activations on an input image.  

Creates images in which the input image is highlighted by each feature map in the given conv layer.

![alt tag](https://raw.githubusercontent.com/htoyryla/convis/master/tubingen-conv3_2-17.png)

Dependencies: Torch

Usage:

 th convis.lua -image examples/inputs/tubingen.jpg -layer conv5_2 -output_dir convis
 
 Parameters:
 
image  the input image
model  the caffemodel to be used
proto  deploy prototxt
output_dir the dir in which the output images are going to be places
layer name of the conv layer

The output_dir must exist in advance. The output files will be named like convis/tubingen-conv3_2-69.png

Known issues:

/home/hannu/torch/install/bin/luajit: convis.lua:61: bad argument #3 to 'narrow' (out of range at ... )
This happens when almost all feature maps have been processed. I will look into it. Anyhow, (more than) enough images will have been generated when this occurs.
