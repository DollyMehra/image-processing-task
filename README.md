# image-processing-task
📌 Create image by yourself Using Python Code

import cv2 , numpy , matplotlib.pyplot as plt
import cv2 , numpy , matplotlib.pyplot as plt
circleshape = numpy.zeros((250,400,3))
circleshape.shape
cv2.circle(circleshape,center=(100,75),radius=75,color=(10,20,30),thickness=-2)
cv2.imshow('CIRCLE',circleshape)
cv2.waitKey()
cv2.destroyAllWindows()
📌 Take 2 image crop some part of both image and swap it.

#showing micky image in graph form , then it will be easy to crop the image in next step
micky = cv2.imread("micky.jpg")
plt.imshow(micky)
#cropping a mickyimage
croppedmickyimage = micky[10:200 , 180:400]
plt.title("mickymouse")
plt.imshow(croppedmickyimage)
#showing boy image
boy = cv2.imread("boy.jpg")
plt.imshow(boy)
​
#cropping a boy image
croppedboyimage = boy[10:200 , 180:400]
plt.title("cooLboy")
plt.imshow(croppedboyimage)
​
#swapping boy cropped image with actual image of micky
micky = cv2.imread("micky.jpg")
micky[10:200 , 180:400] = croppedboyimage
cv2.imshow("x" , micky)
cv2.waitKey()
cv2.destroyAllWindows()
​
#swapping micky cropped image with actual image of boy
boy = cv2.imread("boy.jpg")
boy[10:200 , 180:400] = croppedmickyimage
cv2.imshow("y" , boy)
cv2.waitKey()
cv2.destroyAllWindows()
​
📌 Take 2 image and combine it to form single image. For example collage

#combine two images just like a collage
pic_a = cv2.imread("micky.jpg")
pic_b = cv2.imread("boy.jpg")
ab = numpy.hstack((pic_a ,pic_b))
cv2.imshow("collage",ab)
cv2.waitKey()
cv2.destroyAllWindows()
​
