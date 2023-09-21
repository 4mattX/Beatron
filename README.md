# 🎶 Beatron 🎶
🎵 **Open-Source - Decoder only GPT model to generate MIDI music!** 🎵
&nbsp;  
&nbsp;  
🎉 Welcome to Beatron! 🎉 Dive deep into the power of GPT-like architectures for MIDI music generation. Everything you need is neatly packed within a Jupyter notebook for a quick start.
&nbsp;  

✨ _Quick Highlight:_ This project is all about MIDI music generation with GPT-like architectures. Explore the code, which is richly documented, and get started with just one Jupyter notebook. Modify to your heart's content!
&nbsp;  
&nbsp;  
### 🙏 Shoutout To...
- **kvnsoufal**'s MidiTransformer 🎼
  - 📘 [Implementation Here](https://github.com/kvsnoufal/MidiTransformer) 
  - 📖 [Medium Article](https://medium.com/mlearning-ai/generating-music-with-gpt-b0f4ab738b58)
&nbsp;  
- The [**BEST GPT Youtube walkthrough**](https://www.youtube.com/watch?v=kCc8FmEb1nY&ab_channel=AndrejKarpathy) by Andrej Karpathy's 📺
&nbsp;  
&nbsp;  
## 📘 Table of Contents
- [🚀 Getting Started](#getting-started)
  - [🔍 Important to know](#important-to-know)
  - [🛠 Requirements](#requirements)
  - [🗂 File Structure](#file-structure)
- [🏋 Training the Model](#training-the-model)
- [🔬 Loading and Running Tests](#loading-and-running-tests) 
&nbsp;  
## 🚀 Getting Started
### 🔍 Important to know!
- 📓 Built for notebook environments: Jupyter, Databricks, and Google-Colab!
- 🎵 MIDI data encodings are thanks to [MidiTok](https://miditok.readthedocs.io/en/latest/index.html). 
  - 🎹 Generate your own dataset with the [RemiPlus](https://miditok.readthedocs.io/en/latest/tokenizations.html#remiplus) tokenizer.
&nbsp;  
### 🛠 Requirements
- 🎹 MidiTok (MIDI file tokenization)
- 🧠 PyTorch (The brain behind model creation, training, and inference)
- 📊 Pandas (For data manipulation)
- 🔢 NumPy (matrices and stuff)
&nbsp;  
#### Don't forget to... 📦:
  ```pip install MidiTok```
&nbsp;  
### 🗂 File Structure

Navigating the repo is as easy as reading sheet music! 🎵
- `output/`: 📁 Your saved outputs (trained model checkpoints).
- `data_plots/`: 📊 Visual charts (training-related plots).
- `encoding/`: 🔢 Encoded midi tracks.
- `preload/`: 🚀 Pre-tuned data structures to speed up dataset loading time.
- `songs/`: 🎶 Freshly composed MIDI songs.
- `logs/`: 📜 log files of the training.
&nbsp;  
&nbsp;  
## 🏋 Training the Model
&nbsp;  
1️⃣ Get things rocking with the `train` function:
   - Orchestrates the training process: from logging, data loading to the grand performance of training a Transformer model.
   - Yourmodel checkpoints are safely stored in the `output/` directory every evaluation interval.  
   
2️⃣ Watch your model learn with the `plot_and_save` function:
   - Visual feedback (loss plots) will be stored in the `data_plots/` directory as the model learns.  
   
3️⃣ Record training details with the `save_training_info` function:
   - Detailed logs and parameters are saved in the `data_plots/` as text documents for your reference.
&nbsp;   
&nbsp;  
## 🔬 Loading and Running Tests
&nbsp;  
1️⃣ Load up a trained model with the `load_model` function:
   - Just point it to your chosen trained model checkpoint in the `output/` directory.  
   
2️⃣ Compose with the AI overlords, generate MIDI songs using the testing loop:
   - Dile things in with an initial MIDI sequence from the `encoding/` directory.
   - Your fresh generated MIDI songs are saved in the `songs/` directory.
   
&nbsp;  
🎻 _Final note:_ Tweak the constants and parameters (like `VOCAB_SIZE`, `EMBED_DIM`, etc.) to your own taste. 🎼
&nbsp;  
