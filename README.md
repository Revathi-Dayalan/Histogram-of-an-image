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
# Developed By: Revathi Dayalan
# Register Number: 212221240045


# Write your code to find the histogram of gray scale image and color image channels.
import cv2
import matplotlib.pyplot as plt
Gray_image=cv2.imread('parrot.png')
plt.imshow(Gray_image)
plt.show()
hist=cv2.calcHist([Gray_image],[0],None,[256],[0,256])
plt.figure()
plt.title("Histogram")
plt.xlabel('grayscale value')
plt.ylabel('pixel count')
plt.stem(hist)
plt.show()


# Display the histogram of gray scale image and any one channel histogram from color image
import cv2
import matplotlib.pyplot as plt
Color_image=cv2.imread('dog.jpg')
plt.imshow(Color_image)
plt.show()
hist1=cv2.calcHist([Color_image],[1],None,[256],[0,256])
plt.figure()
plt.title("Histogram")
plt.xlabel('Intensity value')
plt.ylabel('pixel count')
plt.stem(hist1)
plt.show()



# Write the code to perform histogram equalization of the image. 
import cv2
Gray_image=cv2.imread('parrot.png',0)
equ=cv2.equalizeHist(Gray_image)
cv2.imshow('Gray Image',Gray_image)
cv2.imshow('Equalized Image',equ)
cv2.waitKey(0)
cv2.destroyAllWindows()

```
## Output:
### Input Grayscale Image and Color Image
![o1i](https://user-images.githubusercontent.com/96000574/166145315-9ad1c7d7-1573-4aea-b99f-60407fc56042.PNG)
![o1ii](https://user-images.githubusercontent.com/96000574/166145318-6ce74c36-6912-4204-8435-b0cdb273e2c1.PNG)

<br>
<br>
<br>
<br>

### Histogram of Grayscale Image and any channel of Color Image
![02i](https://user-images.githubusercontent.com/96000574/166145327-4ec59b47-49e2-4f03-b3b9-dd986026ccad.PNG)
![o2ii](https://user-images.githubusercontent.com/96000574/166145333-7a3c15e9-3be3-4544-9cf7-22bf1738b183.PNG)

<br>
<br>
<br>
<br>

### Histogram Equalization of Grayscale Image

![o3](https://user-images.githubusercontent.com/96000574/166145336-88f6bd58-12a8-4a9e-8e8f-c62811e1d368.PNG)

<br>
<br>
<br>
<br>

## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
