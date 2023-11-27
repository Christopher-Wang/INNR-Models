# Implicit Neural Neural Representations

## Introduction

Implicit Neural Representations (INR) are a class of functions that model discrete signals as continuous by learning a representation that maps values directly from coordinate space. For instance, a colour image is a discrete signal of $(r, g, b)$ values that is defined by $(x,\ y)$ coordinates. An implict neural representation for an image is a function $f(x,\ y\ |\ \theta) → (r_{x, y},\ b_{x, y},\ g_{x, y})$ with a maximum domain of $(height,\ width)$. Notably, the domain is of fixed size with discrete pixel intervals however the learned function $f(x,\ y\ |\ \theta)$ is continuous.

INRs have been used to map a variety of different data modalities, from images to audio to point clouds to 3D scenes. Popular examples of INRs include [Neural Radiance Fields (NeRFs)](https://arxiv.org/abs/2003.08934) and [Sinusoidal Representation Networks (SIRENs)](https://arxiv.org/abs/2006.09661). To my knowledge this is the first work that attempts to apply INRs to completely represent a neural network. I call this class of network an Implicit Neural Neural Representation, or INNR (pronounced inner). The goals of this work are as follows.
1. Identify the feasibilityof representing neural network architectures as a continuous signal.
2. Explore the performance impact of using INNR models as a form of network compression. This is particularly exciting as this methodology does not require any of the original training data other than the weights of the model itself.
3. Understand how INNR models may be vulnerable to evasion attacks from their original model.

This project was chosen as the code snippet for review for Christopher Wang's MILA application for Fall of 2024. The Jupyter notebook mila_application.ipynb contains the relevant code snippets. Please see the **INNR Model Training** section for an example of novel scientific code. This project is ideal because of its limited scope, ease of readability, and interesting results. All experiments were conducted on Google Colab using a T4. [To run yourself please access this google colab link.](https://colab.research.google.com/drive/1qec4bnKUIW9pAaAA3BfiNIocuZkt4A-w?usp=sharing) All code authored by Christopher Wang solely.
