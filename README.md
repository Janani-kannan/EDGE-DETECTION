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

## Output:

###ORIGINAL IMAGE
```
import cv2
import numpy as np
import matplotlib.pyplot as plt

image = cv2.imread("C:\\Users\\admin\\Downloads\\catttt.jpeg")
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title('Original Image')
plt.axis('off')
```
<img width="955" height="562" alt="image" src="https://github.com/user-attachments/assets/2332fffa-0209-4c72-8ce5-37323936bf08" />


### SOBEL EDGE DETECTOR


```
sobel_x = cv2.Sobel(gray_image, cv2.CV_64F, 1, 0, ksize=5) 
sobel_y = cv2.Sobel(gray_image, cv2.CV_64F, 0, 1, ksize=5)  
sobel_combined = cv2.magnitude(sobel_x, sobel_y)  
plt.imshow(sobel_combined, cmap='gray')
plt.title('Sobel Edge Detection')
plt.axis('off')

```

<img width="895" height="562" alt="image" src="https://github.com/user-attachments/assets/538055fa-97a1-4c0d-b11a-c4e9a419b95b" />


### LAPLACIAN EDGE DETECTOR

```

laplacian = cv2.Laplacian(gray_image, cv2.CV_64F)
plt.imshow(laplacian, cmap='gray')
plt.title('Laplacian Edge Detection')
plt.axis('off')

```

<img width="937" height="554" alt="image" src="https://github.com/user-attachments/assets/fe2ebe33-d83b-4a6a-a844-8b658e5afb25" />

### CANNY EDGE DETECTOR

```

canny_edges = cv2.Canny(gray_image, 50, 150)
plt.imshow(canny_edges, cmap='gray')
plt.title('Canny Edge Detection')
plt.axis('off')

```

<img width="910" height="556" alt="image" src="https://github.com/user-attachments/assets/ee8e2986-6ff7-4f5e-9e63-83d01d848ae1" />

## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
