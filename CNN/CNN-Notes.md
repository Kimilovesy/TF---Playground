# Some important concepts
## Padding
General Formula as shown below:

![General Formula](https://github.com/Kimilovesy/TF---Playground/blob/8dedbeb7314d57026928fc7a957ee4190f100565/CNN/Screen%20Shot%202018-02-24%20at%2018.02.45.png)

**Where, p is the padding size, stride is the step u , f is the filter size.** 

1. Valid Padding: **No Padding** 
  * (n×n * f×f --> n-f+1×n-f+1), where f is the filter size, usually f is odd number
2. Same padding: Pad so that output size is the same as the input size  
  * (n×n * f×f --> n×n)

![Image of Padding](https://github.com/Kimilovesy/TF---Playground/blob/master/CNN/Padding.png)





# Core Layers
## Convoulutional Layer
  1. 1-D Visualization
  
  ![1-D Example](https://github.com/Kimilovesy/deep-learning-coursera/blob/399a701dffccba20ebd7bdb63f203bb6f5b5836c/Convolutional%20Neural%20Networks/images/Convolution_schematic.gif)
  
  Actually, it is not 'real' convoultion compared with theeory in signal processing, it is called **'cross-correlation'**.
  
  2. Convolution Over volumn
   * Input: H x W x Channel | Filter size: f x f x channel | Output: O x O x **1**, the size of last dim is 1!! 

## Pooling Layer
The aim of the pooling layer is to decrease the dimension of the output.
  * Max Pooling
  ![Max_pooling](https://github.com/Kimilovesy/deep-learning-coursera/blob/399a701dffccba20ebd7bdb63f203bb6f5b5836c/Convolutional%20Neural%20Networks/images/max_pool.png)
  * Average Pooling
  ![Average Pooling](https://github.com/Kimilovesy/deep-learning-coursera/blob/399a701dffccba20ebd7bdb63f203bb6f5b5836c/Convolutional%20Neural%20Networks/images/ave-pool.png)
## Fully Connected Layer

# Why Convoultional?
1. Share weights
