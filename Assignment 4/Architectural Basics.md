There are different kind of CNN architecture. How do we define the best architecture? For this, we need to know what is the meaning of best nodel? 

###### Best Model:

When  model gives most efficient accuracy in less number of parameters(reducing computational cost) then model considered as best model.

###### Starting with Basic CNN and reaching best CNN Model:

In the assignment 4, we will start by defining very simple model architecture and analyse the model then we will consider below points to get to the best model. Let's go into detail about what point need to be considered for getting the best model from simple model.

###### 

1. ###### How many layers:

    we need as many layers as required to reach global receptive field. 

2. ###### MaxPooling: 

   by the use of max pooling we can reduce the layer count. it reduces the layers approximately half of the number of layers. generally we will be using 2d max pooling.

   

3. ###### 1x1 Convolutions:

   ![kernel](https://github.com/bomila/eip3/blob/master/1X1_Convolution.png)

   Use of 1X1 Convolution gives us following feature:

   * 1x1 is not even a proper convolution, instead of convolving each pixel separately, multiply the whole channel with just 1 number. 

   * It is computationally less expensive.

   * 1x1 is merging the pre-existing feature extractors, creating new ones, keeping in mind that those features are found together (like edges/gradients which make up an eye)

   * 1x1 is performing a weighted sum of the channels, so it can so happen that it decides not to pick a particular feature which defines the background and not a part of the object.

     

4. ###### 3x3 Convolutions:

   using a 3x3 kernel twice is equivalent to using a 5x5 kernel. This also means that two layers of 3x3 have a resulting receptive field of 5x5 and 3X3 involves less number of computation than 5X5.

   

5. ###### Receptive Field:

   receptive field is used in pyramid like model structure. 

6. ###### SoftMax:

   it takes input distribution and normalize it to probability like. the softmax function is often used in the final layer of a neural network-based classifier. we will not use softmax for real life problem like medical data, object detection etc

7. ###### Learning Rate:

    Learning rate is a hyper-parameter where we multiply each derivative by a small value called the “learning rate” before they subtract it from its corresponding weight.

8. ###### Kernels and how do we decide the number of kernels?

   We would need a set of edges and gradients to be detected to be able to represent the whole image. Through experiments, we have learned that we should use around 32 or 64 kernels in the first layer, increasing the number of kernels slowly. Let's us assume we add 32 kernels in the first layer, 64 in second, 128 in thrid and so on. 

   Our Network would look something like this:

   400x400 | (3x3)x32 | 398x398x32
   398x398 | (3x3)x64 | 396x396x64
   ...

   One need to observe here that the input to the second layer is not **398x398** but 398x398**x32**, as we added 32 kernels. Each kernel would create its own channel. 

   

9. ###### Batch Normalization:

   used to normalize pixel values between 0 to 255. before taking batch of images make sure all the pixel values of image in batch should be in range of 0 to 255

10. ###### Image Normalization:

     it looks for the maximum intensity pixel and a minimum intensity and then will determine a factor that scales the min intensity to black and the max intensity to white. This is applied to every pixel in the image which produces the final result. 

11. ###### Position of MaxPooling: 

    if we have small size of image we can add max pooling in early layers. we generally add max pooling after formation of edges and gradients. generally, after 11X11 edges and gradient formed in image. To see image and gradients in an image zoom out image as much as possible and see the 11X11 area.

    

12. Concept of Transition Layers:

13. Position of Transition Layer:

14. Number of Epochs and when to increase them:

15. DropOut

16. When do we introduce DropOut, or when do we know we have some overfitting

17. The distance of MaxPooling from Prediction,

18. The distance of Batch Normalization from Prediction,

19. When do we stop convolutions and go ahead with a larger kernel or some other alternative (which we have not yet covered)

20. How do we know our network is not going well, comparatively, very early

21. Batch Size, and effects of batch size

22. When to add validation checks

23. LR schedule and concept behind it

24. Adam vs SGD

