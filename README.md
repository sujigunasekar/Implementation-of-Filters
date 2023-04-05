# Implementation-of-Filters
## Aim:
To implement filters for smoothing and sharpening the images in the spatial domain.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1
Import necessary packages numpy,cv2 and matplotlib and save the image which you would like to perform Image filtering.


### Step2
Perform filtering of image.

### Step3
Perform average filter.

### Step4
Perform weighted average filter.

### Step5
Perform gaussian filter.

### Step6
Perform median filter.

### Step7
Perform Laplacian kernel filter.

### Step8
Perform Laplacian operator.

### Step9
Run the programs and execute the output.

## Program:
### Developed By   :Suji.G
### Register Number:212222230152
~~~
import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("tae.jpg")
image2=cv2.cvtColor(image1,cv2.COLOR_BGR2RGB)
### 1. Smoothing Filters
~~~
kernel=np.array([[1,2,1],[2,4,2],[1,2,1]])/16
image3=cv2.filter2D(image2,-1,kernel)
plt.figure(figsize = (12,12))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title('Original')
plt.axis('off')
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title('Weighted average Filtered')
plt.axis('off')
~~~
i) Using Averaging Filter
```
gaussian_blur=cv2.GaussianBlur(src=image2,ksize=(11,11),sigmaX=0,sigmaY=0)
plt.figure(figsize = (12,12))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title('Original')
plt.axis('off')
plt.subplot(1,2,2)
plt.imshow(gaussian_blur)
plt.title('Gaussian Filtered')
plt.axis('off')

```
ii) Using Weighted Averaging Filter
```
kernel=np.array([[1,2,1],[2,4,2],[1,2,1]])/16
image3=cv2.filter2D(image2,-1,kernel)
plt.figure(figsize = (12,12))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title('Original')
plt.axis('off')
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title('Weighted average Filtered')
plt.axis('off')

```
iii) Using Gaussian Filter
```
median=cv2.medianBlur(src=image2,ksize=11)
plt.figure(figsize = (12,12))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title('Original')
plt.axis('off')
plt.subplot(1,2,2)
plt.imshow(median)
plt.title('Median Filtered')
plt.axis('off')

```

iv) Using Median Filter
```
kernel=np.array([[0,1,0],[1,-4,1],[0,1,0]])
image3=cv2.filter2D(image2,-1,kernel)
plt.figure(figsize = (12,12))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title('Original')
plt.axis('off')
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title('Laplacian kernel Filtered')
plt.axis('off')

```

### 2. Sharpening Filters
i) Using Laplacian Kernal
```
lap_operator=cv2.Laplacian(image2,cv2.CV_64F)
plt.figure(figsize = (12,12))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title('Original')
plt.axis('off')

plt.subplot(1,2,2)
plt.imshow(lap_operator)
plt.title('Laplacian operator Filtered')
plt.axis('off')

```
ii) Using Laplacian Operator
```
laplacian=cv2.Laplacian(image2,cv2.CV_64F)
plt.figure(figsize=(8,8))
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

![Screenshot from 2023-04-05 13-34-28](https://user-images.githubusercontent.com/119559822/230021888-c1cb10da-01f8-45c5-81a7-ae372660cd64.png)

ii) Using Weighted Averaging Filter

![Screenshot from 2023-04-05 13-34-28](https://user-images.githubusercontent.com/119559822/230021813-2a750a82-30ff-415a-8833-7e0544898d1c.png)

iii) Using Gaussian Filter

![Screenshot from 2023-04-05 13-34-32](https://user-images.githubusercontent.com/119559822/230021990-e594434a-7c77-495f-81bb-afdb075df820.png)

iv) Using Median Filter


### 2. Sharpening Filters


i) Using Laplacian Kernal



ii) Using Laplacian Operator




## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
