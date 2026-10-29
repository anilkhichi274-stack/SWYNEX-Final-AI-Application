
# SWYNEX Final AI Application
## AI-Based Customer Feedback Classification

**SWYNEX Technologies — Artificial Intelligence Internship**

**Task 4: Final AI Application**

## 1. Project Overview

This project is a beginner-friendly AI application that classifies customer feedback into three sentiment categories:

- Positive
- Negative
- Neutral

It uses Python and machine learning to help organize customer reviews and identify customer opinions.

The project was developed progressively during the SWYNEX Technologies Artificial Intelligence Internship.

## 2. Problem Statement

Businesses receive customer reviews, complaints, and suggestions regularly.

Manually reading and categorizing large amounts of feedback can be time-consuming.

This project demonstrates how machine learning can help classify customer feedback automatically.

## 3. Project Objectives

- Classify customer feedback into sentiment categories.
- Display predictions with confidence scores.
- Handle empty inputs and dataset errors.
- Evaluate predictions using example feedback.
- Identify ambiguous and potentially incorrect predictions.
- Provide a simple interactive command-line interface.

## 4. Technologies Used

- Python
- Pandas
- Scikit-learn
- TF-IDF Vectorization
- Logistic Regression
- Google Colab
- GitHub

## 5. Methodology

### Step 1: Data Collection

The project uses `customer_feedback.csv`, a small dataset of manually labeled customer feedback.

The dataset contains feedback text and sentiment labels.

### Step 2: Text Processing

TF-IDF Vectorization converts feedback text into numerical features.

The model uses character-level n-grams to represent patterns in the text.

### Step 3: Model Training

Logistic Regression learns patterns from the labeled feedback examples.

### Step 4: Sentiment Prediction

The trained model predicts whether new feedback is Positive, Negative, or Neutral.

### Step 5: Confidence Estimation

The application displays the highest predicted class probability as a confidence score.

This score is an estimate, not a guarantee of correctness.

### Step 6: Model Evaluation

The application compares expected and predicted labels for five demonstration examples.

## 6. Intelligent Features

The final application includes:

1. Sentiment classification
2. Prediction confidence scores
3. Empty-input validation
4. Dataset and training error handling
5. Example-based model evaluation
6. Failure case demonstrations
7. Interactive customer feedback input
8. Low-confidence warnings

## 7. Model Evaluation Results

| Customer Feedback | Expected | Predicted | Result |
|---|---|---|---|
| The product is excellent | Positive | Positive | PASS |
| Very bad customer service | Negative | Negative | PASS |
| The product is okay | Neutral | Neutral | PASS |
| I am very happy with the service | Positive | Negative | FAIL |
| The delivery was terrible | Negative | Negative | PASS |

**Demonstration Result: 4/5 correct predictions (80%).**

This result comes from only five examples and should not be interpreted as real-world model accuracy.

## 8. Working Demo

### Example Input

The service was amazing 3.

### Example Output

AI Prediction: Positive

Confidence Score: 60.96%

### How the Application Works

1. The user enters customer feedback.
2. The application validates the input.
3. The trained model predicts a sentiment.
4. The application displays the predicted label and confidence score.
5. Low-confidence predictions receive a manual-review warning.

The interface runs in a terminal or Google Colab notebook.

## 9. Failure Cases

The following examples demonstrate model limitations:

| Feedback | Model Prediction | Observation |
|---|---|---|
| Great, another delayed delivery! | Positive | Sarcasm may be misunderstood |
| The service was not bad | Negative | Negation may be misunderstood |
| I expected better quality | Negative | Context may require manual review |

Another example:

- Input: I am very happy with the service
- Expected: Positive
- Predicted: Negative

This demonstrates that the model can make incorrect predictions.

## 10. Limitations

- The training dataset is small.
- The model may struggle with sarcasm and negation.
- Predictions may be unreliable for unfamiliar wording.
- Confidence scores are not calibrated guarantees.
- The example evaluation is too small to establish generalization.
- The application is a learning prototype, not a production-ready service.

## 11. Ethics and Responsible AI

### Data Privacy

Real customer feedback may contain personal information. Such information should be removed or protected before training or analysis.

### Bias and Fairness

A small or unbalanced dataset may cause biased predictions. More diverse examples are needed.

### Human Oversight

AI predictions should support human decision-making rather than replace it entirely.

### Transparency

Users should understand that the system can make mistakes and that confidence scores do not guarantee accuracy.

### Responsible Deployment

The model requires further testing, privacy safeguards, and independent evaluation before real-world deployment.

## 12. Repository Files

- `app.py` — Main Python application
- `customer_feedback.csv` — Training dataset
- `SWYNEX_AI_Model_Test.ipynb` — Initial model testing notebook
- `SWYNEX_Task_3_Intelligent_Feature.ipynb` — Intelligent feature and evaluation notebook
- `README.md` — Final project documentation

## 13. How to Run the Application

### Option 1: Run Locally

1. Download or clone the repository.
2. Install Python.
3. Install dependencies:

```bash
pip install pandas scikit-learn
```

4. Keep `app.py` and `customer_feedback.csv` in the same directory.
5. Run:

```bash
python app.py
```

6. Enter customer feedback when prompted.
7. Type `exit` to close the application.

### Option 2: Google Colab

1. Open `SWYNEX_Task_3_Intelligent_Feature.ipynb` in Google Colab.
2. Upload `customer_feedback.csv` to the Colab session.
3. Run the notebook cells.
4. Review the model evaluation and interactive predictions.

## 14. Future Improvements

- Collect a larger and more diverse dataset.
- Use separate training and test datasets.
- Evaluate precision, recall, and F1-score.
- Improve sarcasm and negation handling.
- Add a simple web interface.
- Test and calibrate confidence scores.

## 15. Conclusion

This project demonstrates a complete beginner-level machine learning workflow, from dataset preparation and model training to sentiment prediction, evaluation, error handling, and interactive testing.

It also documents limitations and responsible AI considerations.

**Developed for SWYNEX Technologies — Artificial Intelligence Internship, Task 4: Final AI Application.**
