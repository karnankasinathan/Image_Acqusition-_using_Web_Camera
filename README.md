# Image_Acqusition-_using_Web_Camera
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
``` Python
### Developed By:Karnan k
### Register No:212222230062
```
## i) Write the frame as JPG file
```
import cv2
cap = cv2.VideoCapture(0)
frame_number = 0 
while True:
    ret, frame = cap.read()
    cv2.imshow('frame', frame)
    cv2.imwrite(f"frame_{frame_number}.jpg", frame)
    frame_number += 1
    if cv2.waitKey(1) & 0xFF == ord('q'):
        break

cap.release()
cv2.destroyAllWindows()
```

## ii) Display the video
```
import cv2
cap = cv2.VideoCapture(0)
while True:
    ret, frame = cap.read()
    cv2.imshow('Video', frame)
    if cv2.waitKey(1) & 0xFF == ord('q'):
        break

cap.release()
cv2.destroyAllWindows()
```
## iii) Display the video by resizing the window
```
import cv2
cap = cv2.VideoCapture(0)
cv2.namedWindow('Video', cv2.WINDOW_NORMAL)
while True:
    ret, frame = cap.read()
    cv2.imshow('Video', frame)
    cv2.resizeWindow('Video', 100, 200)
    if cv2.waitKey(1) & 0xFF == ord('q'):
        break

cap.release()
cv2.destroyAllWindows()
```

## iv) Rotate and display the video

```
import cv2
cap = cv2.VideoCapture(0)
rotation_angle = 90
while True:
    ret, frame = cap.read()
    rotated_frame = cv2.rotate(frame, cv2.ROTATE_90_CLOCKWISE)
    cv2.imshow('Rotated Video', rotated_frame)
    if cv2.waitKey(1) & 0xFF == ord('q'):
        break
cap.release()
cv2.destroyAllWindows()
```
## Output

### i) Write the frame as JPG image

![e1](https://github.com/karnankasinathan/Image_Acqusition-_using_Web_Camera/assets/118787064/2046c924-6b3a-4db9-bb41-feea4e95dfcc)



### ii) Display the video

![e2](https://github.com/karnankasinathan/Image_Acqusition-_using_Web_Camera/assets/118787064/c81fb93c-90f7-48b8-abe6-3d27a51aeaa2)



### iii) Display the video by resizing the window

![e3](https://github.com/karnankasinathan/Image_Acqusition-_using_Web_Camera/assets/118787064/9d5c26ba-62a6-4baa-9028-9edebe9c4c24)


### iv) Rotate and display the video


![e4](https://github.com/karnankasinathan/Image_Acqusition-_using_Web_Camera/assets/118787064/5d27f5bc-e463-41a1-961e-d5b390263157)



## Result:
Thus the image is accessed from webcamera and displayed using openCV.
