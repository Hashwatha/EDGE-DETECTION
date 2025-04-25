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

## Code
### Developed by : Hashwatha M
### Register Number : 212223240051
## Original
```
import cv2
import numpy as np
import matplotlib.pyplot as plt

image = cv2.imread('sunrise.jpg')
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

## Original
![image](https://github.com/user-attachments/assets/9b8827b4-c59c-416f-b0a8-053400a5ac8a)

## SOBEL EDGE DETECTOR
![image](https://github.com/user-attachments/assets/b5d0c2f5-623c-42cc-ac28-227164ba92e2)

## LAPLACIAN EDGE DETECTOR
![image](https://github.com/user-attachments/assets/2ee0d351-656a-402a-8ca4-ca792a1d3880)

## CANNY EDGE DETECTOR
![image](https://github.com/user-attachments/assets/93949630-0179-4cdf-a1de-feecac3ed396)

## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
