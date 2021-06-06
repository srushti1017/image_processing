# Image_processing

# Hello guys !!! Today we will see how Create image by yourself Using Python Code.Then we will take 2 image and crop some part of both image and swap it, then we will combine them and form a single image.

# Let's Start...

So guys firstly we will see how to create our own image in open cv using python code . For that we need jupyter in our system after installing jupyter we have to install OpenCv  library. Here we also use some modules for image processing like numpy for implementing arrays and matplotlib for the visual understanding by drawing graphs.

    pip install Opencv-python
    pip install numpy 
    pip install matplotlib
    
Now see our 1st task that is to create image . For that we have to import cv2 library , numpy library and matplotlib library

    import cv2
    import numpy as np
    import matplotlib.pyplot as plt
    
Here we will  create 2 images for that  use following syntax :
     
    imge1 = cv2.imread('dog1.png')   
    imge2 = cv2.imread('dog2.png')
    
 Above we created two images now we will show these 2 images syntax for the same is as follow :
     
    #show 1st image 
    plt.title('original')
    plt.imshow(imge1)
   
    #show 2nd image
    plt.title('original1')
    plt.imshow(imge2)
    
Now we will swap these two images for that we will use for loop

    temp = np.zeros([600 , 800 , 3])
    for i in range (50 , 150 ):
        for j in range (50 , 170):
            temp[i , j ] = imge1[i , j]
            imge1[i , j] = imge2[i , j]
            imge2[i , j] = temp[i , j]
          
Now to show the images after swapping :

    #1st image after swapping
    plt.title('original')
    plt.imshow(imge1)
    
    #2nd image after swapping
    plt.title('original')
    plt.imshow(imge2)
    
After swapping we will see how to concatinate two images let's see !!!
For concatinating two images there are two ways 1st concatinate vertically and concatinate horizontally and for both operations there is a straight forward syntax is given in opencv library... These is for the same size images.
for vertically use keyword vconcat([img1_var , img1_var])
for horizontally use keyword hconcat([img1_var , img1_var])

    #concatinate two images vertically
    ver = cv2.vconcat([imge2, imge2])
    
    #show combined image
    cv2.imshow('combine1', ver)
    cv2.waitKey()
    cv2.DestroyAllWindows()

In this way we can create images , swapp the images also we can concatinate images.💯✌

# Thank you so much for reading and visiting my profile if you like then plz follow.🙌🙏

    
