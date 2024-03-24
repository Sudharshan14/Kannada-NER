# KA-NER: A Kannada Named Entity Recognition Dataset
This repository contains manually annotated kannada dataset that has been carefully assembled from various sources, such as Wikipedia, blogs, newspapers, and publications.Data Extraction involved systematically retrieving text passages, for which we utilized web scraping techniques, ensuring adherence to copyright and fair use policies.

In the annotation scheme used for labeling named entities in Kannada text, we employed a systematic approach to identify and classify different types of named entities. This section provides a detailed description of the annotation scheme, including the tags utilized for labeling named entities.
Named Entity Tags We utilized the following named entity tags for annotating named entities in Kannada text:

• B-PER: Beginning of a person’s name

• I-PER: Inside a person’s name

• B-LOC: Beginning of a location name

• I-LOC: Inside a location name

• B-ORG: Beginning of an organization name

• I-ORG: Inside an organization name

• B-TME: Beginning of a time

• B-EVT: Beginning of an event

• I-EVT: Inside an event

• O: Tokens that do not belong to any named entity

In the initial phase of annotation, the corpus obtained from online resources underwent manual tagging with named entity tags. Thisprocess involved identifying and marking specific tokens within the text representing named entities such as names of persons,locations, organizations, time, and events. Each named entity tag provided information about the type and position of the named entity within the text. Subsequently, following the named entity tagging phase, each token in the annotated dataset was further tagged using the Begin, Inside, Outside (BIO) tagging scheme.This step facilitated the precise delineation of named entities by indicating the position of each token relative to the named entity boundaries. Tokens tagged with ’B’ indicated the beginning of a named entity, ’I’ indicated inside a named entity, and ’O’ indicated tokens that did not belong to any named entity.
## Dataset :
The datasets can be downloaded using the following https://uwin365-my.sharepoint.com/:f:/g/personal/shantha2_uwindsor_ca/EroMtdS7QWZEomoMhvWV8pwBJL7HDnXgKfG02d73lHwRuQ?e=pN5aIL

## Evalution:
For the evaluation of the dataset we have used the BiLSTM model and compaired with KNERC(D. Sathyanarayanan, A. Ashok, D. Mishra, S. Chimalamarri and D. Sitaram, "Kannada Named Entity Recognition and Classification using Bidirectional Long Short-Term Memory Networks," 2018)
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

