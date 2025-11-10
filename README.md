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

### Code:
## Original:
```
import cv2
import numpy as np
import matplotlib.pyplot as plt

image = cv2.imread('spyd.jpg')
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title('Original Image')
plt.axis('off')
```
## SOBEL EDGE DETECTOR
```
sobel_x = cv2.Sobel(gray_image, cv2.CV_64F, 1, 0, ksize=5) 
sobel_y = cv2.Sobel(gray_image, cv2.CV_64F, 0, 1, ksize=5)  
sobel_combined = cv2.magnitude(sobel_x, sobel_y)  
plt.imshow(sobel_combined, cmap='gray')
plt.title('Sobel Edge Detection')
plt.axis('off')
```
## LAPLACIAN EDGE DETECTOR
```
laplacian = cv2.Laplacian(gray_image, cv2.CV_64F)
plt.imshow(laplacian, cmap='gray')
plt.title('Laplacian Edge Detection')
plt.axis('off')
```
## CANNY EDGE DETECTOR
```
canny_edges = cv2.Canny(gray_image, 50, 150)
plt.imshow(canny_edges, cmap='gray')
plt.title('Canny Edge Detection')
plt.axis('off')  
```
## Output:
### Original:
![WhatsApp Image 2025-11-10 at 21 15 12_628c2800](https://github.com/user-attachments/assets/c90bf6be-2b02-43dd-b426-af2094239d16)


### SOBEL EDGE DETECTOR
![WhatsApp Image 2025-11-10 at 21 15 15_6927ba23](https://github.com/user-attachments/assets/13db4f10-106c-4e01-b606-bf892ab9f74f)


### LAPLACIAN EDGE DETECTOR

![WhatsApp Image 2025-11-10 at 21 16 11_6a54e020](https://github.com/user-attachments/assets/2911b19f-4814-4f90-bce1-ff605c7a69f6)


### CANNY EDGE DETECTOR

![WhatsApp Image 2025-11-10 at 21 16 11_1e4117bb](https://github.com/user-attachments/assets/9776ed40-bb94-4b1d-9e3f-a1ce436b7490)


## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
