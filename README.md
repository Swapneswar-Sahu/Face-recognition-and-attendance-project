
# Attendance project by face recognition

So first in my code I needed to tackle the problem of Locating the Faces in the Photographs and comparing them in the Webcam.
So here we used Histogram of Oriented Gradients or in short HOG, which helps in detects Faces in cheapest of Cameras.

But in this code our Goal is to identify the Faces where the Landmark Estimation algorithm comes in, which chooses 68 specific points or Landmarks
which exists on every face, so we will train a machine learning algorithm to be able to find these 68 specific points on any face, with this no matter how the face is turned
we can centre the Eyes and Mouth Roughly but just enough

and Now to measure the faces, we took Deep convolutional Neural Network, we train this to generate 128 measurements for each face, we do this by the method of embedding,
it is the Idea of reducing complicated raw data into a list of computer generated numbers which comes up a lot in machine learning.

And now to the main part, Telling actual faces apart, we can do this by getting some basic measurements from each face, for this
we can use any basic classification algorithm, so we use simple Linear SVM classifier for it, which we then train to take the measurements from a new test image
and get the closest match and the Result of Classifier is the name of the Person and then we store it in the excel sheet as the attendance of that person.

For detailed information please read the article which I have taken for my referance:
https://medium.com/@ageitgey/machine-learning-is-fun-part-4-modern-face-recognition-with-deep-learning-c3cffc121d78