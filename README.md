# EXP-8-image-thresholding-opencv
Image Segmentation Using Thresholding Techniques in OpenCV
Aim
To segment an image using Global Thresholding, Adaptive Thresholding, and Otsu's Thresholding techniques using Python and OpenCV.

The program performs the following operations:

Global Thresholding
Adaptive Thresholding
Otsu's Thresholding
Software Used
Anaconda – Python 3.7
Jupyter Notebook / VS Code
OpenCV (cv2)
NumPy
Matplotlib
Algorithm
Step 1:
Import the required libraries: OpenCV, NumPy, and Matplotlib.

Step 2:
Load the input image using OpenCV.

Step 3:
Convert the input image into grayscale format.

Step 4: Global Thresholding
Select a fixed threshold value.
Apply thresholding to separate foreground and background pixels.
Display the thresholded image.
Step 5: Adaptive Thresholding
Compute threshold values for small regions of the image.
Apply Adaptive Mean Thresholding.
Apply Adaptive Gaussian Thresholding.
Display the segmented images.
Step 6: Otsu's Thresholding
Automatically determine the optimal threshold value.
Apply Otsu's thresholding technique.
Display the segmented image.
Step 7:
Compare the results obtained from Global, Adaptive, and Otsu's thresholding methods.

## Program
## Developed By
## Name: SARAVANAN K
## Register No: 212224230146
```
import cv2
import matplotlib.pyplot as plt
img = cv2.imread("surya.jpg")
plt.imshow(cv2.cvtColor(img, cv2.COLOR_BGR2RGB))
plt.title("Original Image")
plt.axis("off")
plt.show()

import cv2
import matplotlib.pyplot as plt
img = cv2.imread("surya.jpg", cv2.IMREAD_GRAYSCALE)
plt.imshow(img, cmap="gray")
plt.title("Original Grayscale Image")
plt.axis("off")
plt.show()

import cv2
import matplotlib.pyplot as plt
img = cv2.imread("surya.jpg", cv2.IMREAD_GRAYSCALE)
_, result = cv2.threshold(img, 127, 255, cv2.THRESH_BINARY)
plt.imshow(result, cmap="gray")
plt.title("Global Thresholding")
plt.axis("off")
plt.show()

import cv2
import matplotlib.pyplot as plt
img = cv2.imread("surya.jpg", cv2.IMREAD_GRAYSCALE)
result = cv2.adaptiveThreshold(
    img, 255,
    cv2.ADAPTIVE_THRESH_GAUSSIAN_C,
    cv2.THRESH_BINARY,
    11, 2
)
plt.imshow(result, cmap="gray")
plt.title("Adaptive Thresholding")
plt.axis("off")
plt.show()

import cv2
import matplotlib.pyplot as plt
img = cv2.imread("surya.jpg", cv2.IMREAD_GRAYSCALE)
_, result = cv2.threshold(
    img, 0, 255,
    cv2.THRESH_BINARY + cv2.THRESH_OTSU
)
plt.imshow(result, cmap="gray")
plt.title("Otsu's Thresholding")
plt.axis("off")
plt.show()

```

## Output

<img width="674" height="410" alt="image" src="https://github.com/user-attachments/assets/ab71d99e-7e3f-4a8a-82fa-31b1ee10b5cd" />
<img width="649" height="421" alt="image" src="https://github.com/user-attachments/assets/2704f1fb-5786-4a72-b027-cd51ec51295f" />
<img width="667" height="416" alt="image" src="https://github.com/user-attachments/assets/a138da7a-1eb5-45e5-aca8-379579be014b" />
<img width="659" height="417" alt="image" src="https://github.com/user-attachments/assets/3657b18d-d4b4-4149-9532-64b189ee9c08" />
<img width="644" height="418" alt="image" src="https://github.com/user-attachments/assets/c6039db3-1707-45d8-ad45-24d48bf6903c" />

## Result
Thus, image segmentation is successfully performed using Global Thresholding, Adaptive Thresholding, and Otsu's Thresholding techniques in OpenCV.
