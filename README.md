# Implementation-of-Erosion-and-Dilation
## AIM:
To implement Erosion and Dilation using Python and OpenCV.

## SOFTWARE REQUIRED:
1. Anaconda - Python 3.7
2. OpenCV

## ALGORITHMl
### Step1:
Import the necessary packages.
<br>

### Step2:
Create the text image using cv2.putText.
<br>

### Step3:
Then create the structuring image for dilation/erosion.
<br>

### Step4:
Apply erosion and dilation using cv2.erode and cv2.dilate.
<br>

### Step5:
Plot the images using plt.imshow.
<br>

   
## PROGRAM:

``` Python
# Import the necessary packages
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Create the Text using cv2.putText
text_image = np.zeros((100,440),dtype = 'uint8')
font = cv2.FONT_HERSHEY_SIMPLEX = 3
cv2.putText(text_image," Evangelin.S",(5,70),font,2,(255),5,cv2.LINE_AA)
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
## OUTPUT:

### Display the input Image
![image](https://github.com/Evangelin-Ruth/erosion--dilation/assets/94219798/1901b89a-b478-428a-bf24-0208a73f697d)

<br>

### Display the Eroded Image
![image](https://github.com/Evangelin-Ruth/erosion--dilation/assets/94219798/54c8d7e1-862b-415f-bcad-37bfb215f182)

<br>

### Display the Dilated Image
![Uploading image.png…]()
<br>

## RESULT:
Thus the generated text image is eroded and dilated using python and OpenCV.
