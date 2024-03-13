# Histogram-of-an-images
## Aim
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Read the gray and color image using imread()

### Step2:
Print the image using imshow().



### Step3:
Use calcHist() function to mark the image in graph frequency for gray and color image.

### step4:
Use calcHist() function to mark the image in graph frequency for gray and color image.

### Step5:
The Histogram of gray scale image and color image is shown.


## Program:
```python
# Developed By:RAGUNATH R
# Register Number:212222240081

import cv2
import matplotlib.pyplot as plt
Gray_image = cv2.imread('img1.jpeg')
Color_image = cv2.imread('img0.jpeg')
plt.imshow(Gray_image)
plt.show()
plt.imshow(Color_image)
plt.show()

hist=cv2.calcHist([Gray_image],[0],None,[256],[0,256])
hist1=cv2.calcHist([Color_image],[1],None,[256],[0,256])

plt.figure()
plt.title("Histogram")
plt.xlabel('grayscale value')
plt.ylabel('pixel count')
plt.stem(hist)
plt.show()

plt.figure()
plt.title("Histogram")
plt.xlabel('grayscale value')
plt.ylabel('pixel count')
plt.stem(hist1)
plt.show()

gray_image=cv2.imread("greyscale.jpeg",0)
equ=cv2.equalizeHist(gray_image)
cv2.imshow("Equlaized image",equ)
cv2.waitKey(0)
cv2.destroyAllWindows()

```
## Output:
### Input Grayscale Image and Color Image
![image](https://github.com/Ragu-123/Histogram-of-an-images/assets/113915622/1162b9da-d877-4094-a16b-4b50c9c59c73)
![image](https://github.com/Ragu-123/Histogram-of-an-images/assets/113915622/010bea4b-3395-47f0-a6b2-517381405344)


### Histogram of Grayscale Image and any channel of Color Image
![image](https://github.com/Ragu-123/Histogram-of-an-images/assets/113915622/3f88318e-94c5-435b-a6fb-81cd450702e1)
![image](https://github.com/Ragu-123/Histogram-of-an-images/assets/113915622/b96394a0-e1a3-4f88-a0c9-40143f6aa894)




### Histogram Equalization of Grayscale Image.
![image](https://github.com/Ragu-123/Histogram-of-an-images/assets/113915622/c5b84a79-d1a9-408b-8992-f1d446ee0293)



## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
