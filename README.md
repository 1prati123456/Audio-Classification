# Audio-Classification
AI in Industry Project | Audio Classification on 30k audio files

The aim of this project is to perform multi-label classification on Audio data. The audio files are short audio samples with different informations like GENRE, CATEGORY, INSTRUMENT, KEY etc..

There are total 29220 audio files
First we will focus on the GENRE classification of the audio files and then the similar approach will be used to classify other categories


Mel-frequency cepstral coefficients are commonly used to represent texture or timbre of sound.

MFCCs are commonly derived as follows:

Take the Fourier transform of (a windowed excerpt of) a signal.
Map the powers of the spectrum obtained above onto the mel scale, using triangular overlapping windows or alternatively, cosine overlapping windows.
Take the logs of the powers at each of the mel frequencies.
Take the discrete cosine transform of the list of mel log powers, as if it were a signal.
The MFCCs are the amplitudes of the resulting spectrum.
They are derived from a type of cepstral representation of the audio clip (a nonlinear "spectrum-of-a-spectrum"). The difference between the cepstrum and the mel-frequency cepstrum is that in the MFC, the frequency bands are equally spaced on the mel scale, which approximates the human auditory system's response more closely than the linearly-spaced frequency bands used in the normal spectrum. This frequency warping can allow for better representation of sound, for example, in audio compression that might potentially reduce the transmission bandwidth and the storage requirements of audio signals.

There are total 39 mfcc coefficient values and 13 is said to be the average number which usually is enough for classification. Here 8, 13, 20 and 39 mfcc coefficients were checked and 13 gave the best results.

The two models used were -
1- ANN
2- KNN

ANN gives better result than the KNN but still not that great. The main reason for the bad performance is suspected to be the unbalanced dataset. So, classification was done using OVERSAMPLING and the performace of the model increased.

The similar approach was implemented on the category class for classification later.
