# Email-Phishing-Detector

## Overview
This project aims to detect and classify confidential user requests using machine learning. By training a model to differentiate between "normal" and "blocked" requests, the system can prevent unauthorized access to sensitive information. The approach involves text preprocessing, feature extraction, and model evaluation.

## Dataset Description
The dataset contains various features designed to help the model identify potentially confidential requests:

- **Request**: User's input text.
- **Keyword_Count**: Number of sensitive keywords detected in the request.
- **Pattern_Match**: Boolean indicating whether specific patterns associated with confidential data were matched (1 for match, 0 for no match).
- **Contextual_Flag**: Indicates whether the request was flagged based on contextual sensitivity (1 for flagged, 0 otherwise).
- **Label**: Original classification of the request ("normal" or "blocked").
- **Label_Binary**: Binary encoding of the label (0 = "normal", 1 = "blocked").

## Model Training and Evaluation

### Steps Involved:
1. **Text Preprocessing**: Lowercasing and removing punctuation from requests.
2. **Feature Extraction**: Using TF-IDF to convert requests into numerical vectors.
3. **Model Training**: Logistic Regression model trained on an 80/20 data split for improved generalization.
4. **Evaluation Metrics**: Accuracy, precision, recall, F1-score, and confusion matrix are used to assess model performance.
5. **Cross-Validation**: Ensures model reliability with consistent performance across different data splits.

## How to Use

1. **Prepare Data**: Preprocess the requests by removing unnecessary characters and extracting features.
2. **Train the Model**: Use the preprocessed data to train a Logistic Regression classifier.
3. **Evaluate Performance**: Analyze performance using confusion matrices and classification reports.
4. **Test New Requests**: Predict whether new requests should be classified as "normal" or "blocked".

## Results Summary
The Logistic Regression model achieved the following results:
- **Accuracy**: 100%
- **Precision**: 100%
- **Recall**: 100%
- **F1-Score**: 100%
- Cross-validation scores: [1.0, 1.0, 1.0, 1.0, 1.0]

These results indicate a highly accurate model, capable of consistently detecting confidential requests.

## Future Enhancements
Potential improvements could include:
- **Exploring Other Models**: Random Forest, LSTM, or hybrid models for comparison.
- **Data Augmentation**: Expanding dataset diversity for better generalization.
- **Real-Time Deployment**: Implementing the model for real-time request monitoring.

## Dataset available for download
