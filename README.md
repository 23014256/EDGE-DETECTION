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

## Program Developed By:
- **Name:** Suman G 
- **Register Number:**  212223240163
```
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Load the image
image = cv2.imread('jpeg.jpeg')  
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
# Original Image
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

## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.


<img width="481" height="501" alt="image" src="https://github.com/user-attachments/assets/c3d630ce-3c77-470f-8297-afb8878b0502" />
<img width="456" height="536" alt="image" src="https://github.com/user-attachments/assets/d776aaed-2e04-4f00-aa1a-f387bad7076b" />
<img width="422" height="525" alt="image" src="https://github.com/user-attachments/assets/10fd40b0-c1c3-40e2-b7b9-2f2b93e6fb07" />
<img width="402" height="513" alt="image" src="https://github.com/user-attachments/assets/dd60106c-88a0-4539-b74f-2833c1712c87" />


Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
