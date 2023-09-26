# HISTOGRAM
# Histogram and Histogram Equalization of an image
## Aim
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the necessary libraries and read two images, Color image and Gray Scale image.

### Step2:
Calculate the Histogram of Gray scale image and each channel of the color image.

### Step3:
Display the histograms with their respective images.

### Step4:
Equalize the grayscale image.

### Step5:
Display the grayscale image.

## Program:
```
# Developed By:IYYANAR S
# Register Number:212222240036
```
```
import cv2
import matplotlib.pyplot as plt
# Write your code to find the histogram of gray scale image and color image channels.
import cv2
import matplotlib.pyplot as plt
Gray_image=cv2.imread('is.jpeg')
plt.imshow(Gray_image)
plt.show()
color_image=cv2.imread('iss.jpeg')
plt.imshow(color_image)
plt.show()
# Display the histogram of gray scale image and any one channel histogram from color image
import cv2
import matplotlib.pyplot as plt
gray_image = cv2.imread("is.jpeg")
color_image = cv2.imread("iss.jpeg")
gray_hist = cv2.calcHist([gray_image],[0],None,[256],[0,256])
color_hist = cv2.calcHist([color_image],[0],None,[256],[0,256])
plt.figure()
plt.imshow(gray_image)
plt.show()
plt.title("Histogram")
plt.xlabel("Grayscale Value")
plt.ylabel("Pixel Count")
plt.stem(gray_hist)
plt.show()

plt.imshow(color_image)
plt.show()
plt.title("Histogram of Color Image - Green Channel")
plt.xlabel("Intensity Value")
plt.ylabel("Pixel Count")
plt.stem(color_hist)
plt.show()

# Write the code to perform histogram equalization of the image. 
import cv2
import matplotlib.pyplot as plt
gray_image = cv2.imread('is.jpeg',0)
equ=cv2.equalizeHist(gray_image)
cv2.imshow('Gray image',gray_image)
cv2.imshow('Equalized Image',equ)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## Output:
### Input Grayscale Image and Color Image
![4IM1](https://github.com/Iyyanar22009120/HISTOGRAM/assets/118680259/5e84f038-e7f6-40b4-aa31-2ca342b12bd6)
![4IM2](https://github.com/Iyyanar22009120/HISTOGRAM/assets/118680259/835b9de8-3e90-4434-87f6-907dad49c300)


### Histogram of Grayscale Image and any channel of Color Image
![4IM3](https://github.com/Iyyanar22009120/HISTOGRAM/assets/118680259/ce478b13-97c8-4a2a-bb66-ea572af7c69c)
![4IM4](https://github.com/Iyyanar22009120/HISTOGRAM/assets/118680259/8ea3457f-e1f4-4ea1-a7a3-28b66afbdb4b)


### Histogram Equalization of Grayscale Image
![4IM5](https://github.com/Iyyanar22009120/HISTOGRAM/assets/118680259/c7ef469f-ab88-4812-ade2-7e1c27eaadf1)


## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
