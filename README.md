# Color Conversion
## AIM
To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.

## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:
```
Read an image using imread() and Convert BGR and RGB to HSV and GRAY
using:
cv2.cvtColor(image,cv2.COLOR_RGB2HSV)
cv2.cvtColor(image,cv2.COLOR_RGB2GRAY)
cv2.cvtColor(image,cv2.COLOR_BGR2HSV)
cv2.cvtColor(image,cv2.COLOR_BGR2GRAY)
```
### Step2:
```
Convert HSV to RGB and BGR
using:
cv2.cvtColor(image,cv2.COLOR_HSV2RGB)
cv2.cvtColor(image,cv2.COLOR_HSV2BGR)
```
### Step3:
```
Convert RGB and BGR to YCrCb
using:
cv2.cvtColor(image,cv2.COLOR_RGB2YCrCb)
cv2.cvtColor(image,cv2.COLOR_BGR2YCrCb)
```
### Step4:
```
Split and Merge RGB Image
using:
blue = image[:,:,0]
green = image[:,:,1]
red = image[:,:,2]
cv2.merge((blue,green,red))
```
### Step5:
```
Split and merge HSV Image
using:
hsv=cv2.cvtColor(image,cv2.COLOR_BGR2HSV)
h, s, v = cv2.split(hsv)
cv2.merge((h,s,v))
```
## Program:

# Developed By: S.SAFA
# Register Number: 212220230040
# i) Convert BGR and RGB to HSV and GRAY
```
import cv2
image=cv2.imread("pic.jpeg")
cv2.imshow("212220230040",image)
BGR_HSV=cv2.cvtColor(image,cv2.COLOR_BGR2HSV)
cv2.imshow("BGR to HSV image",BGR_HSV)
BGR_GRAY=cv2.cvtColor(image,cv2.COLOR_BGR2GRAY)
cv2.imshow("BGR to GRAY image",BGR_GRAY)
RGB_HSV=cv2.cvtColor(image,cv2.COLOR_RGB2HSV)
cv2.imshow("RGB to HSV image",RGB_HSV)
RGB_GRAY=cv2.cvtColor(image,cv2.COLOR_RGB2GRAY)
cv2.imshow("RGB to GRAY image",RGB_GRAY)
cv2.imshow("picz",image)
cv2.waitKey(0)
cv2.destroyAllWindows()


```
# ii)Convert HSV to RGB and BGR
```
hsv=cv2.cvtColor(image,cv2.COLOR_BGR2HSV)
cv2.imshow("HSV image",hsv)
HSV_RGB=cv2.cvtColor(image,cv2.COLOR_HSV2RGB)
cv2.imshow("HSV to RGB image",HSV_RGB)
HSV_BGR=cv2.cvtColor(image,cv2.COLOR_HSV2BGR)
cv2.imshow("HSV to BGR image",HSV_BGR)
cv2.waitKey(0)
cv2.destroyAllWindows()


```
# iii)Convert RGB and BGR to YCrCb
```
RGB_YCrCb=cv2.cvtColor(image,cv2.COLOR_RGB2YCrCb)
cv2.imshow("RGB to YCrCb image",RGB_YCrCb)
BGR_YCrCb=cv2.cvtColor(image,cv2.COLOR_BGR2YCrCb)
cv2.imshow("BGR to YCrCb image",BGR_YCrCb)
cv2.imshow("picz",image)
cv2.waitKey(0)
cv2.destroyAllWindows()

```
# iv)Split and Merge RGB Image
```
blue = image[:,:,0]
cv2.imshow("Blue Split",blue)
green = image[:,:,1]
cv2.imshow("Green Split",green)
red = image[:,:,2]
cv2.imshow("Red Split",red)
merged=cv2.merge((blue,green,red))
cv2.imshow("Merged Image",merged)
cv2.imshow("new pic",image)
cv2.waitKey(0)
cv2.destroyAllWindows()


```
# v) Split and merge HSV Image
```
hsv=cv2.cvtColor(image,cv2.COLOR_BGR2HSV)
h, s, v = cv2.split(hsv)
cv2.imshow('h_plane', h)
cv2.imshow('s_plane', s)
cv2.imshow('v_plane', v)
mergedhsv=cv2.merge((h,s,v))
cv2.imshow("HSV image",hsv)
cv2.imshow('Merged HSV',mergedhsv)
cv2.waitKey(0)
cv2.destroyAllWindows()



```
## Output:
### i) BGR and RGB to HSV and GRAY
![1a](https://user-images.githubusercontent.com/75234912/163564162-e932c31a-5868-4d82-b160-58742b1d7bf6.png)
![1b](https://user-images.githubusercontent.com/75234912/163564173-e9a0882a-dac8-45f4-8dc9-e036d84a786c.png)
![1c](https://user-images.githubusercontent.com/75234912/163564190-c73a6f2b-2330-44fd-81f6-5333ccd9443f.png)


### ii) HSV to RGB and BGR
![2](https://user-images.githubusercontent.com/75234912/163564203-dcc5b903-dd5d-4347-b526-f104549a4f7d.png)


### iii) RGB and BGR to YCrCb
![3](https://user-images.githubusercontent.com/75234912/163564212-ec9a6acc-086a-4b0a-bd5e-7c350262455c.png)


### iv) Split and merge RGB Image
![4a](https://user-images.githubusercontent.com/75234912/163564240-b74b46c4-eb93-4c90-9bc6-71241ec574be.png)
![4b](https://user-images.githubusercontent.com/75234912/163564247-25a4efc2-e00f-4408-a424-13b8dfed7f1f.png)


### v) Split and merge HSV Image
![5a](https://user-images.githubusercontent.com/75234912/163564255-14eed5d7-1a17-404a-beae-6047ecdbe9d3.png)
![5b](https://user-images.githubusercontent.com/75234912/163564269-9fcfa51f-d5e9-456e-a9c4-88dbadc6bcff.png)



## Result:
Thus the color conversion was performed between RGB, HSV and YCbCr color models.
