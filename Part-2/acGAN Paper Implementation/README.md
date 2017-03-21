
## acGAN Paper Implementation from the FAST AI courses, Part2

Here is our implementation of the acGAN Paper. The original paper is listed below :

-	**Face Aging With Conditional Generative Adversarial Networks** | Grigory Antipov, Moez Baccouche, Jean-Luc Dugelay : [Available here](http://arxiv.org/abs/1702.01983)

We plan to implement it with respect to some modifications as our contribution.



=================================

# THE PROCEDURES

The acGAN model proposed in the acGAN Paper uses :

1- The same design for the generator G and the discriminator D as in [[15]](https://arxiv.org/abs/1511.06434). 

2- Following [[12]](https://arxiv.org/abs/1611.06355), we inject the conditional information at the input of G and at the first convolutional layer of D. (Code available at https://github.com/Guim3/IcGAN)

3- acGAN is optimized using the ADAM algorithm [[16]](https://arxiv.org/abs/1412.6980) during 100 epochs which takes about one day on a modern GPU. 

4- In order to encode person’s age, we have defined six age categories: 0- 18, 19-29, 30-39, 40-49, 50-59 and 60+ years old. They have been selected so that the training dataset (cf. Subsection 3.1) contains at least 5, 000 examples in each age category. 
Thus, the conditions of acGAN are six-dimensional one-hot vectors.

5- Our acGAN has been trained on the IMDB-Wiki cleaned dataset [[20]](http://www.eurecom.fr/en/publication/4908/download/sec-publi-4908.pdf)

6- 



+++++++++++++++++++++++++++++++++

### Some References
-	**Age and gender classification using convolutional neural networks** | Gil Levi, Tal Hassner
[Available here](http://www.openu.ac.il/home/hassner/projects/cnn_agegender/CNN_AgeGenderEstimation.pdf)
