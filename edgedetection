import cv2
import matplotlib.pyplot as plt

image = cv2.imread("image.jpg")
image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
images = [None] * 5
names = ['gradients_sobelx', 'gradients_sobely', 'gradients_sobelxy', 'gradients_lapacian', 'canny_output']

gradients_sobelx = cv2.Sobel(image, -1, 1, 0)
gradients_sobely = cv2.Sobel(image, -1, 0, 1)
gradients_sobelxy = cv2.addWeighted(gradients_sobelx, 0.5, gradients_sobely, 0.5, 0)
gradients_lapacian = cv2.Laplacian(image, -1)
canny_output = cv2.Canny(image, 8, 150)
images[0] = gradients_sobelx
images[1] = gradients_sobely
images[2] = gradients_sobelxy
images[3] = gradients_lapacian
images[4] = canny_output

cv2.imshow('gradients_sobelx', images[0])
cv2.imshow('gradients_sobely', images[1])
cv2.imshow('gradients_sobelxy', images[2])
cv2.imshow('gradients_lapacian', images[3])
cv2.imshow('edgedetection', canny_output)

cv2.waitKey()
