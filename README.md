# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary packages

### Step2:
Create the text using cv2.putText

### Step3:
Create the structuring element

### Step4:
Erode the image

### Step5:
Dilate the Image
 
## Program:
# Import the necessary packages
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
```


# Create the Text using cv2.putText
```
img = np.zeros((100,400),dtype='uint8')
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img,'MADHAV',(40,70),font,2,(255),5,cv2.LINE_AA)
plt.imshow(img)
plt.axis('off')
```

# Create the structuring element
```
kernel = np.ones((5,5),np.uint8)
kernel1 = cv2.getStructuringElement(cv2.MORPH_CROSS,(5,5))
```
# Erode the image
```
img_erode = cv2.erode(img,kernel1)
plt.imshow(img_erode)
plt.axis('off')
```

# Dilate the image
```
img_dilate = cv2.dilate(img,kernel1)
plt.imshow(img_dilate)
plt.axis('off')
```



## Output:

### Display the input Image
![image](https://github.com/23004426/erosion--dilation/assets/144979327/088bb0cc-f5d3-4080-b5ba-a0c9bc68bb02)

### Display the Eroded Image
![image](https://github.com/23004426/erosion--dilation/assets/144979327/8770a066-6e68-4e6f-b610-3d88cf04e5c2)

### Display the Dilated Image
![image](https://github.com/23004426/erosion--dilation/assets/144979327/0513cdf8-db81-4368-82bd-f2190e63829b)


## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
