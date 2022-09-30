# Handwritten-Digits-Generator-With-a-GAN
Generative adversarial networks are machine learning systems that can learn to mimic a given distribution of data.
GANs consist of two neural networks, one trained to generate data and the other trained to distinguish fake data from real data (hence the “adversarial” nature of the model).
During the training process, an algorithm is used to adjust the model’s parameters. The goal would be to minimize a loss function so that the model learns the probability distribution of the output given the input. After the training phase, you could use the model to classify a new handwritten digit image by estimating the most probable digit the input corresponds to, as illustrated in the figure below:
![image](https://user-images.githubusercontent.com/85798077/193280049-8aa8e262-04a7-4417-87dc-0438932ee71b.png)
Using the dataset of handwritten digits, a generative model is trained to generate new digits. During the training phase, algorithm is used to adjust the model’s parameters to minimize a loss function and learn the probability distribution of the training set. Then, with the model trained new samples are generated, as illustrated in the following figure:
![image](https://user-images.githubusercontent.com/85798077/193280358-271c4c83-c12c-44f2-9caa-0db822738679.png)
# Preparing the Training Data
The MNIST dataset consists of 28 × 28 pixel grayscale images of handwritten digits from 0 to 9. To use them with PyTorch, conversions is necessary. For that a transform function is used when loading the data:
transform = transforms.Compose([transforms.ToTensor(), transforms.Normalize((0.5,), (0.5,))])
Matplotlib is used to plot some samples of the training data. To improve the visualization, cmap=gray_r is used to reverse the color map and plot the digits in black over a white background:
![image](https://user-images.githubusercontent.com/85798077/193281201-f699cca8-53aa-4eb8-bb48-7ff6a9c5b676.png)
# Samples Generated by the GAN
![image](https://user-images.githubusercontent.com/85798077/193281334-65a88c75-41fc-4f88-ac2e-a27c813b268a.png)
