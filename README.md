# EXP-2-Image-Capture-and-Video-Processing-Using-OpenCV

# Aim:

   To write a Python program using OpenCV to capture an image from the webcam and perform the following operations:

 Write the frame as a JPG file
 Display the video
 Display the video by resizing the window
 Rotate and display the video

 
# 🛠️ Software Used
  Anaconda – Python 3.7
  Jupyter Notebook / VS Code
  OpenCV (cv2)
  
# ⚙️ Algorithm:

Step 1:
Import the required libraries and initialize the webcam using cv2.VideoCapture().

Step 2:
Capture frames continuously from the webcam.

Step 3:import cv2
import matplotlib.pyplot as plt
from IPython.display import clear_output
import time



cap = cv2.VideoCapture(0)
ret, frame = cap.read()
if ret:
    cv2.imwrite("captured_frame.jpg", frame)
cap.release()



captured_image = cv2.imread('captured_frame.jpg')



plt.imshow(captured_image[:,:,::-1])
plt.title('Captured Frame')
plt.axis('off')
plt.show()




cap = cv2.VideoCapture(0)



for i in range(50):
    ret, frame = cap.read()
    if not ret:
        break
    frame_rgb = cv2.cvtColor(frame, cv2.COLOR_BGR2RGB)
    clear_output(wait=True)
    plt.imshow(frame_rgb)
    plt.axis('off')
    plt.show()
    time.sleep(0.05)

cap.release()

cap = cv2.VideoCapture(0)

for i in range(50):
    ret, frame = cap.read()
    if not ret:
        break
    resized_frame = cv2.resize(frame, (100, 150))  # Resize to 320x240
    frame_rgb = cv2.cvtColor(resized_frame, cv2.COLOR_BGR2RGB)
    clear_output(wait=True)
    plt.imshow(frame_rgb)
    plt.axis('off')
    plt.show()
    time.sleep(0.05)

cap.release()


cap = cv2.VideoCapture(0)

for i in range(50):
    ret, frame = cap.read()
    if not ret:
        break
    rotated_frame = cv2.rotate(frame, cv2.ROTATE_90_CLOCKWISE)
    frame_rgb = cv2.cvtColor(rotated_frame, cv2.COLOR_BGR2RGB)
    clear_output(wait=True)
    plt.imshow(frame_rgb)
    plt.axis('off')
    plt.show()
    time.sleep(0.05)

cap.release()



```
```

# Output
i) Write the frame as JPG image:

# Captured image :
 <img width="617" height="500" alt="629791082-5863b7a2-fcd1-43e3-8564-d14d01a342ce" src="https://github.com/user-attachments/assets/25f29ad9-8b79-4366-9541-e99d937d1e94" />

i) Display the video:

# Live webcam video:


<img width="597" height="462" alt="629791640-463ed5d0-82bb-4812-8095-fdf6df3fee87" src="https://github.com/user-attachments/assets/a2e768c7-c549-489f-9ef0-ba4d7681f9ab" />



# iii) Display the video by resizing the window
# Video is shown in resized resolution:

<img width="307" height="452" alt="629791363-4f7d6996-299d-4384-97de-d1f2c974fcab" src="https://github.com/user-attachments/assets/bb47f5b5-7de5-427e-b729-c5dca8a6fd42" />



# iv) Rotate and display the video
# Video is displayed after rotation (90° clockwise):


<img width="235" height="465" alt="629791800-d5044451-e4aa-49c1-87b5-e9c036e68590" src="https://github.com/user-attachments/assets/33707f1e-aa40-48aa-9b96-a85ed27a4d78" />


# Result:

Thus, the image is successfully captured from the webcam and various video processing operations such as saving, displaying, resizing, and rotating are performed using OpenCV.












