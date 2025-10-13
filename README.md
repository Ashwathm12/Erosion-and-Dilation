# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import required libraries (OpenCV, NumPy) and load the image in grayscale

### Step2:
Define a structuring element (kernel) for morphological operations.

### Step3:
Apply erosion using cv2.erode() on the image with the defined kernel.

### Step4:
Apply dilation using cv2.dilate() on the image with the same kernel.

### Step5:
Display and compare the original, eroded, and dilated images.
 
## Program
## Developed by: Ashwath M
### Reg NO: 212223230023
``` 
import cv2
import numpy as np
import matplotlib.pyplot as plt
```
```
def load_img():
    blank_img =np.zeros((800,800))
    font = cv2.FONT_HERSHEY_SIMPLEX
    cv2.putText(blank_img,text='ASHWATH',org=(50,300), fontFace=font,fontScale= 5,color=(255,255,255),thickness=25,lineType=cv2.LINE_AA)
    return blank_img
```
```
def display_img(img):
    fig = plt.figure(figsize=(12,10))
    ax = fig.add_subplot(111)
    ax.imshow(img,cmap='gray')
    plt.show()
```
```
img = load_img()
display_img(img)
```
```
kernel = np.ones((5,5),dtype=np.uint8)
erosion1 = cv2.erode(img,kernel,iterations = 3)
display_img(erosion1)
```
```
kernel = np.ones((5,5),dtype=np.uint8)
dilation = cv2.dilate(img,kernel,iterations = 2)
display_img(dilation)
```
## Output:

### Display the input Image
<img width="765" height="761" alt="image" src="https://github.com/user-attachments/assets/1be226b0-e608-42b2-9eb8-76df4880dc01" />



### Display the Eroded Image
<img width="767" height="762" alt="image" src="https://github.com/user-attachments/assets/59bc2adb-226f-4720-8197-287e9bad25e5" />



### Display the Dilated Image
<img width="782" height="757" alt="image" src="https://github.com/user-attachments/assets/84661ce2-d18f-47c2-ac40-ad9d1970cf15" />



## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
