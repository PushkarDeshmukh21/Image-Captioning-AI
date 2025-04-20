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

**Model Architecture :**
1. The model integrates a CNN (encoder) and an RNN (decoder) to generate captions.
2. **Components:**
   1. Encoder: The VGG16 model extracts visual features from images.
   2. Decoder: An LSTM-based RNN generates textual sequences from the encoded features.
   3. Combine image features and text embeddings as inputs to the decoder.

**Model Training :**
1. The model is trained using the prepared dataset with supervised learning. The loss function and optimizer are chosen to ensure effective learning.
2. Steps:
   1. Use categorical cross-entropy as the loss function to predict the next word in the sequence.
   2. Optimize the model using the Adam optimizer with learning rate adjustments.
   3. Apply teacher forcing during training, feeding the actual next word as input to the model.
