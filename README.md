# audio-ica
Performing a FastICA algo on an audio file to remove background noise. 

# What is ICA?
Independent Component Analysis (ICA) is a statistical analysis technique that uses linear algebra to 'unmix' a mixed signal with linear transformations. The idea here is that if you have two non-gaussian independently recorded source signals that happened to be mixed, we can assume that their correlation is zero and exploit that to create a nice linear algebra problem that helps us figure out the matrix that would unmix the signal. 

# Why didn't it work with music?
Audio files recorded with mics have phasing, which means that there's a timing difference between when the two independent sources were recorded. This phasing issue makes it difficult to perform ICA, since the unmixing matrix is not as nice as that when the two signals have little to no phasing. For further analysis of this project, I hope to see if I can use it to remove vinyl pops from a recording or removing a metronome that was accidentally left in a recording. If I am understanding the problem correctly, these should have no phasing issues, and therefore should be able to be extracted with ICA. Not 100% sure tho. 
