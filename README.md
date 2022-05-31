# Edge-Detection
## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the necessary modules.
<br>
### Step2:
For performing edge detection on a image.
<br>
 1) Sobel :
 ```
 sobelx=cv2.Sobel(img,cv2.CV_64F,1,0,5)
 sobely=cv2.Sobel(img,cv2.CV_64F,0,1,5)
 sobelxy=cv2.Sobel(img,cv2.CV_64F,1,1,5)
 ```
 2) Laplacian :
 ```
 Laplacian=cv2.Laplacian(img,cv2.CV_64F)
 ```
 3) Canny :
 ```
 canny=cv2.Canny(img,120,150)
 ```
## Program:

``` Python
# Import the packages
import cv2 
import matplotlib.pyplot as plt

# Load the image, Convert to grayscale and remove noise
img=cv2.imread("leaf.jpg",0)
img=cv2.cvtColor(img,cv2.COLOR_BGR2RGB)
img=cv2.GaussianBlur(img,(3,3),0)
plt.imshow(img)
plt.axis("off")
plt.show()

# SOBEL EDGE DETECTOR
sobelx=cv2.Sobel(img,cv2.CV_64F,1,0,5)
sobely=cv2.Sobel(img,cv2.CV_64F,0,1,5)
sobelxy=cv2.Sobel(img,cv2.CV_64F,1,1,5)

# LAPLACIAN EDGE DETECTOR
Laplacian=cv2.Laplacian(img,cv2.CV_64F)

# CANNY EDGE DETECTOR
canny=cv2.Canny(img,120,150)

plt.figure(figsize=(20,20))
plt.subplot(1,2,1)
plt.axis("off")
plt.title('Original image')
plt.imshow(img)
plt.subplot(1,2,2)
plt.axis("off")
plt.title('Sobel X axis')
plt.imshow(sobelx)
plt.show()

plt.figure(figsize=(20,20))
plt.subplot(1,2,1)
plt.axis("off")
plt.title('Original image')
plt.imshow(img)
plt.subplot(1,2,2)
plt.axis("off")
plt.title('Sobel Y axis')
plt.imshow(sobely)
plt.show()

plt.figure(figsize=(20,20))
plt.subplot(1,2,1)
plt.axis("off")
plt.title('Original image')
plt.imshow(img)
plt.subplot(1,2,2)
plt.axis("off")
plt.title('Sobel X and Y axis')
plt.imshow(sobelxy)
plt.show()

plt.figure(figsize=(20,20))
plt.subplot(1,2,1)
plt.axis("off")
plt.title('Original image')
plt.imshow(img)
plt.subplot(1,2,2)
plt.axis("off")
plt.title('Laplacian')
plt.imshow(Laplacian)
plt.show()

plt.figure(figsize=(20,20))
plt.subplot(1,2,1)
plt.axis("off")
plt.title('Original image')
plt.imshow(img)
plt.subplot(1,2,2)
plt.axis("off")
plt.title('Canny')
plt.imshow(canny)
plt.show()

```
## Output:
### SOBEL EDGE DETECTOR

![image](https://user-images.githubusercontent.com/103049243/171138909-53a98a2f-3bff-4786-8553-b34461da83f7.png)
![image](https://user-images.githubusercontent.com/103049243/171138951-48526410-c628-400c-803a-ee643a986bb9.png)
![image](https://user-images.githubusercontent.com/103049243/171139002-34d65a5a-fdfc-4062-8ed9-b07fc98d88c6.png)


### LAPLACIAN EDGE DETECTOR
![image](https://user-images.githubusercontent.com/103049243/171139115-aa0475ca-1ec4-442a-8666-f25cb4dab3cd.png)

### CANNY EDGE DETECTOR
![image](https://user-images.githubusercontent.com/103049243/171139194-5852614d-fd8e-46a9-ab02-6a79fa09cf42.png)


## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
