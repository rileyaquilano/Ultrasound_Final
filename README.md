# Ultrasound_Final

The motivation of this project is to use computer vision to design a program that can automatically measure the fetal head circumference in ultrasound images. The product of this project will also have the potential to become a real-time program that can tell the ultrasound provider the critical information. 

During pregnancy, ultrasound imaging is used to measure fetal biometrics. One of these measurements is the fetal head circumference (HC). The HC can be used to estimate the gestational age and monitor growth of the fetus. The HC is measured in a specific cross section of the fetal head, which is called the standard plane. The dataset for this challenge contains a total of 1334 two-dimensional (2D) ultrasound images of the standard plane that can be used to measure the HC. This challenge makes it possible to compare developed algorithms for automated measurement of fetal head circumference in 2D ultrasound images. 

Due to the arise of the low-cost hardware, ultrasound imaging has been playing a major role global public health, especially in resource-constrained regions. Ultrasound technology is relatively inexpensive comparing to other medical devices, and it plays a huge role in fetal health during the mother's pregnancy. However, it takes a long time to train qualified professionals to operate and interpret the information and images gathered from ultrasound technology. Therefore, there is much need in developing AI methods to effectively train practitioners and interpret the images. 

So, in this project, we would utilize various methods and models in the field of computer vision to build an ultrasound image recognition and measurement program.

Below we indicate the role and progress history of each of the team members.

Meng -

Emma - 

riley -

  In further exploring different architectures for potential models, I experimented briefly with Nas-Unet (Neural architecture search UNET). In the respective paper by Weng, et al. their team showed useful applications with respect to ultrasound. The main objective of Nas-UNET is to find architectures that have high evaluation performance on any new data. However, early on in developing this architecture, I instead opted to switch to a “pix2pix” (Isola, et al.) model approach instead. 
  Pix2pix is a conditional generative adversarial network that learns how to map an input image into an output image. The model of pix2pix consists of optimizing G, or the generation of an image from an input, and D, a discriminator that attempts to recognize which images are real or not. Ultimately the goal is to train G to fool D given enough data. This is accomplished by first maximizing the discriminator function and then minimizing the generation function. At first, many problems arose due to our dataset needing to be reformatted to fit the criterion of the model. This was a problem that ultimately was not fully rectified due to time constraints on the assignment. Why this was the case, is that pix2pix requires two “sets” of data (called A and B in the main paper) which must be composed of some general structure (or a mask) and its ground truth equivalent for train, test, and validation. Furthermore, each respective equivalent image must have the same root name in its file (i.e. A/train1.png and B/train1.png). Ultimately this was the single roadblock that was in the way for a considerable amount of time but everything else seems to be formatted correctly to me.

