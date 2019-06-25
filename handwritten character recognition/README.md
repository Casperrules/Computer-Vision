# Handwritten charecter recognition:

### the deep learning part:
We create a convolutional neural network in matlab and train the network over a self compiled dataset using the MNIST dataset for digits and a kaggle dataset for the alphabets. We use a python script to convert teh dataset in csv to an image format.
The images are stored in labled folders. 
We use imageDatastore function in matlab to load the images and lable them according to the folder number.
We create a CNN in matlab for reading and classifying the input images to the 36 classes(digits+alphabets).
we use 90% of the data to train the network and 10% data to evaluate the network. 

I got a 94% accuracy of the above trained network
### The image processing part:
In the current program I use an image from my phone but we can scale the codes to load the images from a webcam and even a video.
We convert the image to grayscale(rgb2gray function), and binarize it. We use the regionprop function to get the information of the region area and 
the dimensions of the bounding box.
We crop the image for the bounding box to segment the charaters in the string.

### The final implimentation:
We pass the croped images to the network and print out the most probable class for the image
We store the images temperorily in a temp folder in a .jpg format. The network needs to be fed images of the same format.
