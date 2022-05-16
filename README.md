# DeepLearningAudioRecognition


# Audio classifier

We got 2-5 seconds audio sample of bird calls for this short project. We'll read these files into Python and use the TensorFlow package.

The audio files are waveforms, and we want to convert them to spectograms.

Converting the audio data into spectograms enables us to do classification using computer vision techniques such as Convolutional Neural Networks (CNN).

Once we get the spectograms, we will load them into our TensorFlow-based CNN.

The result will be a binary outcome (1 or 0). If we heard a capuchin bird, the value will be 1, else it will be 0.

The goal of this classification is to determine the density of bird cries inside a specific audio file. The final audio file with which we will compare our model will be slightly longer (3 mins each). 

These large clips must be cut into window pieces. We will then slide our TensorFlow neural network, which has been trained on 3s bird clips.

The number of calls heard can then be determined. The consecutive detection of calls will then be combined together and treated as a single event.

The output file will be a CSV containing all of the outputs.
## Data
The data comes from the Kaggle challenge: "Z by HP Unlocked Challenge 3 - Signal Processing".
https://www.kaggle.com/datasets/kenjee/z-by-hp-unlocked-challenge-3-signal-processing

**The Task**

The Challenge is to build a Machine Learning model and code to count the number of Capuchinbird calls within a given clip. This can be done in a variety of ways and we would recommend that you do some research into various methods of audio recognition.

**Data Explorer**

We are going to have 3 different folders
* Forest Recordings
  - These are the full clips that we need to pass trough and count the number of calls
* Parsed_Capuchinbird_Clips
  - 3s audio clip of Capuchinbird calls
* Parsed_Not_Capuchinbird_Clips
  - 3s audio clip of not-Capuchinbird calls
