# DL-CNN
A CNN, or Convolutional Neural Network, is a specialized type of deep learning algorithm designed primarily to process and analyze grid-like data such as images and videos. It automates feature extraction, allowing computers to recognize patterns, objects, and faces without manual intervention
The he Three Core Layers
- A CNN achieves its results by passing the image data through three distinct types of layers, each serving a specific purpose.

1. Convolutional Layer (Feature Extraction)
  This is the heart of the network. Instead of connecting every input pixel to a neuron, a CNN uses filters (also called kernels). A filter is a small grid of weights—often just 3x3 pixels—that slides across the entire image.
<img width="412" height="242" alt="image" src="https://github.com/user-attachments/assets/6ce1c8da-48b2-4dc3-a86d-64a68dba7d74" />
-As the filter slides (or "convolves"), it performs a calculation to detect a specific pattern.

- Early layers use these filters to learn simple features like vertical edges or color gradients. Deeper layers combine these simple features into complex ones, like eyes, wheels, or leaves.

- The Big Advantage: Parameter sharing. A single 3x3 filter uses exactly the same 9 weights to scan the entire image. This drastically reduces the size of the model compared to a standard network.

2. Pooling Layer (Down sampling)
- Once the convolutional layer maps out where features are located, the pooling layer intentionally shrinks the spatial dimensions of that map.

- Max Pooling is the most common method: it looks at a small patch (e.g., a 2x2 grid) of the feature map and keeps only the highest numerical value, discarding the rest.

- This reduces the computational load and helps the network become translation invariant—meaning the network learns to care about whether a feature exists, rather than its exact pixel-perfect location.

  3. Fully Connected Layer (Classification)
- After the image has been passed through multiple alternating Convolutional and Pooling layers, it has been compressed down into a deep, highly abstracted "feature map."

- Only at this very end is the data finally flattened into a 1D array.

- This flattened array feeds into a standard dense network (the exact type of network discussed previously) to output the final prediction probabilities (e.g., "Cat" 90%, "Dog" 10%).
