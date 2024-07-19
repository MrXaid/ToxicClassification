# ToxicClassification: ️ Detecting Comment Toxicity with Deep Learning 💀💔☠️

![ChatWithDocs Demo](/demotest.png)

Safeguard online communities by identifying potentially harmful or toxic comments with this powerful comment toxicity detection system. This project leverages deep learning to analyze comments 
and determine their toxicity level.

## Features 🌟

**Multi-Class Toxicity Detection**: Classifies comments into various toxicity categories, going beyond just "toxic" or "not toxic."
**Deep Learning Power**: Employs a Bidirectional LSTM (Long Short-Term Memory) architecture, capturing both forward and backward contextual dependencies in comments.
**Customizable and Scalable**: The code is designed to be easily adaptable to different datasets and toxicity categories.


## Technologies Used 🛠️

- [TensorFlow](https://www.tensorflow.org/): For building and loading the deep learning model
- [Keras](https://keras.io/): High-level neural network API
- [NumPy](https://numpy.org/): For efficient numerical computations
- [Matplotlib]: For plotting graphs for accurace
  

## Installation 🚀

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/EmoClassification.git
   cd EmoClassification
   ```

2. Install the required dependencies:
   ```bash
   pip install tensorflow pandas matplotlib scikit-learn
   ```


## Usage 🖥️

To use the pre-trained model for emotion classification, follow these steps:

1.) Prepare your comment data (preprocessing may be required).
2.) Load the pre-trained model (instructions provided in the code).
3.) Pass your comments to the model for toxicity classification.


## Model Architecture:

  ```python
  from tensorflow.keras.layers import Embedding, Bidirectional, LSTM, Dense

  MAX_FEATURES = ...  # Maximum number of words in the vocabulary
I  NPUT_LENGTH = ...  # Maximum length of a comment

  model = Sequential([
    Embedding(MAX_FEATURES + 1, 32, input_length=INPUT_LENGTH),
    Bidirectional(LSTM(32, activation='tanh')),
    Dense(128, activation='relu'),
    Dense(256, activation='relu'),
    Dense(128, activation='relu'),
    Dense(6, activation='sigmoid')  # Adjust the output layer size for your toxicity categories
  ])
   ```
## Contributing 🤝

Contributions are welcome! Please feel free to submit a Pull Request.
