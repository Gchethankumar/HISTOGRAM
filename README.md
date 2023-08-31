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
 Developed By: G.Chethan kumar
 Register Number: 212222240022
```
# Write your code to find the histogram of gray scale image and color image channels.
```python
import cv2
import matplotlib.pyplot as plt
Gray_image = cv2.imread('rr.jpg')
color_image = cv2.imread('dodge.jpg')
plt.imshow(Gray_image)
plt.show()
plt.imshow(color_image)
plt.show()
```
# Display the histogram of gray scale image and any one channel histogram from color image
```python
import cv2
import matplotlib.pyplot as plt
gray_image = cv2.imread("rr.jpg")
color_image = cv2.imread("dodge.jpg")
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
```
# Write the code to perform histogram equalization of the image. 
```python
import cv2
import matplotlib.pyplot as plt
gray_image = cv2.imread('rr.jpg',0)
equ=cv2.equalizeHist(gray_image)
cv2.imshow('Gray image',gray_image)
cv2.imshow('Equalized Image',equ)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## Output:
### Input Grayscale Image and Color Image
![Screenshot from 2023-08-31 20-30-42](https://github.com/Gchethankumar/HISTOGRAM/assets/118348224/9f838e37-5fa9-4593-ad0a-8ac6bcafc024)
### Histogram of Grayscale Image and any channel of Color Image
![Screenshot from 2023-08-31 20-31-51](https://github.com/Gchethankumar/HISTOGRAM/assets/118348224/82ca7a5a-b3e4-4728-93d3-b97d23fe53b1)
![Screenshot from 2023-08-31 20-32-24](https://github.com/Gchethankumar/HISTOGRAM/assets/118348224/e59a67b9-5930-4075-90fc-4040766099ba)
### Histogram Equalization of Grayscale Image
![Screenshot from 2023-08-31 20-41-41](https://github.com/Gchethankumar/HISTOGRAM/assets/118348224/692a35db-6c68-46cb-8655-64905b48a561)
## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
