# Neural-Style-Transfer
Neural style transfer in tensorflow using pretrained VGG-19.

This repo contains a tensorflow implementation of the paper [**A Neural Algorithm of Artistic Style**](https://arxiv.org/abs/1508.06576). 

This implementation was part of a deeplearning.ai Convolutional Neural Networks course. Some of the utility functions for using a pretrained VGG-19 network were provided by the course staff. 

# Examples
San Francisco Bay Bridge
![San Francisco Bay Bridge][sf]

[sf]: https://github.com/PrzemekPobrotyn/Neural-Style-Transfer/blob/master/neural_sf.jpg "Neural Bay Bridge"

Original: 

![San Francisco Bay Bridge][sf_orig]

[sf_orig]: https://github.com/PrzemekPobrotyn/Neural-Style-Transfer/blob/master/sf.jpg "Original Bay Bridge"

Oxford winter skyline

![Winter Oxford][ox_nst]

[ox_nst]: https://github.com/PrzemekPobrotyn/Neural-Style-Transfer/blob/master/output-3.jpg "Oxford-nst"

Original

![Winter Oxford][ox]

[ox]: https://github.com/PrzemekPobrotyn/Neural-Style-Transfer/blob/master/oxford.jpg "Oxford"

# Data

We used a pretrained model by MatConvNet, available at [this link](http://www.vlfeat.org/matconvnet/pretrained/). Download it and put it in *data* directory together with the scripts to generate images locally.

# Dependecies

* tensorflow 1.0.0
* numpy 1.13.3
* scipy 1.0.0
* imageio 2.2.0
* PIL 4.1.1

# Running the script

Download all python files. In the same directory, create a *data* directory and put there *imagenet-vgg-verydeep-19* from [http://www.vlfeat.org/matconvnet/pretrained/]. Create an empty *output* directory to store outputs.

Run the script as follows:

python generate_image.py <content_image_path> <style_image_path> <output_path> <num_iterations> 

There is an optional flag -s for saving intermediate results.

Using 500 iterations to generate 300x400 image takes around 2h on a modest CPU and less than a minute on a Nvidia K80. 

Using too large images results may cause *out of memory* error.

For best results, make sure style and content images are of similar size and shape.
