## Notes on MLP
### Section 1: Basic Neural Network

<details>
  <summary>Loss Function :grin:</summary>
  
The goal of supervised learning is to minimize the loss function
  1. Regression: the Mean Square Error (MSE) and Mean Absolute Error (MAE)
  2. Binary classification: the Binary Cross Entropy (BCE)
  3. Multi-class Classification: Categorical Cross Entropy (CCE)
  ![Image](https://github.com/YixinFan11/Machine-Learning/blob/master/MLP/images/loss_fun_1.png?raw=true)
</details>

### Section 2:  Type of Neural Network
<details>
  <summary>Neural Network Structure</summary>

 ![Image](https://github.com/YixinFan11/Machine-Learning/blob/master/MLP/images/fun_1.png?raw=true)
 
  Φ is activation function and output a is activation. Common activation function:
  
 ![Image](https://github.com/YixinFan11/Machine-Learning/blob/master/MLP/images/act_fun.png?raw=true)
 ![Image](https://github.com/YixinFan11/Machine-Learning/blob/master/MLP/images/act_fun_tab.png?raw=true)


</details>

### Section 3:  Back Propagation

Back Propagation example on XOR and AND See Colab

Keras layers see: [Keras Layers API](https://keras.io/api/layers/).
Common layers: 
 - Core Layer: Dense layer(fully connected), Activation layer, Embedding layer, Masking layer, Lambda layer
 - Convolutional Layer
 - Pooling Layer: MaxPooling layer, AveragePooling layer, etc.
 - Reshaping Layer: Reshaping layer, Unsampling Layer, etc.

<details>
  <summary>Sequential Model</summary>
There are two ways to build Keras models: sequential and functional.

The sequential API allows you to create models layer-by-layer for most problems. It is limited in that it does not allow you to create models that share layers or have multiple inputs or outputs.

Alternatively, the functional API allows you to create models that have a lot more flexibility as you can easily define models where layers connect to more than just the previous and next layers. In fact, you can connect layers to (literally) any other layer. As a result, creating complex networks such as siamese networks and residual networks become possible.
</details>

### Section 4:  Optimisation

<details>
  <summary>Optimisation Technique</summary>
  
The goal of supervised learning is to minimize the loss function
 - Stochastic Gradient Descent 
 - Stochastic Gradient Descent with Momentum
 - RMSprop
 - ADAM
  



</details>

### Section 5:  Initialisation
If the gradients become small, training will proceed at a much slower rate and may not converge. This is called the **vanishing gradients problem**.
If the gradients become too large, the algorithm may diverge. This is called the  **exploding gradients problem**, and is mostly encountered in recurrent neural networks.

Xavier initialisation(Glorot initialisation)

Feature scaling, Normalisation(min-max, standardisation)

### Section 6:  Regularisation
**Regularisation** can be defined as any strategy designed to reduce **generalisation error**, but **not** impact on the **training error**. In deep learning an effective regulariser successfully balances the bias-variance trade off, that is it decreases the model variance responsible for over-fitting, while not overly increasing the bias.
<details>
  <summary>Early Stopping</summary>
  For large datasets, split into training, test and holdout sets(Holdout data is used to assess the final performance of the tuned model).
  Early stopping terminates the training process after the test loss has not improved over the previously recorded best test loss for a specified number of epochs
  </details>
  
 <details>
  <summary>L1/L2 regularisation</summary>
L1 and L2 regularisation are types of parameter-norm penalties, which can be implemented by adding a term to the cost function: J'(w) = J(w) + λΩ(w), where λ is hyperparameter determine the contribution of penalty term Ω(w)(kernel_regularizer in keras API)
  - L2 is also known as ridge-regression
  - L1 is also known as LASSO-regression
  </details>
  
  <details>
  <summary>Dropout</summary>
During training, every neuron (including the input neurons but excluding the output neurons) has a probability p of having its input and output weights set to zero. This reduces the chance of introducing spurious correlations that do not significantly contribute to improving the loss.
  </details>
  
  <details>
  <summary>Batch Normalisation</summary>
Batch normalisation is a method originally developed to reduce the vanishing/exploding gradients problem, but it has also been shown to have a regularising effect. It consists of adding an additional operation just before the activation function, that zero centers and normalises the inputs for each batch, then scales and shifts the results using two new learnable parameters. It can be added to individual layers in the network, each with separate learnable parameters, and is implemented in the TF2 keras API as a "BatchNormalization" layer.
  </details>
  
  <details>
  <summary>Data Augmentation</summary>
The best way to reduce over-fitting is to use more data.One can generate new training examples from existing ones by augmenting them. When using image data, for example, one could slightly shift, rotate, resize, crop, adjust the contrast, add small random noise etc, and this would force the model to be more tolerant to these properties and learn better representations of the data.
It is preferable to generate these new examples during training, rather than saving them to disk, and **TF2** offers several data augmentation methods
  </details>

