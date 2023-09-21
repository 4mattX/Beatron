# 🎶 Beatron 🎶
🎵 **Open-Source decoder only generative pre-trained model to generate MIDI music!** 🎵


🎉 Welcome to Beatron! 🎉 Dive deep into the power of GPT-like architectures for MIDI music generation. Everything you need is neatly packed within a Jupyter notebook for a quick start.

✨ _Quick Highlight:_ This project is all about MIDI music generation with GPT-like architectures. Explore the code, which is richly documented, and get started with just one Jupyter notebook. Modify to your heart's content!


### 🙏 Shoutout To...
- **kvnsoufal**'s MidiTransformer 🎼
  - 📘 [Implementation Here](https://github.com/kvsnoufal/MidiTransformer) 
  - 📖 [Medium Article](https://medium.com/mlearning-ai/generating-music-with-gpt-b0f4ab738b58)
  
- The [**BEST GPT Youtube walkthrough**](https://www.youtube.com/watch?v=kCc8FmEb1nY&ab_channel=AndrejKarpathy) by Andrej Karpathy's 📺


## 📘 Table of Contents
- [🚀 Getting Started](#getting-started)
  - [🔍 Important to know](#important-to-know)
  - [🛠 Requirements](#requirements)
  - [🗂 File Structure](#file-structure)
- [🏋 Training the Model](#training-the-model)
- [🔬 Loading and Running Tests](#loading-and-running-tests)




## 🚀 Getting Started

### 🔍 Important to know!
- 📓 Built for notebook environments: Jupyter, Databricks, and Google-Colab!
- 🎵 MIDI data encodings are thanks to [MidiTok](https://miditok.readthedocs.io/en/latest/index.html). 
  - 🎹 Generate your own dataset with the [RemiPlus](https://miditok.readthedocs.io/en/latest/tokenizations.html#remiplus) tokenizer.

### 🛠 Requirements
- 🎹 MidiTok (For the rhythms of MIDI file tokenization)
- 🧠 PyTorch (The brain behind model creation, training, and inference)
- 📊 Pandas (For the symphony of data manipulation)
- 🔢 NumPy (To hit the right notes with numerical operations)
  
#### Install with ease 📦:
  ```pip install MidiTok```



### 🗂 File Structure

Navigating the repo is as easy as reading sheet music! 🎵
- `output/`: 📁 Your saved symphonies (trained model checkpoints).
- `data_plots/`: 📊 Visual charts (training-related plots).
- `encoding/`: 🔢 Encoded melodies ready for performance.
- `preload/`: 🚀 Pre-tuned data structures for an encore during training.
- `songs/`: 🎶 Freshly composed MIDI songs.
- `logs/`: 📜 The chronicles (log files) of the training concert.


## 🏋 Training the Model

1️⃣ Get things rocking with the `train` function:
   - Orchestrates the training process: from logging, data loading to the grand performance of training a Transformer model.
   - Your music (model checkpoints) are safely stored in the `output/` directory.

2️⃣ Dance along with the training rhythm using the `plot_and_save` function:
   - Visual feedback (loss plots) will be stored in the `data_plots/` directory as the model learns.

3️⃣ Never miss a note! Record training details with the `save_training_info` function:
   - Detailed logs and parameters are saved in the `data_plots/` as text documents for your reference.
     

## 🔬 Loading and Running Tests

1️⃣ Load up a maestro (trained model) with the `load_model` function:
   - Just point it to your chosen maestro's address (trained model checkpoint) in the `output/` directory.

2️⃣ Command your orchestra (generate MIDI songs) using the testing loop:
   - Kick things off with an initial MIDI sequence from the `encoding/` directory.
   - Your fresh compositions (generated MIDI songs) are saved in the `songs/` directory, ready for the world to hear!

🎻 _Final note:_ Tweak the constants and parameters (like `VOCAB_SIZE`, `EMBED_DIM`, etc.) to your own taste. Let your creative spirit lead the way! 🎼
