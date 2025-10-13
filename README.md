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
## Developed by: Karan A
### Reg NO: 212223230099
``` 
import cv2
import numpy as np
import matplotlib.pyplot as plt
```
```
image = np.zeros((600, 600), dtype=np.uint8)
cv2.putText(image,text='KARAN A',org=(40,300),fontFace=cv2.FONT_HERSHEY_SIMPLEX,fontScale=4,color=(255,255,255),thickness=25,lineType=cv2.LINE_AA)
plt.imshow(image,cmap='gray')
plt.axis('off') 
plt.show()
```
```
kernel = np.ones((10, 10), np.uint8)
eroded_image = cv2.erode(image, kernel, iterations=1)
```
```
plt.imshow(eroded_image,cmap='gray')
plt.title("Eroded Image")
plt.axis('off')
```
```
dilated_image = cv2.dilate(image, kernel, iterations=1)
```
```
plt.imshow(dilated_image,cmap='gray') 
plt.title("Dilated Image")
plt.axis('off')
```
## Output:

### Display the input Image
<img width="389" height="389" alt="image" src="https://github.com/user-attachments/assets/f0558053-31d1-4eae-8806-a5d1db49bd68" />


### Display the Eroded Image
<img width="389" height="411" alt="image" src="https://github.com/user-attachments/assets/7058dfaf-ccb5-43b8-a6ac-e8a50f26644a" />


### Display the Dilated Image
<img width="389" height="411" alt="image" src="https://github.com/user-attachments/assets/d9cb679e-3bd8-4a2d-8ce4-c616c8e18bd2" />


## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
