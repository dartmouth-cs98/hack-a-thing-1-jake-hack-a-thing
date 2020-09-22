# Jake's Hack-a-thing

## Background

I wanted to learn more about pytorch. I'm fairly familar with tensorflow, but had never used pytorch before. So I completed a Pytorch tutorial I found online: https://pytorch.org/tutorials/beginner/deep_learning_60min_blitz.html
(the "60 minute blitz" is deceiving, this took me about 4 hours due to the copious amounts of notes and things I had to look up)

After learning, built my own model from scratch that took 7ish hours.

## Walk-through

The first section of my Hack-a-thing is dedicated to this tutorial - all the basic notes about how Pytorch and tensors work and then a basic CNN that classifies images as `classes = ('plane', 'car', 'bird', 'cat','deer', 'dog', 'frog', 'horse', 'ship', 'truck')`.

The second section is a multi-class classifier I built myself in pytorch. It classifies bonds using 6 features to 1 of 21 bond rating classes. I acheived an accuracy of 24% with very little hyper parameter tuning, but this may be because of the size of the dataset and the limited featureset. 23% is still well-above base-line accuracy so fairly satisfied with this outcome for a first Pytorch attempt.

## What I learned

How to use pytorch to perform machine learning. 1-hot encoding doesn't work here! That took me forever to figure out.

## What didn't work

I had trouble getting this to run on my GPU (1080ti). I think this is just because I'm using the same server as a 98 classmate, and he's doing some other machine learning stuff that perpetually fills up the GPU cache. Regardless, training on the CPU is slow and inefficient so for actual Pytorch projects will have to figure out how to resolve the CUDA exceptions that were being thrown.