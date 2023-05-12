# Opening-and-Closing

## Aim:

To implement Opening and Closing using Python and OpenCV.

## Software Required:

1. Anaconda - Python 3.7
2. OpenCV

## Algorithm:

### Step 1:

Load the necessary packages requiured for the implemtation of opening and closing.

### Step 2:

Create the text image for the implemtation of opening and closing using cv2.putText function.

### Step 3:

Create the structuring image for the implemtation of opening and closing on the text image.

### Step 4:

Apply the erosion and dilation to the text image using cv2.MORPH_OPEN and cv2.MORPH_CLOSE.

### Step 5:

Display the images of the erosion and dilation applied using the plt.imshow.

### Step 6:

End the program.
 
## Program:

``` python

# Import the necessary packages:

import cv2
import numpy as np
import matplotlib.pyplot as plt

# Create the Text using cv2.putText:

text_image = np.zeros((100,450),dtype = 'uint8')
font = cv2.FONT_HERSHEY_SIMPLEX = 4
cv2.putText(text_image,"Guru Prasad",(5,70),font,2,(255),5,cv2.LINE_AA)
plt.title("Original Image")
plt.imshow(text_image,'magma')
plt.axis('off')

# Create the structuring element:

kernel = cv2.getStructuringElement(cv2.MORPH_CROSS,(9,9))

# Use Opening operation:

image1=cv2.morphologyEx(text_image,cv2.MORPH_OPEN,kernel)
plt.title("Opening")
plt.imshow(image1,'magma')
plt.axis('off')

# Use Closing Operation:

image2=cv2.morphologyEx(text_image,cv2.MORPH_CLOSE,kernel)
plt.title("Closing")
plt.imshow(image2,'magma')
plt.axis('off')

```

## Output:

### Display the input Image:

![img1](https://github.com/Guruprasad21002001/Opening-and-Closing/assets/95342910/fac09670-7e18-43c2-b2e3-d783dbefa765)

### Display the result of Opening:

![img2](https://github.com/Guruprasad21002001/Opening-and-Closing/assets/95342910/4220f9d0-c27e-4e6f-af7d-c0b9852b3b47)

### Display the result of Closing:

![img3](https://github.com/Guruprasad21002001/Opening-and-Closing/assets/95342910/d65cd116-73a0-43cf-872f-db17ca73873e)

## Result:

Thus the Opening and Closing operation is used in the image using python and OpenCV.

