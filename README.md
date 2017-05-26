# Image Classifier

**By:** Daksh Gupta

**Project Description:**

***Libraries Required:*** OpenCV 3.1.0

This is an image classifier, that classifies images as Spam or Notspam. Here Spam images refer to images that have large amount of text, memes, cartoons etc. and Notspam images in general are clicked pictures of humans, landscapes, animals etc.

I have manually collected and labeled my dataset which has a total od 3,426 images. The images are my personal clicks and images I think of as SPAM from my WhatsApp images folder.

The classifier uses the following features to describe the images:

- No. of faces in the image
- No. of distinct color in the image
- % area of image covered by text
- % area of image covered by top color 1
- % area of image covered by top color 2
- % area of image covered by top color 3
- % area of image covered by top color 4
- % area of image covered by top color 5
- % area of image covered by top color 6
- % area of image covered by top color 7
- % area of image covered by top color 8
- % area of image covered by top color 9
- % area of image covered by top color 10

From basic experimentation, I found that in general, Spam images have very less number of unique colors and the ones that they have share a occupy a large number of image pixels. On the other hand, Notspam images have a large number of unique colors.

To get a proper number of unique colors, I have considered only the colors/shades that occupy more than 0.5% of the image.

I will be selecting the best out of SVC, LogisticRegression, DecisionTreeClassifier, MLPClassifier and BernoulliNB to train and classify this data.

***To Run:***

Place the images in a folder called 'data' in the same folder as the Notebook. The structure of the folder should be like "*data\\notspam (1).jpeg; data\\notspam (2).jpeg; .....; data\\spam (1).jpg ...*"

The Notebook 'phase 1' processes the raw images and extracts features from them.

The Notebook 'phase 2' contains the actual image classification code.

There is a 'data.pckl' and 'labels.pckl' file with the Notebook, these contain the data matrix and the target variable numpy array respectively. The code below gives preference to loading the data from the .pckl files over processing the images again and again.

The model comparision results are stored in 'modelparams.pckl'