# mbti_personality_prediction

MBTI Personality Prediction Project
Overview
This project aims to predict MBTI personality types from text data using machine learning techniques. We explored several methods, including training a model on existing datasets, applying transfer learning, and leveraging pseudo-labels for improved performance.

Objectives
Train a Personality Prediction Model: Train an XGBoost model on datasets with known MBTI labels (MBTI and Personality Cafe forums).
Evaluate Model Generalizability: Assess the model’s ability to generalize to new, unlabeled datasets, specifically the Ubuntu Dialog Corpus.
Use ChatGPT for Pseudo-Labeling: Utilize ChatGPT to simulate MBTI labeling on the Ubuntu Dialog Corpus to evaluate the model’s performance indirectly.
Methodology
Data Preparation
Training Data: The XGBoost model was trained on MBTI and Personality Cafe forum datasets, which provided ground truth labels for various MBTI personality types.
Test Data: The Ubuntu Dialog Corpus, which lacks ground truth labels, was used to evaluate the model's generalizability.
Model Training
XGBoost Model: An XGBoost model was trained on labeled MBTI data to predict personality types. The model achieved a 65% accuracy rate on the training data.
Transfer Learning: The pre-trained XGBoost model was applied to the Ubuntu Dialog Corpus to predict personality types, leveraging its learned patterns to handle new, unlabeled data.
Pseudo-Labeling with ChatGPT
ChatGPT Labeling: To simulate MBTI labels for the Ubuntu Dialog Corpus, ChatGPT was used to categorize texts based on MBTI-related questions. This allowed for the creation of pseudo-labels for the test data.
Sample Evaluation: A subset of 15 texts was manually labeled by ChatGPT, and these pseudo-labels were compared with the predictions made by the XGBoost model.
Results
Accuracy: The XGBoost model provided predictions for the Ubuntu Dialog Corpus, but exact MBTI type matches were rare (13% accuracy). However, many predictions shared 2 or 3 dichotomies, indicating that the model identified similar personality traits across texts.
Dichotomy Similarity: On average, the similarity between XGBoost and ChatGPT predictions was 70%, reflecting that the models identified many shared characteristics despite differences in overall personality type predictions.
Conclusions
The project demonstrated the effectiveness of using pre-trained models and pseudo-labels to handle unlabeled data. Although exact MBTI type matches were infrequent, the models showed a significant degree of alignment in personality dichotomies, suggesting that they capture similar underlying traits. The use of ChatGPT for pseudo-labeling provided valuable insights into the model’s performance and highlighted the potential of combining multiple approaches for personality prediction.

Future Work
Refine Pseudo-Labeling: Improve the accuracy and reliability of pseudo-labels by experimenting with different labeling strategies and models.
Expand Datasets: Incorporate additional datasets and refine the model to enhance its generalizability and performance.
Detailed Evaluation: Conduct more comprehensive evaluations of the model’s predictions, focusing on both exact matches and dichotomy similarities.
