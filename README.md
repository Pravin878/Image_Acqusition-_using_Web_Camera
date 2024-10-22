
# Image Acqusition using Web Camera
## Aim
To write a python program using OpenCV to capture the image from the web camera and do the following image manipulations.
i) Write the frame as JPG 
ii) Display the video 
iii) Display the video by resizing the window
iv) Rotate and display the video

## Software Used
Anaconda - Python 3.7
## Algorithm
### Step 1:
Use cv2.VideoCapture(0) to access web camera

### Step 2:
Use cv2.imread to read the video or image

### Step 3:
Use cv2.imwrite to save the image

### Step 4:
Use cv2.imshow to show the video

### Step 5:
End the program and close the output video window by pressing 'q'.

## Program:
```
 Developed By: pravin kumar G
 Register No: 212222230109
```
## i) Write the frame as JPG file
```
import cv2
viedoCaptureObject=cv2.VideoCapture(0)
while(True):
    ret,frame=viedoCaptureObject.read()
    cv2.imwrite("Archana.jpg",frame)
    result=False
viedoCaptureObject.release()
cv2.destroyAllWindows()
```


## ii) Display the video

```
import numpy as np
import cv2
cap=cv2.VideoCapture(0)
while True:
    ret,frame=cap.read()
    cv2.imshow('flower',frame)
    if cv2.waitKey(1)==ord('q'):
        break
cap.release()
cv2.destroyAllWindows()
```
## iii) Display the video by resizing the window
```
import numpy as np
import cv2
cap=cv2.VideoCapture(0)
while True:
    ret,frame=cap.read()
    width=int(cap.get(3))
    height=int(cap.get(4))
    image=np.zeros(frame.shape,np.uint8)
    smaller_frame=cv2.resize(frame,(0,0),fx=0.5,fy=0.5)
    image[:height//2, :width//2]=smaller_frame
    image[height//2:, :width//2]=smaller_frame
    image[:height//2, width//2:]=smaller_frame
    image[height//2:, width//2:]=smaller_frame
    cv2.imshow('212222240011_Archana',image)
    if cv2.waitKey(1)==ord('q'):
        break
cap.release()
cv2.destroyAllWindows()
```



## iv) Rotate and display the video
```
import numpy as np
import cv2
cap=cv2.VideoCapture(0)
while True:
    ret,frame=cap.read()
    width=int(cap.get(3))
    height=int(cap.get(4))
    image=np.zeros(frame.shape,np.uint8)
    smaller_frame=cv2.resize(frame,(0,0),fx=0.5,fy=0.5)
    image[:height//2, :width//2]=cv2.rotate(smaller_frame,cv2.ROTATE_180)
    image[height//2:, :width//2]=smaller_frame
    image[:height//2, width//2:]=cv2.rotate(smaller_frame,cv2.ROTATE_180)
    image[height//2:, width//2:]=smaller_frame
    cv2.imshow('212222240011_Archana',image)
    if cv2.waitKey(1)==ord('q'):
        break
cap.release()
cv2.destroyAllWindows()
```







## Output

### i) Write the frame as JPG image
![(https://github.com/mohan8900/Image_Acqusition-_using_Web_Camera/blob/main/306834696-5c319921-b55e-4ec5-a6f2-f2294b0a8e72.png)](https://github.com/mohan8900/Image_Acqusition-_using_Web_Camera/blob/main/306834696-5c319921-b55e-4ec5-a6f2-f2294b0a8e72.png)

### ii) Display the video
![Screenshot 2024-02-21 213311](https://github.com/Jaiganesh235/Image_Acqusition-_using_Web_Camera/assets/118657189/d29f2b17-edf9-4bbe-906e-b6e5a9424d12)



### iii) Display the video by resizing the window

![Screenshot 2024-02-21 213416](https://github.com/Jaiganesh235/Image_Acqusition-_using_Web_Camera/assets/118657189/49686dd1-a328-4909-a5f1-ddf0567ecff6)

### iv) Rotate and display the video


![Screenshot 2024-02-21 213518](https://github.com/Jaiganesh235/Image_Acqusition-_using_Web_Camera/assets/118657189/2fe12628-6724-41d5-9e06-15bbfa8eacb2)



## Result:
Thus the image is accessed from webcamera and displayed using openCV
