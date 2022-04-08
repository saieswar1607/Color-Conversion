# Color Conversion
## AIM
To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.

## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:

import opencv.
<br>

### Step2:

Read the original Image.
<br>

### Step3:

Store the required conversion of the image in a variable.
<br>

### Step4:

Show the image stored in the given variable.
<br>

### Step5:

Destroy all the windows and end the program.
<br>

## Program:
```python
# Developed By: Sai Eswar Kandukuri
# Register Number: 212221240020
# i) Convert BGR and RGB to HSV and GRAY

import cv2
house_color_image= cv2.imread('house.jpeg')
cv2.imshow ('Original image', house_color_image)
hsv_image= cv2.cvtColor (house_color_image, cv2.COLOR_BGR2HSV)
cv2.imshow('BGR2HSV', hsv_image)
hsv_image1 = cv2.cvtColor (house_color_image, cv2.COLOR_RGB2HSV)
cv2.imshow('RGB2HSV', hsv_image1)
gray_image= cv2.cvtColor (house_color_image, cv2.COLOR_BGR2GRAY)
cv2.imshow('BGR2GRAY', gray_image)
gray_image1 = cv2.cvtColor (house_color_image, cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY', gray_image1)
cv2.waitKey(0)
cv2.destroyAllWindows()

# ii)Convert HSV to RGB and BGR

import cv2
house_HSV_image= cv2.imread('house.jpeg')
cv2.imshow('Original HSV image',house_HSV_image)
RGB_image = cv2.cvtColor(house_HSV_image, cv2.COLOR_HSV2RGB)
cv2.imshow('HSV to RGB',RGB_image )
BGR_image = cv2.cvtColor(house_HSV_image, cv2.COLOR_HSV2BGR)
cv2.imshow('HSV to BGR',BGR_image)
cv2.waitKey(0)
cv2.destroyAllwindows()

# iii)Convert RGB and BGR to YCrCb

import cv2
houseImage = cv2.imread('house.jpeg')
cv2.imshow('Original HSV Image',houseImage)
YCrCb_image = cv2.cvtColor(houseImage, cv2.COLOR_RGB2YCrCb)
cv2.imshow('BGR2HSV',YCrCb_image)
YCrCb_image1 = cv2.cvtColor(houseImage, cv2.COLOR_BGR2YCrCb)
cv2.imshow('RGB2HSV',YCrCb_image1)
cv2.waitKey(0)
cv2.destroyAllWindows()

# iv)Split and Merge RGB Image

import cv2
image = cv2.imread('house.jpeg')
blue = image[:,:,0]
green = image[:,:,1]
red = image[:,:,2]
cv2.imshow('B-Channel',blue)
cv2.imshow('G-Channel',green)
cv2.imshow('R-Channel',red)
mergeBgr = cv2.merge((blue,green,red))
cv2.imshow('Merged BGR image',mergeBgr)
cv2.waitKey(0)
cv2.destroyAllWindows()

# v) Split and merge HSV Image

import cv2
image = cv2.imread('house.jpeg')
hsv = cv2.cvtColor(image,cv2.COLOR_BGR2HSV)
h,s,v = cv2.split(hsv)
cv2.imshow('Hue - Image',h)
cv2.imshow('Saturation - Image',s)
cv2.imshow('Gray - Image',v)
mergedHSV = cv2.merge((h,s,v))
cv2.imshow('Merged HSV Image',mergedHSV)
cv2.waitKey(0)
cv2.destroyAllWindows()

```
## Output:
### i) BGR and RGB to HSV and GRAY
<br>
<img width="1440" alt="1A" src="https://user-images.githubusercontent.com/93427011/162411303-60806ec5-064f-4299-8dfc-0056498077d3.png">
<br>

### ii) HSV to RGB and BGR
<br>
<img width="1440" alt="1B" src="https://user-images.githubusercontent.com/93427011/162411334-e895e52c-7dd8-4b95-9fb1-dfde14d28175.png">
<br>

### iii) RGB and BGR to YCrCb
<br>
<img width="1440" alt="1C" src="https://user-images.githubusercontent.com/93427011/162411351-0e3ab47e-7f6e-4e79-b3aa-3102ac38c5f1.png">
<br>

### iv) Split and merge RGB Image
<br>
<img width="1440" alt="1D" src="https://user-images.githubusercontent.com/93427011/162411387-4e19de9a-3d82-4ea4-b25c-d3e7a7b3d39e.png">
<br>

### v) Split and merge HSV Image
<br>
<img width="1440" alt="1E" src="https://user-images.githubusercontent.com/93427011/162411412-54df8059-b666-4387-8519-4d7265d4941e.png">
<br>


## Result:
Thus the color conversion was performed between RGB, HSV and YCbCr color models.
