### Week 3 Assignments: Neural Style Transfer

#### Assignment Overview
This week, you'll work on implementing and understanding the core components of neural style transfer using TensorFlow and VGG16. The tasks are designed to be of medium difficulty, striking a balance between guided steps and independent problem-solving. Follow the steps outlined below and complete the tasks within each section.

---

### Assignment 1: Setting Up the Environment

#### Task 1.1: Import Required Libraries
Import the necessary libraries to set up the project environment. Ensure you include:
- TensorFlow
- NumPy
- PIL (Python Imaging Library)
- Any specific modules from TensorFlow (e.g., VGG16)

#### Example Code Snippet:
```python
import tensorflow as tf
import numpy as np
from PIL import Image
from tensorflow.keras.applications.vgg16 import VGG16
```

#### Question:
Why do we need TensorFlow and a pre-trained model for neural style transfer?

---

### Assignment 2: Preprocessing Images

#### Task 2.1: Load and Resize Images
1. Download a content image and a style image.
2. Load the images using the `PIL.Image.open` method.
3. Resize the images to 224x224 pixels.
4. Ensure the resized images retain their aspect ratio as much as possible.

#### Example Code Snippet:
```python
# Replace 'path_to_content_image' and 'path_to_style_image' with actual file paths
content_image = Image.open('path_to_content_image').resize((224, 224))
style_image = Image.open('path_to_style_image').resize((224, 224))

# Display the images (optional)
content_image.show()
style_image.show()
```

#### Task 2.2: Convert Images to Tensors
1. Convert the loaded images to tensors using `tf.convert_to_tensor`.
2. Normalize the image values to be between 0 and 1.

#### Example Code Snippet:
```python
content_tensor = tf.convert_to_tensor(np.array(content_image), dtype=tf.float32) / 255.0
style_tensor = tf.convert_to_tensor(np.array(style_image), dtype=tf.float32) / 255.0
```

#### Question:
Why is normalization important in neural networks? 

---

### Assignment 3: Model Preparation

#### Task 3.1: Load Pre-trained VGG16 Model
1. Load the VGG16 model from `tensorflow.keras.applications`.
2. Use only the convolutional base (exclude the fully connected layers).
3. Explain why convolutional layers are important for feature extraction.

#### Example Code Snippet:
```python
vgg = VGG16(include_top=False, weights='imagenet')
```

#### Task 3.2: Extract Feature Layers
1. Identify specific layers in VGG16 that will be used for extracting content and style features (e.g., block4_conv1 for content, block1_conv1 to block5_conv1 for style).

 Hint:

Content Features: Layers like block4_conv2 capture high-level features such as shapes and objects, making them ideal for preserving the structure of the content image.

Style Features: Layers like block1_conv1, block2_conv1, block3_conv1, block4_conv1, and block5_conv1 capture different levels of textures and patterns, ranging from simple edges to complex features.

3. Write a function to extract these features from the model.

---

### Assignment 4: Style Transfer Implementation

#### Task 4.1: Compute Content Loss
1. Write a function to calculate content loss between the target and generated content features.
2. Use the mean squared error (MSE) for the calculation.

#### Task 4.2: Compute Style Loss
1. Write a function to calculate style loss using Gram matrices.
2. Explain how the Gram matrix captures style information.

#### Example Code Snippet (Incomplete):
```python
def gram_matrix(tensor):
    # Complete this function to compute the Gram matrix
    pass
```

#### Task 4.3: Optimize the Generated Image
1. Use TensorFlow’s optimizers to minimize the combined loss (content + style).
2. Adjust the weights of content and style loss to achieve different effects.

---

### Submission Instructions
1. Save your work in a Jupyter notebook.
2. Include comments to explain each step.
3. Submit your notebook and any required images via the provided submission platform.

### Optional Assigment
Experiment with different content and style images. Observe how changing the image pair affects the output and document your findings.

Hyperparameter Tuning: Experiment with different values for content and style loss weights (alpha and beta) to see how they influence the output. Record the impact on style transfer quality.

