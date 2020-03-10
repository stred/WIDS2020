# Neural network in Excel
## To provide an intuition as to how NNs work

The reality is that they are based on straightforward maths – just lots of it! The complexity comes, as with anything in life, when we have to do lots of maths.

At the core of a neural network is a neuron – which is just a maths function. It takes one or more input values, applies weights to the inputs, applies an activation function to the results of the weighting (often just a Sigmoid function) and then gives an output. Depending on where it sits in the network, the input might be coming from a source data set (maybe data from a customer database, or pixels from images of cats) or else the input comes from the previous layer of neurons. The output could go on to the next layer of neurons, or it could be the final output of the network.

The layers of neurons in the middle are called the hidden layer. We can have one or more hidden layers – the more we have, the deeper the network. Hence “deep learning”.

We train the network by putting through some known data and then comparing the error between the outputs and the expected values. The error is pushed back through the network to tweak all the weights (a method called backpropogation). This process is repeated with many training examples until we arrive at a good set of average weights for each neuron that give us the least amount of error on the output. Obviously, the more neurons and the deeper the layers, the longer this training process takes.

I mentioned above that the maths is actually quite straightforward. In fact, it is so straightforward that we can actually build a simple neural network using Excel! Here is a video showing how to do it:

   https://www.youtube.com/watch?v=8TWHUkVQVts

If you don’t have time to build it yourself, here’s one I prepared earlier: Neural Network in Excel.

To use it, copy the Randoms from S5:U14 into the weights values in N5:P14 (which will actually generate new random values). Now we use the Solver tool (you may need to add it in as an Excel Add-in) to minimise the value of the error calculated in $J$1 by adjusting the weights in $N$5:$P$5,$N$8:$P$8,$N$11:$O$11,$N$14:$P$14 using the GRG Nonlinear algorithm.

The Solver tool’s GRG function (Generalized Reduced Gradient) does the weight tweaking for us is actually very similar way to the function used my many neural networks, called Gradient Descent.
