# Implementation-of-filter
## Aim:
To implement filters for smoothing and sharpening the images in the spatial domain.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1
Import the required libraries.


### Step2
Convert the image from BGR to RGB.


### Step3
Apply the required filters for the image separately.


### Step4
Plot the original and filtered image by using matplotlib.pyplot.


### Step5
End the program.


## Program:
```py
Developed By   : SUBIKSHAN P
Register Number: 212223240161
```
### 1. Smoothing Filters

i) Using Averaging Filter
```Python

import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("eiffel.png")
image2=cv2.cvtColor(image1,cv2.COLOR_BGR2RGB)
kernel=np.ones((11,11),np.float32)/169
image3=cv2.filter2D(image2,-1,kernel)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title("Average Filter Image")
plt.axis("off")
plt.show()

```
ii) Using Weighted Averaging Filter
```Python
kernel1=np.array([[1,2,1],[2,4,2],[1,2,1]])/16
image3=cv2.filter2D(image2,-1,kernel1)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title("Weighted Average Filter Image")
plt.axis("off")
plt.show()




```
iii) Using Gaussian Filter
```Python

gaussian_blur=cv2.GaussianBlur(image2,(33,33),0,0)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(gaussian_blur)
plt.title("Gaussian Blur")
plt.axis("off")
plt.show()



```

iv) Using Median Filter
```Python

median=cv2.medianBlur(image2,13)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(median)
plt.title("Median Blur")
plt.axis("off")
plt.show()



```

### 2. Sharpening Filters
i) Using Laplacian Kernal
```Python

kernel2=np.array([[-1,-1,-1],[2,-2,1],[2,1,-1]])
image3=cv2.filter2D(image2,-1,kernel2)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title("Laplacian Kernel")
plt.axis("off")
plt.show()



```
ii) Using Laplacian Operator
```Python


laplacian=cv2.Laplacian(image2,cv2.CV_64F)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(laplacian)
plt.title("Laplacian Operator")
plt.axis("off")
plt.show()


```

## OUTPUT:
### 1. Smoothing Filters
i) Using Averaging Filter

![Screenshot from 2024-03-11 21-26-57](https://github.com/22009011/Implementation-of-filter/assets/118343461/730065ef-4e50-435c-a43f-b3f862e4e7a5)




ii) Using Weighted Averaging Filter

![Screenshot from 2024-03-11 21-28-29](https://github.com/22009011/Implementation-of-filter/assets/118343461/8da10613-120c-430a-9fd7-06d07aa96709)



iii) Using Gaussian Filter

![gassin](https://github.com/22009011/Implementation-of-filter/assets/118343461/e450cb0e-9866-4234-aa45-79285bb96294)



iv) Using Median Filter

![medion](https://github.com/22009011/Implementation-of-filter/assets/118343461/86e588ef-10f9-40e6-90dc-a6d0645b47c6)




### 2. Sharpening Filters

i) Using Laplacian Kernal

![Screenshot from 2024-03-11 21-41-14](https://github.com/22009011/Implementation-of-filter/assets/118343461/171dfbd7-72d0-40e6-93f7-fded8538c052)



ii) Using Laplacian Operator

![Screenshot from 2024-03-11 21-42-46](https://github.com/22009011/Implementation-of-filter/assets/118343461/56013bf7-24e2-4880-a598-a8790fbd58eb)



## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
