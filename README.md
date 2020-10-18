# EigenFaces
Implementation of Face Recognition using Eigenfaces.
This paper delves into the implementation of face detection using the concept of Eigenfaces. The work highlights the prospective of an OpenCV aided facial detection system. The aim of facial recognition is to detect faces in still images and has many methods such as local, global, and hybrid approach.

# Introduction
Face detection has been a computationally complex problem to solve: including the several dynamic variables and the differences that may exist between the training and the testing images. These variables could include the difference in lighting and angle difference in head tilting.
This design is hence focused on developing an early system that does not depend on three-dimensional geometry. This system is efficient in its scope of usage: computationally fast and reasonably simple. 
This system works well for constrained environments such as a household or an official environment with limited computational ability.

# Working and Explanations
In 1997, Pentland and Moghaddam proposed a differential eigenspace-based approach that allows the application of statistical analysis in the recognition process.
Lower-dimensional feature vectors are used to approximate the face vectors (face images) in eigenspace-based approaches.
The above-mentioned approaches consider an off-line phase of training, where the projection matrix (W∈ RN ×m), the one that achieves the dimensional reduction, is obtained by utilizing all the face images in the database.
The mean face (x) and the reduced representation of each database image (pk) are also calculated in the off-line phase.
There are a few steps involved in the detection of facial features: as described in [7], a preliminary module transforms the face image into a unitary vector (a module that implements normalization) and then performs a subtraction of the mean face. The resulting vector is projected using the projection matrix. This projection depends on the Eigenspace method that is used (PCA, FLD, etc.).
This projection corresponds to a dimensional reduction of the input, starting with vectors in RN (where N is the dimension of the image vectors) and obtaining the projected vectors q, belonging to Rm, with m<N. It is a weighted assumption of the usual case that m<<N. 
Then we note the similarity of q against each of the reduced vectors. This similarity can be computed using many parameters. One such parameter is the Euclidean distance.
When the vector q is compared with the reduced vectors, we can identify the class of the vector that is most similar to q.
Therefore, theoretically, it is imperative to maintain another class that may be labeled as a “Rejection Class”, or system, to use for when the similarity is not good enough.

# References
1. P. Viola and M. Jones, ​Rapid Object Detection using a Boosted Cascade of Simple Features,​ in the Accepted Conference on Computer Vision And Pattern Recognition, 2001.
2. M. A. Turk and A. P. Pentland, ​Face Recognition using Eigenfaces,​ in Proceedings CVPR ‘91.
3. Chen Yu, ​Linear Algebra and Face Recognition,​ Class at Indiana University.
4. CP Papageorgiou and Micheal Oren, General framework for object detection,​ February ‘98.
5. Rohan Gupta, ​Breaking Down Facial Recognition: The Viola-Jones Algorithm, August 7, 2019.
6. N. Belhumeur, P. Hespanha and J. Kriegman,​ Eigenfaces vs. Fisherfaces: Recognition Using Class Specific Linear Projection,​ IEEE Transactions On Pattern Analysis And Machine Intelligence, Vol. 19, No. 7, July 1997.
7. B. Moghaddam and A. P. Pentland,
Probabilistic Visual Learning for Object
Representation, ​IEEE Transactions on Pattern Analysis and Machine Intelligence, July 1997.
8. A. S. Khan, L. K. Alizai, ​Introduction to Face Detection Using Eigenfaces, IEEE--ICET 2006 2nd International Conference on Emerging Technologies Peshawar, Pakistan, 13-14, November 2006.
9. ZW Chan, ​Face Recognition using Eigenfaces, ​GitHub publication, usage in code for training data.
