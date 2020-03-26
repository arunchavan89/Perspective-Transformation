# Perspective-Transformation
Undistort and transform to Perspective view

[//]: # (Image References)

[image1]: ./result.png "Grayscale"
![alt text][image1]

The goal is to generate output like the image shown above. To do that, write a function that takes your distorted image as input and completes the following steps:

* Undistort the image using cv2.undistort() with mtx and dist
* Convert to grayscale
* Find the chessboard corners
* Draw corners
* Define 4 source points (the outer 4 corners detected in the chessboard pattern)
* Define 4 destination points (must be listed in the same order as src points!)
* Use cv2.getPerspectiveTransform() to get M, the transform matrix
* use cv2.warpPerspective() to apply M and warp your image to a top-down view
