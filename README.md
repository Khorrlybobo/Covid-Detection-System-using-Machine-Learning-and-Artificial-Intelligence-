# Covid-Detection-System-using-Machine-Learning-and-Artificial-Intelligence-

  ## How the Code Works

1. **Importing Libraries and Modules:**
   The code starts by importing necessary libraries and modules for audio processing, data manipulation, visualization, and machine learning.

2. **Loading Audio Data:**
   The code loads audio data from a file using a given UUID (Universal Unique Identifier) and extracts the audio signal, sample rate, and other relevant information.

3. **Zero Padding:**
   The loaded audio signal is then zero-padded to a target duration. This ensures that all audio signals have the same length for consistency in further processing.

4. **Calculating Spectral Features:**
   The Short-Time Fourier Transform (STFT) and Mel-Frequency Cepstral Coefficients (MFCC) are computed from the audio signal. These features provide information about the frequency content and spectral characteristics of the audio.

5. **Calculating Power Spectrum:**
   The power spectrum is calculated using Welch's method, which estimates the power spectral density of the audio signal.

6. **Plotting Raw Audio Signal:**
   The raw audio signal is plotted over time using Plotly. The x-axis represents time in seconds, and the y-axis represents amplitude.

7. **Plotting STFT Spectrogram:**
   The STFT spectrogram, which displays the frequency content over time, is plotted using Librosa and Matplotlib. The x-axis represents time, the y-axis represents log-scaled frequencies, and color represents magnitude.

8. **Plotting MFCC Spectrogram:**
   The MFCC spectrogram, which highlights the significant features of the audio signal, is plotted in a similar manner to the STFT spectrogram.

9. **Plotting Power Spectrum Density:**
   The power spectrum density is plotted, showing the frequency distribution of the audio signal's power.

10. **Splitting Train-Test Data:**
   The dataset is split into training and testing sets, with features extracted from the audio data. The split is stratified to maintain class distribution.

11. **Selecting Features and Labels:**
   The features for classification are selected, including various audio characteristics and spectrogram features. The label is the 'STATUS' column, indicating the health status of the audio sample.

12. **Normalizing Data:**
   The training and testing features are normalized using Min-Max scaling. The label (status) is encoded using LabelEncoder.

13. **Setting Up Logistic Regression:**
   A Logistic Regression model is set up for multiclass classification. The 'multi_class' parameter indicates multinomial classification, and the model is fitted to the training data.

14. **Evaluating Logistic Regression:**
   The logistic regression model is evaluated using accuracy, precision, recall, and confusion matrix on both the training and testing datasets.

15. **Setting Up XGBoost Classifier:**
   An XGBoost classifier is configured with specified parameters for multiclass classification. The model is fitted to the training data using the XGBoost library.

16. **Evaluating XGBoost Classifier:**
   The XGBoost classifier's performance is evaluated similarly to the logistic regression, including accuracy, precision, recall, and confusion matrix, for both the training and testing datasets.

17. **Plotting Feature Importance:**
   The top 10 most important features for the XGBoost classifier are plotted using a horizontal bar chart.

18. **Plotting Loss Evolution:**
   The evolution of training and testing log loss is plotted over the iterations (number of trees) for the XGBoost classifier.

19. **Merging Predictions:**
    The predictions of both the logistic regression and XGBoost classifiers are merged back into the original dataset using UUIDs for comparison.
