# Generative Adversarial Networks

[![Tensorflow](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT7b9ZDD7lMdkByT-f_RCAqSQYqnq_CpgD16IFrwfmUwWCmdt7H)](https://www.tensorflow.org/beta/guide/effective_tf2)


[![Colab](https://camo.githubusercontent.com/52feade06f2fecbf006889a904d221e6a730c194/68747470733a2f2f636f6c61622e72657365617263682e676f6f676c652e636f6d2f6173736574732f636f6c61622d62616467652e737667)](https://colab.research.google.com/gist/JohnAntonusMaximus/eddf2a3577553dee44a5c71745f5bdb6/tf_2_0_gan.ipynb)

## Background

Generative Adversarial Networks, or GANs for short, are an approach to generative modeling using deep learning methods, such as convolutional neural networks.

Generative modeling is an unsupervised learning task in machine learning that involves automatically discovering and learning the regularities or patterns in input data in such a way that the model can be used to generate or output new examples that plausibly could have been drawn from the original dataset.

GANs are a clever way of training a generative model by framing the problem as a supervised learning problem with two sub-models: the generator model that we train to generate new examples, and the discriminator model that tries to classify examples as either real (from the domain) or fake (generated). The two models are trained together in a zero-sum game, adversarial, until the discriminator model is fooled about half the time, meaning the generator model is generating plausible examples.

GANs are an exciting and rapidly changing field, delivering on the promise of generative models in their ability to generate realistic examples across a range of problem domains, most notably in image-to-image translation tasks such as translating photos of summer to winter or day to night, and in generating photorealistic photos of objects, scenes, and people that even humans cannot tell are fake.

[![GANS Model](https://image.slidesharecdn.com/gans-170201015537/95/a-very-gentle-introduction-to-generative-adversarial-networks-aka-gans-13-638.jpg?cb=1485980114)]()



## Approach

In this example, we're constructing a generative adversarial network using Tensorflow 2.0. First we'll need to build the discriminator network and generator networks separately. We'll train the discriminator by itself and then we'll train the generator network as a combined models. When we train the generator, we need to freeze the discriminator network completely and flip the labels. 

The accuracy and loss rate is graphed in the notebook, however we notice that in a GAN loss and accuracy are not good indicators of model performance as both the discriminator and generator are learning in tandem. Instead we have to use the produced images from the generator to see how the model is improving over the epochs. 

# Links

* [KaizenTek](http://www.kaizentek.io) - IT Consulting & Cloud Professional Services