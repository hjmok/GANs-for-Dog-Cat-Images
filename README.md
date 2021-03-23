# GANs for Dog/Cat Images

The purpose of this project was to create Dog & Cat images with a Generative Adversarial Network.

The dataset consisted of 24,994 prelabelled photos, evenly split between dogs and cats. The dataset was taken from Kaggle's Dogs vs. Cats Dataset:
https://www.kaggle.com/c/dogs-vs-cats

## GAN Basics
For this Deep Learning model, PyTorch was used for its flexibilty as we needed to create two neural networks: The Discriminator and The Generator. The basic idea will be that the Generator will create images of fake dogs and cats, and the Discriminator will be given both fake and real images to determine which dogs and cats are real. As the Discriminator gets better at distinguishing between real and fake images, the Generator will also improve by creating more realistic images over time.

# Discriminator Model
The purpose of the Discriminator is to classify between images of real and fake dogs and cats. As such, the Discriminator will be a Convolutional Neural Networking.
The CNN starts with a convolutional layer with 3 inputs. The hidden layer consists of 64, 128, 256, and 512 neurons, all using LeakyReLU as the activation function. The final output is determined by a Sigmoid function to decide whether the image was real or fake.

# Generator Model
The purpose of the Generator is to create fake images of the dogs and cats that become more realistic by using feedback from the Discriminator. As such, the model will be an inverse of a Convolutional Neural Network.
This inverse CNN is layered with the following: 100, 512, 256, 128, 64, and 3. The activation function for the hidden layers were all ReLU, and the final output activation function is the hyperbolic tangent function.

# Optimizer and Loss
For both neural networks, Adam optimizer was found to perform well.
In addition, Binary Cross-Entropy loss was used since the final result will be a mutually exclusive binary answer (either real or fake, cannot be both)

# Results 
Please find results in the following link: https://hjmok.github.io/josephmok_portfolio/#/GAN#portfolio 
