#### Channels

In ANN a channel is a container of specific kind of feature. for example: if RGB color scheme is used in CNN then information which is there in Red channel will not be moving in green channel or the information in green channel will not be moving in the blue channel. Here, we are discussing channels in terms of colors. Image can be devided into hundreds of channels and carry forward only those channels which helps to determine the object. or in other words we can say that all the feature of same type becomes channel.


#### Kernels

![kernel](https://github.com/bomila/eip3/blob/master/image_kernel.png)

In terms of image processing, kernel is two dimensional representation of numbers in matrix format. Each kernel is used for specific function like edge detection, sharpening of image, blurring etc. Convolution operation uses kernel matrix, the kernel size should be smaller than the original image. convolution operation on image is calculated as: multiply kernel with each corresponding pixel of image and sum the value of product. 


#### Why should we only (well mostly) use 3x3 Kernels?

![3X3 Convolution](https://github.com/bomila/eip3/blob/master/3X3%20Convolution.png)

we prefer 3X3 convolution because it is compute friendly. for blurring, sharpening or smoothing of image 3X3 kernel generally used. 

For example: let's say we have filter of 5x5 kernel with stride size of 2. For 1 channel, the receptive field would be 5 at cost of 25 (multiplication and addition) operation. At place of 5X5 kernel if we use two 3X3 filter  with stride size of 1,2 we will get same receptive field with less number of operation (3X3 + 3X3=18 operation).




#### How many times do we need to perform 3x3 convolution operation to reach 1x1 from 199x199 ?

199 | 197 | 195 | 193 | 191 | 189 | 187 | 185 | 183 | 181 | 179 | 177 | 175 | 173 | 171 | 169 | 167 | 165 | 163 | 161 | 159 |
157 | 155 | 153 | 151 | 149 | 147 | 145 | 143 | 141 | 139 | 137 | 135 | 133 | 131 | 129 | 127 | 125 | 123 | 121 | 119 | 117 |
115 | 113 | 111 | 109 | 107 | 105 | 103 | 101 | 99  | 97  | 95  | 93  | 91  | 89  | 87  | 85  | 83  | 81  | 79  | 77  | 75  |
73  | 71  | 69  | 67  | 65  | 63  | 61  | 59  | 57  | 55  | 53  | 51  | 49  | 47  | 45  | 43  | 41  | 39  | 37  | 35  | 33  |
31  | 29  | 27  | 25  | 23  | 21  | 19  | 17  | 15  | 13  | 11  | 9   |  7  | 5   |  3  |  1

Here, we need 78 convolution operation of 3*3 to reach receptive field of 1
