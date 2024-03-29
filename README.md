# _Music Generator_
> This section of this README contains the original project proposal at the time of project inception:
### Problem Statement
Generation of ambient music by using neural networks.
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