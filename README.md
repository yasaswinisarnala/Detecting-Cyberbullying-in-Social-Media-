# Detecting-Cyberbullying-in-Social-Media-
An NLP-Based Classification Framework 
## Overview
This project introduces an automated, high-accuracy Natural Language Processing (NLP) framework designed to classify social media posts into Cyberbullying or Non-Cyberbullying categories. Developed by a team of authors (Yasaswini, Jashwitha, Naveen Kumar, and Sandeep), the project addresses the growing threat of online toxicity by replacing inefficient manual moderation with a scalable, automated solution.

## Key Technical Challenges & Core Innovations

### Class Imbalance
- In real-world toxicity datasets, cyberbullying posts represent a small minority (in this dataset, safe posts comprised 65% while cyberbullying made up 35%).
- Conventional models often become biased toward the majority class under these conditions.

### High-Dimensional Feature Spaces
- Text analysis naturally creates massive, complex feature vectors that demand high-performance classifiers.

## Solutions

### Modified TF-IDF (MTF-IDF)
- Instead of standard Term Frequency-Inverse Document Frequency, the authors engineered a modified version that assigns disproportionately higher weights to rare, toxic keywords.
- This amplifies the signal of bullying phrases and balances out the data disparity.

### Support Vector Machine (SVM)
- The extracted features are fed into an SVM classifier, chosen for its exceptional ability to manage high-dimensional spaces by finding the optimal separating hyperplane between classes.

## Architecture, Tools, and Technologies
| Layer       | Technologies Used              | Purpose                        |
|-------------|--------------------------------|--------------------------------|
| Frontend    | React, Tailwind CSS, Chart.js  | Interactive UI & charts        |
| Backend     | Python, Flask, Flask-CORS      | REST API & server logic        |
| ML/NLP Core | Scikit-learn, NLTK             | Preprocessing & classification |

## Results & Performance
The proposed MTF-IDF-SVM framework was benchmarked against three industry-standard baselines: Naive Bayes, Random Forest, and Logistic Regression. The proposed model significantly outperformed the competition, achieving the following metrics:

- Accuracy: 97.10% (Overall correctness)
- Precision: 98.05% (Crucial for minimizing false positives, i.e., incorrectly flagging safe content)
- Recall: 96.50% (Ensures the model successfully catches nearly all actual instances of cyberbullying)
- F1-Score: 97.23% (The harmonic mean, confirming a highly robust and balanced model)

## Conclusion & Future Scope
The pairing of MTF-IDF and SVM successfully yields a highly reliable tool immediately applicable for real-time content moderation. Moving forward, the authors identify several areas for future development, including:
- Upgrading the framework to Deep Learning architectures (such as BERT or LSTM networks) to better catch sarcasm.
- Extending the system to support multi-lingual analysis.
- Integrating a sentiment analysis layer to score the severity of negative content rather than just utilizing binary classification.
