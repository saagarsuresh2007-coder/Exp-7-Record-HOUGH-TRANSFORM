#  Lane Detection

##  Aim

To implement a basic lane detection pipeline using OpenCV by completing missing code segments at specified locations.

---

## Learning Objective

* Understand each stage of image processing
* Learn how to build a complete computer vision pipeline
* Practice writing code in guided sections

##  Software Used

* Anaconda – Python 3.7
* Jupyter Notebook / VS Code
* OpenCV (cv2)
* NumPy
* Matplotlib

---

##  Algorithm & Explanation

---

###  Step 1: Import Libraries

```python
import cv2
import numpy as np
import matplotlib.pyplot as plt
```

---

###  Step 2: Read the Image

```python
# Read the image using OpenCV

img = cv2.imread("apple.jpeg")
img = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
```

---

###  Step 3: Convert to Grayscale

```python
# Convert to grayscale.

gray = cv2.cvtColor(img, cv2.COLOR_BGR2GRAY)
```

---

###  Step 4: Display Images

```python
plt.figure(figsize=(10,5))

plt.subplot(1,2,1); plt.imshow(img); plt.title('Input Image')
plt.subplot(1,2,2); plt.imshow(gray, cmap='gray'); plt.title('Grayscale')
```

---

###  Step 5: Thresholding

```python
# Apply thresholding

threshold = 127
_, threshold = cv2.threshold(gray, threshold, 255, cv2.THRESH_BINARY)
```

---

###  Step 6: Region of Interest (ROI)

```python
# ROI masking already provided
# (Do not modify)
```

---

### Step 7: Edge Detection (Canny)

```python
# Perform Edge Detection

edges = cv2.Canny(gray, 100, 200)
```

---

###  Step 8: Gaussian Blur

```python
# Apply Gaussian Blur

blurred = cv2.GaussianBlur(gray, (5, 5), 0)
```

---

###  Step 9: Hough Transform

```python
# Detect lines using Hough Transform

rho = 1
theta = np.pi / 180
threshold = 100
minLineLength = 50
maxLineGap = 10

lines = cv2.HoughLinesP(edges, rho, theta, threshold,
                        minLineLength=minLineLength,
                        maxLineGap=maxLineGap)
```

---

### Step 10: Lane Detection Logic

```python
# Already implemented
# (Do not modify)
```

---

##  Expected Output

![alt text](<Screenshot 2026-08-20 152320.png>) ![alt text](<Screenshot 2026-08-20 152309.png>) ![alt text](<Screenshot 2026-08-20 152304.png>) ![alt text](<Screenshot 2026-08-20 152258.png>) ![alt text](<Screenshot 2026-08-20 152252.png>) ![alt text](<Screenshot 2026-08-20 152244.png>) ![alt text](<Screenshot 2026-08-20 152236.png>) ![alt text](<Screenshot 2026-08-20 152231.png>) ![alt text](<Screenshot 2026-08-20 152225.png>) ![alt text](<Screenshot 2026-08-20 152221.png>)



## Result

Thus, the lane detection pipeline is successfully implemented by completing the missing code sections. The system detects and highlights lane lines effectively.



##  Developed By

* **Name:** SAAGAR S
* **Register No:** 212225040351
