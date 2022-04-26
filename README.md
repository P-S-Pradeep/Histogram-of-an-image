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
```python
# Developed By:Pradeep P S
# Register Number:212220230034
import cv2
import matplotlib.pyplot as plt

# Write your code to find the histogram of gray scale image and color image channels.
gi=cv2.imread("b.jpg",0)
ci=cv2.imread("a.jpg")
gi=cv2.resize(gi,(500,400))
ci=cv2.resize(ci,(500,400))
cv2.imshow("gi",gi)
cv2.imshow("ci",ci)
cv2.waitKey(0)
cv2.destroyAllWindows()


# Display the histogram of gray scale image and any one channel histogram from color image
hist=cv2.calcHist([gi],[0],None,[256],[0,255])
hist1=cv2.calcHist([ci],[2],None,[256],[0,255])
plt.figure()
plt.title("grey image")
plt.xlabel("greyscale value")
plt.ylabel("pixel count")
plt.stem(hist)
plt.show()
plt.figure()
plt.title("color image")
plt.xlabel("colorscale value")
plt.ylabel("pixel count")
plt.stem(hist1)
plt.show()


# Write the code to perform histogram equalization of the image. 
equ=cv2.equalizeHist(gi)
cv2.imshow("gi",gi)
cv2.imshow("df",equ)
cv2.waitKey(0)
cv2.destroyAllWindows()

```
## Output:
### Input Grayscale Image and Color Image
![Screenshot (69)]![Screenshot (1)](https://user-images.githubusercontent.com/102652887/165310432-921f7f85-8dd4-46d2-b22c-803bd6bcdf9e.png)



### Histogram of Grayscale Image and any channel of Color Image
![Screenshot (67)]![Screenshot (2)](https://user-images.githubusercontent.com/102652887/165310695-9fd5add4-54ba-401a-b401-9ba36961aeb6.png)



### Histogram Equalization of Grayscale Image
![Screenshot (70)]![Screenshot (3)](https://user-images.githubusercontent.com/102652887/165310748-78115deb-1e8e-472d-81b7-74c0dc7b1bf8.png)


## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
