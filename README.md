# Posenet-Posture-Correction

This is a project that can give advice regarding sitting postures in real time. For the folks who are virtually planted at their desks, this project can help us develop healthier sitting habits that positively impact our health. 

<a href="https://imgur.com/LdzQpqF"><img src="https://i.imgur.com/LdzQpqF.jpg" title="source: imgur.com" /></a>
(example of result)

## The Algorithm

This project requires two networks from Nvidia's Jetson Nano, posenet and imagenet. Feedback from the program are generated from classification. Imagenet will be retrained on a set of images and will learn to distinguish a good seating posture from a bad seating posture. Before the data gets to imagenet for classification, however, posenet will helpfully annotate data images and identify the subjects' skeletal positions.

## Running this project

Let's get started!

### Making the Dataset

A very basic working dataset is given to you. Though it works, having a larger dataset would be much better for accuracy. If you wish to retrain resnet-18 on a bigger dataset, feel free to follow these steps.

In a convenient spot on your host machine, amass as many pictures as you can of different seating postures. I used the following conventions for my pictures but if you can do something different:

1. One person per subject seated on a chair.
2. Only the left profile view is shown.
3. Head, shoulder, knees, and toes are all showm and preferably not covered.
4. The background is relative plain and empty.

Name your dataset something useful and create three directories within it: test, train, and val. Within each of the three, add two more directories: good and bad. Now, split your images however you want. I recommend test and train having a 25%/75% ratio. For convenience, sequentially label the images in each sub-directory. Finally, in the directory of test, train, and val, add a "labels.txt" and write "good" and "bad" in two lines. 

After creating the dataset on your local computer, zip the file and send it to your Jetson Nano via this command:

### Annotating the Dataset with Posenet

On your Jetson Nano, go to the ~/jsdfjsldfkj . You should see the zip file there.

Unzip the zip file and you should get a replica of your dataset on your host machine.

Just to double check that posenet did its job correctly, scp your dataset back to your host machine and double check if your images are nicely annotated. Your images should look something like this




### The Program

1. Make sure your Jetson Nano board is set up and ready to operate in headless mode. For further instructions, visit Nvidia's helpful Github page:
2. ssh into your nano with ssh <username>@<IP Address> and password
3. Next, create a project directory and name it something useful <d

[View a video explanation here](video link)
