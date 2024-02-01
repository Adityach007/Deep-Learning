# 1. Class Definition (MyDense):

  - The class **'MyDense'** is defined, which is a custom layer class extending tf.keras.layers.Layer.

  - It takes units as a required parameter, representing the number of neurons in the layer.

  - The activation parameter is optional and specifies the activation function to be used. If not provided, it defaults to None.

  - The **kwargs parameter allows additional keyword arguments to be passed to the base class constructor.

# 2. Initialization (__init__ method):

  - The **__init__** method initializes the layer.

  - It calls the constructor of the base class **(super()**.__init__(**kwargs))** to properly initialize the layer.

  - **self.units** is set to the provided units parameter, representing the number of neurons in the layer.

  - **self.activation** is set to the activation function specified in the activation parameter. If activation is not provided, it defaults to None.

Note: tf.keras.activations.get(activation) is used to obtain the activation function. If activation is a string (e.g., "relu"), it retrieves the corresponding activation function. If it's already a function, it uses it as is.

# 3. Building the Layer (build method):

  - The build method is called when the layer is first used and is responsible for creating the layer's weights.

  - It receives the batch_input_shape, which is the shape of the input tensor.

  - **self.add_weight** is used to create trainable weights for the layer:

  - **self.kernel** represents the weight matrix with shape **[input_size, units]** and is initialized using the "glorot_normal" initializer.
self.bias represents the bias vector with shape [units] and is initialized with zeros.

# 4. Forward Pass (call method):

  - The call method defines the forward pass of the layer.

  - It computes the output by applying the activation function to the linear transformation **'x @ self.kernel + self.bias'**, where x is the input tensor.

# 5. Configuration for Serialization (base_config method):

  - The **'base_config'** method returns a dictionary containing the configuration needed to recreate the layer.

  - It calls the **'get_config'** method of the base class (super().get_config()) to obtain the base configuration.

  - It adds custom configuration entries for the **'units'** and **'serialized activation'** function to the base configuration.
