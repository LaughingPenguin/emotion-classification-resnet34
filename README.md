# Emotion Classification from Voice Using ResNet34 and Transfer Learning

Our implementation of emotion detection and classification using ResNet34 and transfer learning. Main libraries used were Librosa for preprocessing audio data (.wav) into Mel spectrograms and Fast.ai (v1) to fit the convolutional neural network to our specific training dataset.

### Reproducing Results

To run our code for training the neural network, make sure your project folder's directory and subfolders match what is shown below.

``` 
├── Project Directory
│   ├── RAVDESS
│   │   ├── Angry (03-01-05)
│   │   ├── Calm (03-01-02)
│   │   ├── Disgust (03-01-07)
│   │   ├── Fearful (03-01-06)
│   │   ├── Happy (03-01-03)
│   │   ├── Neutral (03-01-01)
│   │   ├── Sad (03-01-04)
│   │   ├── Surprised (03-01-08)
│   ├── sorted_data
│   │   ├── angry
│   │   ├── calm
│   │   ├── disgust
│   │   ├── fearful
│   │   ├── happy
│   │   ├── models
│   │   ├── neutral
│   │   ├── sad
│   │   ├── surprised
│   ├── test_folder
│   ├── train_folder
```

### Results

93% accuracy rate when trained and tested on Mel spectrogram images of 144x144 resolution. 97% accuracy rate when retrained and tested on Mel spectrogram images of 288x288 resolution. Model was retrained repeatedly on specified layers, which was determined by examining its learning rate vs loss function to optimize the learning rate on lower layers and higher layers.

### Addtional Features

We furthered the project to create a fun, live audio feature. In the Jupyter Notebook (does not work with Google Colab, use VSCode instead), users can record their own line reading and have the model predict what the emotion in their voice.

### Training Dataset

Livingstone SR, Russo FA (2018) The Ryerson Audio-Visual Database of Emotional Speech and Song (RAVDESS): A dynamic, multimodal set of facial and vocal expressions in North American English. PLoS ONE 13(5): e0196391. https://doi.org/10.1371/journal.pone.0196391.
