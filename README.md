# Keras-Basic
Basic implementation of keras and VGG like NN
Dataset not included due to size constraints

Please have a basic idea about argument parsing in python.


# Keras Learning rate decay scheduler.
It illustrates how reducing the learning rate over time improves our model.
Here it was tested on cifar-10 dataset using resnet architecture.



# Keras Cyclic Learning rate.
it tries to remove the cons of learning rate decay.
main idea : https://arxiv.org/abs/1506.01186

# Keras  Optimal Learning rate Finder
The automatic learning rate finder algorithm works like this:

Step #1: We start by defining an upper and lower bound on our learning rate. The lower bound should be very small (1e-10) and the upper bound should be very large (1e+1).
At 1e-10 the learning rate will be too small for our network to learn, while at 1e+1 the learning rate will be too large and our model will overfit.
Both of these are okay, and in fact, that’s what we hope to see!
Step #2: We then start training our network, starting at the lower bound.
After each batch update, we exponentially increase our learning rate.
We log the loss after each batch update as well.
Step #3: Training continues, and therefore the learning rate continues to increase until we hit our maximum learning rate value.
Typically, this entire training process/learning rate increase only takes 1-5 epochs.
Step #4: After training is complete we plot a smoothed loss over time, enabling us to see when the learning rate is both:
Just large enough for loss to decrease
And too large, to the point where loss starts to increase.

