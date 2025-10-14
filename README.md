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
###PROGRAM
### ORIGINAL IMAGE
```
NAME : SUBASH E
REG NO : 212223040209



import cv2
import numpy as np
import matplotlib.pyplot as plt

image = cv2.imread('Shanks.jpeg')
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title('Original Image')
plt.axis('off')
```
### SOBEL EDGE DETECTOR
```
sobel_x = cv2.Sobel(gray_image, cv2.CV_64F, 1, 0, ksize=5) 
sobel_y = cv2.Sobel(gray_image, cv2.CV_64F, 0, 1, ksize=5)  
sobel_combined = cv2.magnitude(sobel_x, sobel_y)  
plt.imshow(sobel_combined, cmap='gray')
plt.title('Sobel Edge Detection')
plt.axis('off')
```
### LAPLACIAN EDGE DETECTOR
```
laplacian = cv2.Laplacian(gray_image, cv2.CV_64F)
plt.imshow(laplacian, cmap='gray')
plt.title('Laplacian Edge Detection')
plt.axis('off')
```
### CANNY EDGE DETECTOR
```
canny_edges = cv2.Canny(gray_image, 50, 150)
plt.imshow(canny_edges, cmap='gray')
plt.title('Canny Edge Detection')
plt.axis('off')  
```
## Output:
###ORIGINAL IMAGE 
<img width="614" height="628" alt="Screenshot 2025-09-29 085156" src="https://github.com/user-attachments/assets/97ca9e54-26b2-4ef0-849c-abb47f552fd4" />

### SOBEL EDGE DETECTOR
<img width="627" height="634" alt="Screenshot 2025-09-29 085236" src="https://github.com/user-attachments/assets/8ff7569d-5580-4f90-81d3-3cdd7545806e" />



### LAPLACIAN EDGE DETECTOR
<img width="620" height="630" alt="Screenshot 2025-09-29 085318" src="https://github.com/user-attachments/assets/3d0e2fa8-f13b-4abc-93de-5c1ded73c650" />



### CANNY EDGE DETECTOR
<img width="605" height="627" alt="Screenshot 2025-09-29 085348" src="https://github.com/user-attachments/assets/89ff1ab3-9c01-4f90-a78d-da6c4b595e3a" />


## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
