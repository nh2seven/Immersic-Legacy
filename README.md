# _Immersic_
> This section of this README contains the original project proposal at the time of project inception. This project began as a submission for the MML course at PES University, Bangalore.
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
> This section of this README contains the actual project documentation. Changes made to the project after the initial proposal are also documented here.
- This project aims to be able to seamlessly generate ambient music, by training a LSTM model on a dataset of ambient music. The model will be able to generate music that is similar to the input dataset, but not identical. This will allow for the generation of new music that is unique, but still in the style of the input dataset.
### Dataset Used
- The dataset used for training is a collection of ambient music MIDI files, which can be found [here](https://github.com/nmtremblay/lofi-samples), along with other miscellaneous MIDI samples.
### Setup
1. Non-GPU Setup
    - To run this project without a GPU, any version of [python3](https://www.python.org/downloads/) that supports the latest version of TensorFlow will do.
    - Run `pip install -r requirements.txt` to install the required libraries.

2. GPU Setup
    - To run this project with a GPU, a CUDA-compatible GPU and the appropriate drivers are required.
    - To avoid any compatibility issues/interference, it is recommended to create a new conda environment, and install the required libraries in that environment.
    - It is recommended to use the [Anaconda Navigator](https://www.anaconda.com/download/success) instead of [Miniconda](https://docs.anaconda.com/free/miniconda/), as it comes with all the necessary packages pre-installed.
    - For the steps mentioned above, find the installation instructions [here](https://www.tensorflow.org/install/gpu).
### Preprocessing
- The `music21` library is the main library used to parse the MIDI files, and extract the notes and chords from them.
- Alternatives to `music21` are `pretty_midi` and `miditoolkit`, but `music21` is the most popular and widely used library for MIDI file processing.
- Due to the memory intensive nature of this process, it is separated from the main notebook for better memory management.
- This is done to avoid re-extraction of features every time the dataset may be changed.
### Model Training
- The model used for this project is a LSTM model, which is a type of RNN.
- The model has 1 dropout layer, 3 LSTM layers, 4 dense layers and 1 activation layer for the output.
- In the tests conducted, the model was trained for 500 epochs, with a batch size of 64. 
- Due to the limited dataset, underfitting can be a commmon issue, which can be resolved by increasing the number of epochs or reducing the number of neurons in each layer.
- Checkpointing is used to save the model weights after every epoch, so that the model can be reloaded from the last checkpoint in case of a crash.
- A plot of the loss over time can be found in `Immersic.ipynb`.
### Music Generation
- The model is used to generate music by feeding it a seed sequence of notes and chords, and then predicting the next note or chord in the sequence.
- After music is generated, it is saved as a MIDI file, which can be played using any MIDI player locally.

# Important Links
> This section of this README contains important links that are relevant to the project/were referred to during development.
### Possible Datasets
- https://colinraffel.com/projects/lmd/
- https://www.kaggle.com/datasets/imsparsh/lakh-midi-clean
- https://www.kaggle.com/datasets/saikayala/jazz-ml-ready-midi
- https://github.com/mdeff/fma
- https://magenta.tensorflow.org/datasets/nsynth
- https://magenta.tensorflow.org/datasets/e-gmd
- https://www.kaggle.com/datasets/vincentloos/classical-music-midi-as-csv
- Any other small dataset you may find can be used for this project. 

### Articles
- https://blog.paperspace.com/music-generation-with-lstms/
- https://towardsdatascience.com/how-to-generate-music-using-a-lstm-neural-network-in-keras-68786834d4c5