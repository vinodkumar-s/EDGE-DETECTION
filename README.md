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
```python
DEVELOPED BY: VINOD KUMAR S
REGISTER NO: 212222240116
```
```python
import cv2
import matplotlib.pyplot as plt
img=cv2.imread("FLOWER.jpg",0)
gray=cv2.cvtColor(img,cv2.COLOR_GRAY2RGB)
img = cv2.GaussianBlur(gray,(3,3),0)

```
### SOBEL EDGE DETECTOR
#### SOBEL X AXIS ,SOBEL Y AXIS , SOBEL XY AXIS
```python
sobelx = cv2.Sobel(img,cv2.CV_64F,1,0,ksize=5)
sobely=cv2.Sobel(img,cv2.CV_64F,0,1,ksize=5)
sobelxy=cv2.Sobel(img,cv2.CV_64F,1,1,ksize=5)
plt.figure(1)
plt.subplot(2,2,1),plt.imshow(img,cmap='gray')
plt.title('Original'), plt.xticks([]), plt.yticks([])
plt.show()
plt.subplot(2,2,1),plt.imshow(sobelx,cmap='gray')
plt.axis('off')
plt.show()
plt.subplot(2,2,1),plt.imshow(sobely,cmap='gray')
plt.axis('off')
plt.show()
plt.subplot(2,2,1),plt.imshow(sobelxy,cmap='gray')
plt.axis('off')
plt.show()

```

### LAPLACIAN EDGE DETECTOR
```python
laplacian=cv2.Laplacian(gray,cv2.CV_64F)
plt.imshow(laplacian)
plt.subplot(2,2,1),plt.imshow(laplacian,cmap='gray')
plt.title("Laplacian Edge Detector")
plt.axis('off')
plt.show()
```
### CANNY EDGE DETECTOR
```python
canny=cv2.Canny(gray,120,150)
plt.subplot(1,2,2)
plt.imshow(canny)
plt.title("Canny Edge Detector")
plt.axis("off")
plt.show()
```

## Output:
## ORIGINAL IMAGE:
![Screenshot 2024-04-12 211059](https://github.com/vinodkumar-s/EDGE-DETECTION/assets/113497226/839caa82-3470-4c74-866f-cb4b274ad036)

### SOBEL EDGE DETECTOR
#### SOBEL X AXIS

![Screenshot 2024-04-12 211219](https://github.com/vinodkumar-s/EDGE-DETECTION/assets/113497226/e61fa4e3-7ff2-4112-a920-055206e537f3)



#### SOBEL Y AXIS

![Screenshot 2024-04-12 211242](https://github.com/vinodkumar-s/EDGE-DETECTION/assets/113497226/5ac181a3-a995-4cf7-beea-56eaddf70185)


#### SOBEL XY AXIS

![Screenshot 2024-04-12 211305](https://github.com/vinodkumar-s/EDGE-DETECTION/assets/113497226/ead75058-2a61-4df7-818d-92c5a9cdb241)


### LAPLACIAN EDGE DETECTOR


![Screenshot 2024-04-12 211323](https://github.com/vinodkumar-s/EDGE-DETECTION/assets/113497226/cb7b71e5-a22d-44e6-a13a-6366eaeba9d3)


### CANNY EDGE DETECTOR

![Screenshot 2024-04-12 211332](https://github.com/vinodkumar-s/EDGE-DETECTION/assets/113497226/2f58d4c3-025f-4e55-86ad-3602d81239da)



## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
