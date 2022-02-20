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

### Section 6:  Regularisation

