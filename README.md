# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:s
### Step1:
<br>Import the necessary packages.

### Step2:
Create the text image using cv2.putText.

### Step3:
Then create the structuring image for dilation/erosion.

### Step4:
Apply erosion and dilation using cv2.erode and cv2.dilate.

### Step5:
Plot the images using plt.imshow.



 
## Program:
developed by VISMAYA.S
register number : 212221230125

``` Python
# Import the necessary packages

import cv2
import numpy as np
import matplotlib.pyplot as plt

# Create the Text using cv2.putText
text_image = np.zeros((100,440),dtype = 'uint8')
font = cv2.FONT_HERSHEY_SIMPLEX = 3
cv2.putText(text_image," VISMAYA.S",(5,70),font,2,(255),5,cv2.LINE_AA)
plt.title("Original Image")
plt.imshow(text_image,'magma')
plt.axis('off')


# Create the structuring element
kernel = cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))

# Erode the image
image_erode = cv2.erode(text_image,kernel)
plt.title("Eroded Image")
plt.imshow(image_erode,'magma')
plt.axis('off')


# Dilate the image
image_dilate = cv2.dilate(text_image,kernel)
plt.title("Dilated Image")
plt.imshow(image_dilate,'magma')
plt.axis('off')





```
## Output:

### Display the input Image
<br>![3](https://github.com/VismayaNair/Implementation-of-Erosion-and-Dilation/assets/93427210/4c2d64e7-b337-4b56-8c47-95d4c8528116)
<br>
<br>
<br>
<br>

### Display the Eroded Image
<br>![2](https://github.com/VismayaNair/Implementation-of-Erosion-and-Dilation/assets/93427210/d5d11956-c5cd-4618-85a4-9fc748545345)

<br>
<br>
<br>
<br>
<br>

### Display the Dilated Image
<br>![1](https://github.com/VismayaNair/Implementation-of-Erosion-and-Dilation/assets/93427210/a15db014-5faa-40f2-b285-ea6d9bd03adf)

<br>
<br>
<br>
<br>
<br>

## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
