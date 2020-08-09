# Auto-regressive-models
This repository contains code for training a type of generative model : auto regressive models, and it's variants such as PixelCNN and GatedPixelCNN architecture.<br/>
Vanilla PixelCNN is implemented in Tensorflow, meanwhile PyTorch is used to train GatedPixelCNN and PixelCNN with color dependecy masking mechanism.<br/>
Instead of MNIST for which this model performs exceptionally well, I have used a Stanford Dog dataset, which you can download from here: https://www.kaggle.com/c/generative-dog-images/data<br/><br/>

Thoughts on results:<br/>
1) Well, I am very disappointed by seeing generated images as I am expecting some Photo realistic Images as GANs, which I am gonna try.
The model wasn't generating any intelligible at all and but it is still better than random noise and model learn some statistics of shape and boundries of dog's body, which you can see in GatedPixelCNN's output.<br/>
2) I had tried increasing epochs and layers of residual block but it didn't work. The loss is fluctuating aroung 3.6.<br/>
3) I tried to generate 64 * 64 images but I trained on kaggle notebooks and I got Resource exhausted error on CUDA, tried reducing batch size
but still didn't work. So I generate 48 * 48 images. You can try to generate in original size if you have powerful machines.<br/>
4) The other thing to improve the result is preprocessing the dataset. There are only around 22k images and I have used only 16k images compared to massive datasets such as CIFAR 10 and CelebA. So Training data can be further increased using data augmentation methods.<br/><br/>

TODO : Try slightly advance and state of the art architecture such as PixelSNAIL and PixelCNN++.<br/>
Feel free to reach out to me at: jaydeept126@gmail.com for any feedback.<br/><br/>

Resources:<br/>
Apart from papers, these blogs helps me further to understand the masking and gating mechanism clearly.<br/>
http://sergeiturukin.com/2017/02/24/gated-pixelcnn.html<br/>
http://sergeiturukin.com/2017/02/22/pixelcnn.html<br/>
