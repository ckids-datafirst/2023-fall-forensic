---
title: Approach
summary: Data science methodology used to address the problem, including data preprocessing steps, exploratory data analysis, feature engineering techniques, machine learning models, and evaluation metrics.
date: "2018-06-28T00:00:00Z"
editable: true
share: false
---

This page contains key sections of the **Final Report** for the project focused on the data science methodology used to approach the problem.  It should be no more than 3 pages long.  It should be done after or in combination with the Requirements document.  It should have an initial release after no more than eight weeks into the project, and can serve as an interim project report.  It can be refined as the project progresses and the problem is better understood.  

## Data Quality

Describe any steps that were used to address any issues concerning the quality of the data.  This may include collecting data quality metrics, discarding subsets of the data, or applying specific techniques for handling missing values, dealing with outliers, etc. 

## Data Preprocessing

Describe the steps taken to preprocess the raw data to prepare it for analysis. This may include data transformations to convert to a required format, feature engineering operations, encoding features as binary, etc.

## Exploratory Data Analysis (EDA)

In our Exploratory Data Analysis (EDA), we utilized bar graphs to visually represent the distribution of four question types: Non-questions, Option-posing questions, Invitations, and Directives. This approach provided insightful insights into the dataset's composition, aiding in identifying patterns and trends. The visualizations during EDA served as a foundational step for subsequent model development, fine-tuning, and the goal of accurate automated question type coding.

![Question Type](https://github.com/ckids-datafirst/2023-fall-forensic/blob/main/assets/media/question%20types.png?raw=true)

## Model Development

For model development, we leveraged the RoBERTa architecture from Hugging Face as our pre-trained model, chosen for its state-of-the-art natural language processing capabilities. The fine-tuning process involved refining the model using an oversampled dataset, a strategic approach to address the challenge of low invitation frequency. This methodology ensured the model's adaptability to the nuances of diverse question types, enhancing its performance in automated question type coding. The selection of RoBERTa and the fine-tuning on the oversampled dataset align with our goal of achieving a high-quality, specialized model for accurate and nuanced classification in forensic interviews and court transcripts analysis.

## Model Evaluation

In evaluating our automated question type coding model, we utilized a robust set of metrics, including the confusion matrix and F1 accuracy scores. These metrics, chosen for their ability to comprehensively assess the model's performance, were instrumental in addressing the intricate challenge of distinguishing question types. The results showcased a high level of human-machine agreement, with accuracies of 82% for non-questions, 82% for option-posing questions, an impressive 98% for wh-questions, and a notable 96% for invitations. This strategic choice of evaluation techniques ensured a thorough understanding of the model's proficiency, guarding against undesirable behaviors like overfitting.
