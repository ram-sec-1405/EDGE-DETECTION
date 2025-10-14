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
![Screenshot 2025-04-22 214334](https://github.com/user-attachments/assets/96f5eff7-dc82-4b86-aaf7-dcb55a2c79a3)


### SOBEL EDGE DETECTOR
![Screenshot 2025-04-22 214313](https://github.com/user-attachments/assets/d9944a54-30f6-492d-97fe-58f7ecae749c)


### LAPLACIAN EDGE DETECTOR
![Screenshot 2025-04-22 214320](https://github.com/user-attachments/assets/cfc7c8dc-33ee-4fc5-811c-d62962c4c65a)


### CANNY EDGE DETECTOR
![Screenshot 2025-04-22 214327](https://github.com/user-attachments/assets/98f063be-b627-4384-8643-144457cdc07e)

## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
