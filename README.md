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

i) Using Averaging Filter
```
kernel=np.ones((11,11),np.float32)/121
image3=cv2.filter2D(image2,-1,kernel)
plt.figure(figsize=(8,8))
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

gaussian_blur=cv2.GaussianBlur(image2,(33,33),0,0)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(gaussian_blur)
plt.title("Gaussian Blur")
plt.axis("off")
plt.show()



iv) Using Median Filter
```
median=cv2.medianBlur(image2,13)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(gaussian_blur)
plt.title("Median Blur")
plt.axis("off")
plt.show()

```

### 2. Sharpening Filters
i) Using Laplacian Kernal
```
kernel2=np.array([[-1,-1,-1],[2,-2,1],[2,1,-1]])
image3=cv2.filter2D(image2,-1,kernel2)
plt.figure(figsize=(8,8))
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
~~~

## OUTPUT:
### 1. Smoothing Filters


i) Using Averaging Filter

![Screenshot from 2023-04-05 13-53-42](https://user-images.githubusercontent.com/119559822/230024492-cbfea983-1ddd-469c-ba0f-6f240a7b0f76.png)

ii) Using Weighted Averaging Filter
 
![Screenshot from 2023-04-05 13-34-28](https://user-images.githubusercontent.com/119559822/230021813-2a750a82-30ff-415a-8833-7e0544898d1c.png)

iii) Using Gaussian Filter

![Screenshot from 2023-04-05 13-34-32](https://user-images.githubusercontent.com/119559822/230021990-e594434a-7c77-495f-81bb-afdb075df820.png)

iv) Using Median Filter

![Screenshot from 2023-04-05 13-34-44](https://user-images.githubusercontent.com/119559822/230023546-3df370c2-b428-4e1d-a97f-847186248d0a.png)

### 2. Sharpening Filters


i) Using Laplacian Kernal

![Screenshot from 2023-04-05 13-34-53](https://user-images.githubusercontent.com/119559822/230023620-239cdeac-1a59-4fe4-841a-57f4e91464b7.png)


ii) Using Laplacian Operator

![Screenshot from 2023-04-05 13-35-09](https://user-images.githubusercontent.com/119559822/230023646-b3d67e1f-e141-4721-b27c-0605cb4913d6.png)


## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
