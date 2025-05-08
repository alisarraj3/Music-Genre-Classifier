# Music-Genre-Classifier
Have you ever wondered how shazam works? Have you ever wondered how spotify recommends music that is similar to your music taste? All of these things are possible because of two things: machine learning and audio analysis. We will be exploring both of these in this report through implementing a music genre classifier that will determine if a song's genre is either jazz or metal, using Bayes theorem.
Bayes Theorem
P(A|B) = P(B|A) * P(A) / P(B)
Bayes Theorem is a powerful tool in the probability toolkit. It allows us to calculate the probability of an event based on prior knowledge of conditions that are related to the event. We will use it to determine the probability a song is either jazz or metal (more specifically, we will use Gaussian Naive Bayes, more on that later in the report). But how do we go about this? Well this is where audio analysis comes into play. We will examining what is called the 'features' of a soundwave, which are charateristics or properties of the wave.

Key Features Include:
Chroma: a representation of the harmonic contents. Also can be thought of as the energy or intensity of a sound wave.
Root Mean Square (RMS): the average loudness of a wave.
Spectral Centroid: the center of mass or the balance of a signal. So if a song has more frequencies towards the end, it's spectral centroid will be towards the end. Whereas if it has a more even distribuition of frequencies, it's spectral centroid will be somewhere in the middle. It can be thought of as the average frequence of a sound spectrum.
Spectral Bandwidth: Also dealing with frequencies, this indicates how spread out the frequencies are along the sound spectrum.
Mel-Frequency Cepstral Coefficient (MFCC): Arguably the most complex and least intuitive in this list, MFCC's are fundamental in any sound recoginition technology. They are coefficients that represent the spectral characteristics of an audio signal in the context of how humans percieve sound. They are computed using an algorithm which involves the Fourier transform to represent oscillating functions as summations, the Mel-Scale which represents the way humans percieve sound in pitch, and a number of other mathematical steps (more details can be found in the section for MFCC's in the sources at the end of this report). MFCC's are difficult to define, but reading through how they are computed can give somewhat of an understanding. But for our purposes, what we need to know is that they are multiple coefficients which capture unique characteristics in sound waves, and we will use 20 of them in the process of classifying the genre.
Zero Crossing Rate: the rate at which a soundwave changes signs (i.e the rate at which a wave changes from positive to negative.


