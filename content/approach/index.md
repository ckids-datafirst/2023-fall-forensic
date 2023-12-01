---
title: Approach
summary: Data science methodology used to address the problem, including data preprocessing steps, exploratory data analysis, feature engineering techniques, machine learning models, and evaluation metrics.
date: "2018-06-28T00:00:00Z"
editable: true
share: false
---

This page serves as a pivotal component of the **Final Report**, outlining the data science methodology employed to tackle the project's challenges. It combines insights from the Requirements document and evolves as the project advances and a deeper understanding of the problem is attained.

## Data Preprocessing

In the data preprocessing phase, we focused on refining the raw data for model training. The "question" column (T), representing the questions used for model training, was prioritized. Simultaneously, lines marked with "1" in the "excluded" column (V) were omitted as they fell beyond the project's scope. Additionally, attention was given to the "updatedQT" column (X), containing human-coded question codes (0, 1, 2, 3). These essential steps ensured the dataset's relevance and alignment with project objectives, paving the way for effective model training and subsequent analysis of automated question type coding.

## Exploratory Data Analysis (EDA)

In our Exploratory Data Analysis (EDA), we utilized bar graphs to visually represent the distribution of four question types: Non-questions, Option-posing questions, Invitations, and Directives. This approach provided insightful insights into the dataset's composition, aiding in identifying patterns and trends. The visualizations during EDA served as a foundational step for subsequent model development, fine-tuning, and the goal of accurate automated question type coding.

![Question Type](https://github.com/ckids-datafirst/2023-fall-forensic/blob/main/assets/media/question%20types.png?raw=true)

## Model Development

For model development, we leveraged the RoBERTa architecture from Hugging Face as our pre-trained model, chosen for its state-of-the-art natural language processing capabilities. The fine-tuning process involved refining the model using an oversampled dataset, a strategic approach to address the challenge of low invitation frequency. This methodology ensured the model's adaptability to the nuances of diverse question types, enhancing its performance in automated question type coding. The selection of RoBERTa and the fine-tuning on the oversampled dataset align with our goal of achieving a high-quality, specialized model for accurate and nuanced classification in forensic interviews and court transcripts analysis.

## Model Evaluation

In evaluating our automated question type coding model, we utilized a robust set of metrics, including the confusion matrix and F1 accuracy scores. These metrics, chosen for their ability to comprehensively assess the model's performance, were instrumental in addressing the intricate challenge of distinguishing question types. The results showcased a high level of human-machine agreement, with accuracies of 82% for non-questions, 82% for option-posing questions, an impressive 98% for wh-questions, and a notable 96% for invitations. This strategic choice of evaluation techniques ensured a thorough understanding of the model's proficiency, guarding against undesirable behaviors like overfitting.
