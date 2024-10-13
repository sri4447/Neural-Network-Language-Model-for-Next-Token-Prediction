# Neural-Network-Language-Model-for-Next-Token-Prediction

# Overview
This project implements a next-token prediction model using an LSTM-based neural network. The model can generate text in English and another assigned language, trained using a corpus of sequential data. It leverages the GPT-2 tokenizer for encoding and decoding text.

# Setup
1) Install Dependencies:
   <pre>
     pip install torch transformers matplotlib pandas
   </pre>
2) Run the Model:
   Make sure your text file is correctly placed (e.g., input1.txt in /content/sample_data). Update the path as needed in the code.

# Usage
 1. Train the Model

    The training loop processes a given text corpus, logs the training and validation loss, and saves performance metrics.
     Adjust hyperparameters such as:
      - Embedding dimension: 128
      - LSTM hidden units: 256
      - Learning rate: 0.001
      - Epochs: 5

 2. Generate Text

    Run the generate_sequence() function with a prompt. Example:
    <pre>
      start_text_english = "The journey begins"
      start_text_other_language = "Por favor, deme tres consejos"
    </pre>

    Expected output:
    <pre>
      Generated English Text:
         The journey begins with the first step...

      Generated Other Language Text:
          Por favor, deme tres consejos para mejorar...

    </pre>

3. Model Explanation:
   
   - Training Loss: Measures the error between the model’s predictions and ground truth on the training dataset.
   
   - Validation Loss: Evaluates the model's performance on unseen data to detect overfitting. If validation loss increases while training loss 
       decreases, it could indicate overfitting.

4. Results and Observations:

    - Training and validation loss graphs: Visualize how well the model generalizes.
    - Generated Text: Demonstrates the model’s ability to predict meaningful sequences in both languages.
  
5. Future Improvements:

   - More Epochs: Improve performance with longer training.
   - Hyperparameter Tuning: Explore different values for hidden units, learning rates, and layers.
   


