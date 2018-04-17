from skimage import io,data
import numpy as np
img = io.imread('image.jpg')
rows,cols,dims = img.shape
row2 = int(rows/2)
col2 = int(cols/2)
img2 = img
for i in range(0,row2):
    for j in range(0,cols):
        for k in range(0,3):
            img2[i,j,k] = img[i,j,k] 
            for i in range(row2,rows):
    for j in range(0,cols):
        for k in range(0,3):
            img2[i,j,k] = img[row2+(-1)*(i-row2),j,k]
            io.imshow(img2)
            io.show()
            from PIL import Image
            im = Image.open('image.jpg')
            imL = im.convert('L')
            imL.save('gray.jpg')
            imL.show()
