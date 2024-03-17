# BiLSTM for Kannada Named Entity Recognition (NER)

This repository contains code for a BiLSTM (Bidirectional Long Short-Term Memory) model implemented in PyTorch for sequence labeling tasks, particularly named entity recognition (NER), on Kannada language text data.

## Contents:

1. **Code Files:**
    - `bilstm_model.py`: Python script containing the implementation of the BiLSTM model, data preprocessing functions, training loop, evaluation functions, and metric calculation.
    
2. **Data Files:**
    - `DATA/Kannada-train.txt`: Training data in Kannada language for NER task.
    - `DATA/Kannada-validate.txt`: Validation data in Kannada language for NER task.
    
3. **Saved Models:**
    - `bilstm_model.pth`: Trained BiLSTM model saved after training.

4. **Saved Data and Vocabulary Mappings:**
    - `train_X.json`: Processed input data (train features) in JSON format.
    - `train_y.json`: Processed output labels (train targets) in JSON format.
    - `word_to_idx.json`: Mapping of words to numerical indices in JSON format.
    - `tag_to_idx.json`: Mapping of tags to numerical indices in JSON format.

## License

This project is licensed under the [MIT License](LICENSE) - see the [LICENSE](LICENSE) file for details.

The MIT License is a permissive open-source license that allows you to use, modify, and distribute the code with very few restrictions. It also comes with no warranty or liability.

By contributing to this project, you agree to license your contributions under the terms of the [MIT License](LICENSE).

## Instructions to Run:

1. **Environment Setup:**
    - Ensure Python and required libraries (PyTorch, NumPy, scikit-learn, Matplotlib) are installed.

2. **Clone the Repository:**
    ```bash
    git clone https://github.com/Sudharshan14/Kannada-NER.git
    cd your-repo
    ```

3. **Data Preparation:**
    - Make sure training and validation data files (`Kannada-train.txt`, `Kannada-validate.txt`) are in the `DATA` directory.
    
4. **Training:**
    - Run the training script to train the BiLSTM model:
    ```bash
    python bilstm_model.py
    ```

5. **Evaluation:**
    - After training, the script will automatically evaluate the trained model on the validation data.
    - Evaluation metrics (Accuracy, Precision, Recall, F1 Score) will be displayed in the console, and a bar plot showing the metrics will be generated.

6. **Results Interpretation:**
    - Interpret the evaluation results to understand the performance of the model on the validation data.
    - Adjust hyperparameters, model architecture, or preprocessing steps as needed for better performance.

## References:
- [PyTorch Documentation](https://pytorch.org/docs/stable/index.html)
- [scikit-learn Documentation](https://scikit-learn.org/stable/documentation.html)
- [Matplotlib Documentation](https://matplotlib.org/stable/contents.html)

