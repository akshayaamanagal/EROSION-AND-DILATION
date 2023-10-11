# EROSION-AND-DILATION

# Aim
To implement Erosion and Dilation using Python and OpenCV.
# Software Required
1. Anaconda - Python 3.7
2. OpenCV
# Algorithm:
## Step1:
Import the necessary packages.
## Step2:
Create the text using cv2.putText.
## Step3:
Then create the structuring image for dilation/erosion.
## Step4:
Apply erosion and dilation using plt.erode and plt.dilate.
## Step5: 
Plot the images using plt.imshow.
# Program:

``` Python
# Import the necessary packages

import numpy as np
import cv2
import matplotlib.pyplot as plt

# Create the Text using cv2.putText
image = np.zeros((100,500),dtype = 'uint8')
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(image,"AKSHAYAA M",(5,70),font,2,(255),5,cv2.LINE_AA)
plt.imshow(image,cmap='gray')
plt.title('Input Text'), plt.xticks([]), plt.yticks([])
plt.show()

# Create the structuring element
kernel=cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))

# Erode the image
image_erode=cv2.erode(image,kernel)
plt.imshow(image_erode,cmap='gray')
plt.title('Eroded Text'), plt.xticks([]), plt.yticks([])
plt.show()

# Dilate the image
image_dilate=cv2.dilate(image,kernel)
plt.imshow(image_dilate,cmap='gray')
plt.title('Dilated Text'), plt.xticks([]), plt.yticks([])
plt.show()
```
# Output:
## Display the input Image
![EROSION-AND-DILATION](1.png)
## Display the Eroded Image
![EROSION-AND-DILATION](2.png)
## Display the Dilated Image
![EROSION-AND-DILATION](3.png)
# Result
Thus the generated text image is eroded and dilated using python and OpenCV.
