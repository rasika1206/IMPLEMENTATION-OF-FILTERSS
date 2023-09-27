# IMPLEMENTATION-OF-FILTERSS
## Aim:
To implement filters for smoothing and sharpening the images in the spatial domain.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1
Import the required modules.

### Step2
Convert the image from BGR to RGB.

### Step3
Apply the required filters for the image separately.
### Step4
Plot the original and filtered image by using matplotlib.pyplot

### Step5
End the program

## Program:
### Developed By   : rasika
### Register Number: 212222230117
</br>

### 1. Smoothing Filters
```
import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("tulip.jpg")
image2=cv2.cvtColor(image1,cv2.COLOR_BGR2RGB)
```
i) Using Averaging Filter
```
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
```
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
```
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
```
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
```
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
```
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
</br>

i) Using Averaging Filter
</br>![Screenshot from 2023-09-27 11-29-03](https://github.com/rasika1206/IMPLEMENTATION-OF-FILTERSS/assets/124434806/a412dc4e-5b10-40f0-a7f0-571f2892aeed)

</br>
</br>
</br>


ii) Using Weighted Averaging Filter
</br>![Screenshot from 2023-09-27 11-29-45](https://github.com/rasika1206/IMPLEMENTATION-OF-FILTERSS/assets/124434806/8069a112-a50d-49e2-b4d6-f0d60fd94d6a)

</br>
</br>
</br>
</br>

iii) Using Gaussian Filter
</br>![Screenshot from 2023-09-27 11-30-18](https://github.com/rasika1206/IMPLEMENTATION-OF-FILTERSS/assets/124434806/8a301242-63aa-4820-b657-5589c6793155)

</br>
</br>
</br>
</br>

iv) Using Median Filter
</br>![Screenshot from 2023-09-27 11-31-00](https://github.com/rasika1206/IMPLEMENTATION-OF-FILTERSS/assets/124434806/78ef83d4-0f55-47f6-a772-a435b51f51b9)

</br>
</br>
</br>
</br>

### 2. Sharpening Filters
</br>

i) Using Laplacian Kernal
</br>![Screenshot from 2023-09-27 11-31-52](https://github.com/rasika1206/IMPLEMENTATION-OF-FILTERSS/assets/124434806/1dffe04a-84ea-4eed-a7c7-d51582884276)

</br>
</br>
</br>
</br>

ii) Using Laplacian Operator
</br>
</br>![Screenshot from 2023-09-27 11-32-26](https://github.com/rasika1206/IMPLEMENTATION-OF-FILTERSS/assets/124434806/bd97f83b-02c6-4d81-a05c-7e25ef87ed00)

</br>
</br>
</br>

## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
