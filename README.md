# EX-6
# EDGE-DETECTION
## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import all the necessary modules for the program.

### Step2:
Load a image using imread() from cv2 module.

### Step3:
Convert the image to grayscale

### Step4:
Using Sobel operator from cv2,detect the edges of the image.

### Step5:

Using Laplacian operator from cv2,detect the edges of the image and Using Canny operator from cv2,detect the edges of the image.

## Program:

DEVELOPED BY : NIKSHITHA S
REGISTER NUMBER : 212224040220
``` py
import cv2
import numpy as np
import matplotlib.pyplot as plt

image = cv2.imread('Tiger.jpg')  # Replace with your image path
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
# Original Image
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title('Original Image')
plt.axis('off')
```
<img width="159" height="283" alt="image" src="https://github.com/user-attachments/assets/4cb0c3b0-ee29-429c-af93-3c17f588598f" />


### SOBEL EDGE DETECTOR
``` py
sobel_x = cv2.Sobel(gray_image, cv2.CV_64F, 1, 0, ksize=5)  # Sobel in x direction
sobel_y = cv2.Sobel(gray_image, cv2.CV_64F, 0, 1, ksize=5)  # Sobel in y direction
sobel_combined = cv2.magnitude(sobel_x, sobel_y)  # Combine both directions
plt.imshow(sobel_combined, cmap='gray')
plt.title('Sobel Edge Detection')
plt.axis('off')
```
<img width="161" height="281" alt="image" src="https://github.com/user-attachments/assets/086a6e45-4ca1-49d8-b37c-2ed166ba59f5" />


### LAPLACIAN EDGE DETECTOR
``` py
laplacian = cv2.Laplacian(gray_image, cv2.CV_64F)
plt.imshow(laplacian, cmap='gray')
plt.title('Laplacian Edge Detection')
plt.axis('off')
```
<img width="161" height="290" alt="image" src="https://github.com/user-attachments/assets/f3e689a0-3900-45ea-a84e-a33cbf0e9716" />

### CANNY EDGE DETECTOR
``` py
canny_edges = cv2.Canny(gray_image, 50, 150)
plt.imshow(canny_edges, cmap='gray')
plt.title('Canny Edge Detection')
plt.axis('off')  
```
<img width="159" height="290" alt="image" src="https://github.com/user-attachments/assets/585c7b46-8be3-4d86-8c35-750e6de96043" />



## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
