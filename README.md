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

## PROGRAM:
## IMPORT PACKAGES AND LOAD IMAGES
  ```python
import cv2
import matplotlib.pyplot as plt

img=cv2.imread("edge.jpg",0)
gray=cv2.cvtColor(img,cv2.COLOR_GRAY2RGB)
gray = cv2.GaussianBlur(gray,(3,3),0)
```
## SOBEL EDGE DETECTOR:
**SOBEL X:**
  ```python
  sobelx = cv2.Sobel(gray,cv2.CV_64F,1,0,ksize=5)
plt.imshow(sobelx,cmap='gray')
plt.title("Sobel X axis")
plt.axis("off")
plt.show()
```
**SOBEL Y:**
```python
sobely = cv2.Sobel(gray,cv2.CV_64F,0,1,ksize=5)
plt.imshow(sobely,cmap='gray')
plt.title("Sobel Y axis")
plt.axis("off")
plt.show()
```
**SOBEL XY:**
  ```python
  sobelxy = cv2.Sobel(gray,cv2.CV_64F,1,1,ksize=5)
plt.imshow(sobelxy,cmap='gray')
plt.title("Sobel XY axis")
plt.axis("off")
plt.show()
```
## LAPLACIAN EDGE DETECTOR:
```python
lap=cv2.Laplacian(gray,cv2.CV_64F)
plt.imshow(lap,cmap='gray')
plt.title("Laplacian Edge Detector")
plt.axis("off")
plt.show()
```
## CANNY EDGE DETECTOR:
```python
canny=cv2.Canny(gray,120,150)
plt.imshow(canny,cmap='gray')
plt.title("Canny Edge Detector")
plt.axis("off")
plt.show()
```
## Output:
## ORIGINAL IMAGE:
![edge](https://github.com/sivaram-R/EDGE-DETECTION/assets/121165794/b365a9f6-e162-4ed9-8c2f-81dd2d511fc6)
### SOBEL EDGE DETECTOR:
![image](https://github.com/sivaram-R/EDGE-DETECTION/assets/121165794/0fc8f19f-0157-4f8b-ab9a-99b4b2583b8e)
![image](https://github.com/sivaram-R/EDGE-DETECTION/assets/121165794/1a008d86-2a9b-47d8-bc23-2937237e5ed8)
![image](https://github.com/sivaram-R/EDGE-DETECTION/assets/121165794/f366214e-ea6f-47b8-8332-bc8bd39a49fb)
### LAPLACIAN EDGE DETECTOR
![image](https://github.com/sivaram-R/EDGE-DETECTION/assets/121165794/3ebac1b5-c2b7-4424-95c0-833b4573f3dd)
### CANNY EDGE DETECTOR
![image](https://github.com/sivaram-R/EDGE-DETECTION/assets/121165794/554e2a6d-6673-4611-b060-ea987d25a1fa)
## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
