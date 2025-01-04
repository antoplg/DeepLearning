# SENTENCE RECONSTRUCTION via DEEP LEARNING 


## Project Overview

The project aims to reconstruct the original sentence from a sequence of randomly permuted words of an English sentence.

### Key Features and Constraints:
Input: A sequence of words corresponding to a random permutation of a given English sentence.

Output: The original sentence, reconstructed either:

- In a single step.

- Iteratively (autoregressive), generating one token at a time.

No pre-trained models can be used.

Neural network models must have fewer than 20 million parameters.

No post-processing techniques like beam search are allowed.

Additional training data cannot be used.

### Dataset:
Sentences are taken from the generics_kb dataset from Hugging Face.

The vocabulary is restricted to the 10,000 most frequent words.

Only sentences using this vocabulary are included.

### Model Architecture

The neural network architecture was designed to be both innovative and efficient, meeting the constraint of having fewer than 20 million parameters. A text vectorization layer processed raw text into numerical sequences, restricting the vocabulary to the 10,000 most frequent words. The model itself employed a Transformer-based architecture, which is well-suited for handling sequential data like sentences. To enhance efficiency, the model incorporated embedding layers, LSTM layers for sequential processing, and a final dense layer to generate predictions. This modular design allowed the model to effectively capture the nuances of word order while maintaining a lightweight structure.

### Training Process

Training the model involved several carefully chosen techniques. The categorical crossentropy loss function was used to measure the accuracy of predictions, while the Adam optimizer ensured efficient updates to the model's parameters during training. The dataset was divided into batches to optimize memory usage, and a portion of it was reserved for validation to monitor the model's performance over time. Through this rigorous training process, the model learned to reconstruct sentences from permuted inputs, adhering to the constraints imposed by the project guidelines.

### Evaluation

Evaluation metrics for the project included accuracy, parameter efficiency, and qualitative analysis of reconstructed sentences. The model's ability to generate coherent sentences demonstrated its effectiveness, although challenges emerged with longer and more complex sentences. The absence of postprocessing techniques meant that the model's outputs were entirely raw, which occasionally led to minor inaccuracies.

### Conclusion

In conclusion, this project represents a thoughtful and innovative approach to solving the problem of sentence reconstruction within strict academic constraints. By designing efficient neural networks tailored to the task, Antonio Rapallini has demonstrated a deep understanding of deep learning principles and their practical applications. The work sets a solid foundation for further exploration in the field of low-resource neural language processing, offering valuable insights for future research and development.

