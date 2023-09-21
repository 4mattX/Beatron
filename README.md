# Beatron
Open-Source MIDI decoder only generative pre-trained model

## Table of Contents
- [Getting Started](#getting-started)
  - [Important to know](#important-to-know)
  - [Requirements](#requirements)
  - [File Structure](#file-structure)
- [Training the Model](#training-the-model)
- [Loading and Running Tests](#loading-and-running-tests)

### Appreciation To...
**kvnsoufal**'s MidiTransformer
Check out his [implementation](https://github.com/kvsnoufal/MidiTransformer) and his [Medium Article](https://medium.com/mlearning-ai/generating-music-with-gpt-b0f4ab738b58)
The [BEST GPT Youtube walkthrough](https://www.youtube.com/watch?v=kCc8FmEb1nY&ab_channel=AndrejKarpathy) by Andrej Karpathy's

## Getting Started

### Important to know!
- This is designed to function in notebooks like Jupyter, Databricks, and Google-Colab
- The encodings of the trained data are generated from [MidiTok](https://miditok.readthedocs.io/en/latest/index.html)
  - To generate your own data set use the [RemiPlus](https://miditok.readthedocs.io/en/latest/tokenizations.html#remiplus) tokenizer

### Requirements
- MidiTok (Python package for MIDI file tokenization)
- PyTorch (for model creation, training, and inference)
- Pandas (for data manipulation)
- NumPy (for numerical operations)
- Logging (for logging messages)
- Other dependencies as specified in the provided code.

### Python Package Dependencies
  ```pip install MidiTok```

### File Structure

This assumes a directory structure as shown in the various functions:
- `output/`: Where trained model checkpoints are saved.
- `data_plots/`: Directory for saving plots related to training.
- `encoding/`: Contains encoded data.
- `preload/`: Caches certain data structures for faster loading during training.
- `songs/`: Where generated MIDI songs are saved.
- `logs/`: Contains log files for the training process.

## Training the Model

1. Use the `train` function.
   - This function sets up logging, loads the MIDI data, pre-processes it, and then trains a Transformer model.
   - Model checkpoints are saved in the `output/` directory.

2. Monitor the training progress with real-time loss plots using `plot_and_save` function.
   - Loss plots will be saved in `data_plots/` directory.

3. Save training info and parameters using `save_training_info` function. 
   - This information will be saved as text files in `data_plots/`.

## Loading and Running Tests

1. Load a trained model using the `load_model` function.
   - Provide the path to a trained model checkpoint from the `output/` directory.

2. Generate MIDI songs using the provided testing loop.
   - The initial MIDI sequence is loaded from the `encoding/` directory.
   - The Transformer model then generates a new MIDI sequence based on this initial sequence.
   - The generated MIDI songs are saved in the `songs/` directory with the prefix `gameboy001_test` followed by a unique identifier.

Remember to adjust constants and parameters (like `VOCAB_SIZE`, `EMBED_DIM`, etc.) as per your specific requirements.
