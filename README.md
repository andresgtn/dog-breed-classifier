# dog-breed-classifier
A dog breed classifier using CNNs [created on 03/24/2021]

As part of the Deeplearning nanodegree from Udacity, I implemented an image classifier using CNNs (convolutional neural networks) with Pytorch.

Udacity provides some boilerplate code and a structure, and it is up to the student to complete it. 

IMPORTANT NOTICE: If you are taking the Udacity Deeplearning course and have not completed this assignment, I'd encourage you to stop reading now for two reasons: 1) Try your best to solve the code and don't look up solutions - struggling with coming up with your own solution is what allows you to learn; 2) Copying other's code and looking up the solutions is against the course code of conduct.  But mainly, stop and try yourself so you can learn, and then come back and compare your solution against mine, which is not perfect but works fine.

The model takes as input an RGB image (224x224x3) and can detect human faces and dogs. If it is a human, it will indicate a human was detected and say which dog breed the person resembles most.  If it detects a dog, it will output the breed.  If it detects anything else, it will say it did not recognize the contents of the image.

To detect faces, I used Haar Cascades from OpenCV. 
To detect dogs, I used CNNs: a pre-trained VGG16 architecture, and custom a architecture designed by me and inspired by VGG16, but shallower than it (to speed up training).  The pre-trained model achieved better results.  The main challenge was training the custom model from scratch; even with a GPU, it requires a very long time to train if you want to achieve good results.

The code is broken into the following sections:
Step 0: Import Datasets
Step 1: Detect Humans
Step 2: Detect Dogs
Step 3: Create a CNN to Classify Dog Breeds (from Scratch)
Step 4: Create a CNN to Classify Dog Breeds (using Transfer Learning)
Step 5: Write your Algorithm
Step 6: Test Your Algorithm

The entire code is contained within dog_app.ipynb and is implemented as a mostly self-contained Jupyter notebook.  The exception is the training and test dog images, which was part of the course repo and which I have not added on this repo since I could not download it.

The file named report.html is just the dog_app.ipynb Jupyter notebook exported as HTML.

The model artifacts for both the pretrained VGG16 and custome model are included here as *.pt files.
