# MosaicCreator


## About
A simple algorithm to create a mosaic of images representing a main image.

![Alt text](out.png?raw=true "Title")

## Requirements
I used basic operations of **OpenCV** and **Numpy**.

## Usage
Go to the repo folder and run the *main.py* with the path of the main image as well as the directory of the source images photograph to process. You can also choose the output location and name.
```
$ python main.py ./Sources/All_images/IMG_3323-18_janvier_2017.jpg ./Sources/All_images/
```
Just feed the terminal with the number of images that you want along each axis and then wait for the process to run ! It will automatically save the image where you indicated or of not, where you are currently located when running the command line.

## Explanations
The algorithm is fairly simple :
- Reduce the dimensions of the main image to, let's say a 50x50 tiles grid. The aim of the algorithm is to fill this grid with indices of images so that the mosaic looks like the main image. The process is as follows:
- Reduce the size of the main image
- Load all possible images within the indicated directory (and reduce their size to a tile size).
- For each (i,j) in the tile grid, find the image (among let's say 30 random images within the list) that is, in average, the closest to the tile mean
- Fill the main image with the resized closest image 
As simple as that !

## Improvements possible
Some features could be added to this useful program :
- Limit the use of the same image
- Recognize faces in images so that all individuals appear approximately the same amount of time
