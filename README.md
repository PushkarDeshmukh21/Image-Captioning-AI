# Image-Captioning-AI
AI model than can generate captions for image.

Training Datasett :- Flickr8K
Dataset taken from Kaggle : https://www.kaggle.com/datasets/adityajn105/flickr8k

**Steps to build the model :**
1. **Dataset Preparation :** The Flickr8K dataset is used, consisting of 8,000 images and five captions per image.
   Images and captions are loaded, and text is tokenized to create a vocabulary of words.
2. **Feature Extraction with CNN :** Features are extracted from images using the VGG16 model, pre-trained on ImageNet.
   The classification layers of VGG16 are removed to retain only the convolutional base.
3. **Caption Preprocessing :** Captions are converted into a format suitable for input to the RNN model. This involves
   creating sequences of words and numerical representations.

**Model Architecture**
The model integrates a CNN (encoder) and an RNN (decoder) to generate captions.
Components:
o Encoder: The VGG16 model extracts visual features from images.
o Decoder: An LSTM-based RNN generates textual sequences from the encoded
  features.
o Combine image features and text embeddings as inputs to the decoder.
