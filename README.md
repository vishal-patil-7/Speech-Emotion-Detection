# Speech-Emotion-Detection
This project is about building a Speech Emotion Recognition (SER) system that identifies emotions from human speech using audio files. The system extracts key audio features such as MFCC (Mel Frequency Cepstral Coefficients), Chroma, and Mel Spectrogram to train a Support Vector Machine (SVM) model, which can classify emotions like happiness, sadness, anger, and neutrality.

## Steps Involved
### 1. Mount Google Drive
To access the dataset, we mount Google Drive in Google Colab. This allows the program to read files stored in the user's Google Drive.

### 2. Set Dataset Path
The dataset of .wav audio files is stored in a specific folder within Google Drive. The path to this folder is set in the code so that the program can locate the audio files.

### 3. Print Files in Dataset Directory
This step lists all the files in the specified dataset directory to ensure that the .wav files are available and correctly loaded. This helps in verifying that the dataset is ready for use.

### 4. Install Required Libraries

- librosa: Used for extracting audio features from the .wav files.
- soundfile: Used to read and write sound files.
- scikit-learn: Used for machine learning tasks like training the model.

### 5. Extract Features from Audio Files
We define a function to extract important features from the audio files:

- MFCC (Mel Frequency Cepstral Coefficients): Represents the short-term power spectrum of sound, which is useful for speech analysis.
- Chroma: Represents the 12 different pitch classes and is useful for identifying harmonic content.
- Mel Spectrogram: Provides a time-frequency representation of the audio.
These features are essential for training the model, as they help the SVM classifier understand and differentiate between various emotions in speech.

### 6. Load Data and Train-Test Split
The data is loaded by reading the .wav files and extracting the audio features. The filenames of the audio files contain labels that correspond to different emotions. We map these labels to the extracted features and then split the data into training and testing sets.

### 7. Train SVM Classifier
An SVM (Support Vector Machine) classifier is trained on the extracted audio features. This model learns to classify different emotions based on the patterns in the audio features.

### 8. Test with a New Audio File
After training the model, we can test it using a new audio file. The program extracts features from the new file and predicts the emotion expressed in the speech based on what the model has learned.

## Conclusion
This project demonstrates how to classify emotions from speech using audio feature extraction and machine learning. The SVM classifier is trained on features like MFCCs and predicts emotions with reasonable accuracy. Future enhancements can include the use of deep learning models like CNNs or RNNs to improve performance and accuracy.






