# _Immersic_
> This section of this README contains the original project proposal at the time of project inception.
### Problem Statement
Generation of ambient music using neural networks.
### Why is it unique? 
- We plan to implement this music generator to create music that sounds as natural as possible, without lyrics. 
- This leads to our project essentially becoming a tool to compose scores/background music seamlessly. 
- Music can be generated as per a user’s choice, with zero intervention beyond a simple prompt.
### Possible Datasets
- MIDI (Musical Instrument Digital Interface) files
- Any music files that are not licensed/copyrighted, to avoid copyright issues
### Method
- Application of basic music theory to identify characteristics in the training dataset, which will then subsequently be used to generate music.
- Training a neural network on MIDI files to extract features of the audio, such as notes and chords.
- Choice of neural network broadly comes under the category of RNNs and/or Time-Series.
- Potential libraries to be used: **`tensorflow`, `music21`**

# Project Documentation
> This section of this README contains the actual project documentation, which is a work in progress.
### Data Information
The base dataset used for this project is a subset of the Lakh MIDI dataset, which contains about 17000 MIDI files.

Note that `Data/Archive` is ignored by Git, due to a very large directory size (about 874MB).
The dataset can however be downloaded from here: https://www.kaggle.com/datasets/imsparsh/lakh-midi-clean
- `Data/Archive` contains the raw MIDI files, separated into multiple subdirectories.
- `Data/Preprocessed` contains usable data formats for future purposes.

# Important Links
### Datasets
- https://colinraffel.com/projects/lmd/
- https://www.kaggle.com/datasets/imsparsh/lakh-midi-clean
- https://www.kaggle.com/datasets/saikayala/jazz-ml-ready-midi
- https://github.com/mdeff/fma
- https://magenta.tensorflow.org/datasets/nsynth
- https://magenta.tensorflow.org/datasets/e-gmd
- https://www.kaggle.com/datasets/vincentloos/classical-music-midi-as-csv

### Articles
- https://blog.paperspace.com/music-generation-with-lstms/
- https://towardsdatascience.com/how-to-generate-music-using-a-lstm-neural-network-in-keras-68786834d4c5