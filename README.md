# GradCam
A technique for making Convolution Neural Network (CNN)-based models more transparent by visualizing the regions of input that are "important" for predictions from these models - or visual explanations and the approach called Gradient-weighted Class Activation Mapping (Grad-CAM), uses the class-specific gradient information flowing into the final convolution layer of a CNN to produce a coarse localization map of the important regions in the image.

visualize class activation maps for debugging deep neural networks using an algorithm called Grad-CAM. We will then implement Grad-CAM using Keras and TensorFlow.

While deep learning has facilitated unprecedented accuracy in image classification, object detection, and image segmentation, one of their biggest problems is model interpretability, a core component in model understanding and model debugging.

In practice, deep learning models are treated as “black box” methods, and many times we have no reasonable idea as to:

Where the network is “looking” in the input image
Which series of neurons activated in the forward-pass during inference/prediction
How the network arrived at its final output
That raises an interesting question — how can you trust the decisions of a model if you cannot properly validate how it arrived there?

To help deep learning practitioners visually debug their models and properly understand where it’s “looking” in an image, Gradient-weighted Class Activation Mapping, or more simply, Grad-CAM is used:

Grad-CAM uses the gradients of any target concept (say logits for “dog” or even a caption), flowing into the final convolutional layer to produce a coarse localization map highlighting the important regions in the image for predicting the concept.”

Using Grad-CAM, we can visually validate where our network is looking, verifying that it is indeed looking at the correct patterns in the image and activating around those patterns.

If the network is not activating around the proper patterns/objects in the image, then we know:
Our network has not properly learned the underlying patterns in our dataset
Our training procedure needs to be revisited
We may need to collect additional data
And most importantly, our model is not ready for deployment.
Grad-CAM is a tool that should be in any deep learning practitioner’s toolbox — take the time to learn how to apply it now.
Grad-CAM provides the importance of debugging and visually verifying that your convolutional neural network is “looking” at the right places in an image.
From there, we’ll dive into Grad-CAM, an algorithm that can be used visualize the class activation maps of a Convolutional Neural Network (CNN), thereby allowing you to verify that your network is “looking” and “activating” at the correct locations.

We will then implement Grad-CAM using Keras and TensorFlow.


This method is:
Easily implemented
Works with nearly any Convolutional Neural Network architecture
Can be used to visually debug where a network is looking in an image
Grad-CAM works by (1) finding the final convolutional layer in the network and then (2) examining the gradient information flowing into that layer.

The output of Grad-CAM is a heatmap visualization for a given class label (either the top, predicted label or an arbitrary label we select for debugging). We can use this heatmap to visually verify where in the image the CNN is looking.




