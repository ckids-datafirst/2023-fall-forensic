---
title: Problem and Requirements
summary: Problem and Requirements document that will drive the work to be done in the project
date: "2018-06-28T00:00:00Z"
editable: true
share: false
---

## Introduction
In the realm of forensic interviewing research, the meticulous process of question type coding plays a pivotal role in distinguishing best practice open-ended questions from the undesirable closed-ended and leading questions that interviewers are trained to avoid. Traditionally, research teams have grappled with a time-consuming and labor-intensive approach to question type coding, wherein each question in an interview is manually coded by a researcher, with a subset subjected to a second researcher's coding to demonstrate inter-rater reliability.

In response to this challenge, our team has embarked on an innovative initiative by harnessing the capabilities of a large language model, specifically RoBERTa, to discern question types based on a rudimentary classification system. This approach not only promises efficiency gains but also marks a departure from the reliance on mock interviews, as our model has been trained on a substantial dataset comprising 349,033 real forensic interview questions.

As we advance into the next phase of our project, our focus shifts towards fine-tuning the model and employing zero-shot and few-shot prompting techniques to make distinctions where there is limited manually-coded data. This research stands at the forefront of leveraging automated coding to provide swift and straightforward measures of testimonial quality, contributing to a nuanced understanding of interview dynamics in the field.

## Motivation
Question type coding is integral to evaluating interview quality, a concept extensively discussed by Lamb et al. in their 2018 study. The preferred measure for assessing interview quality emphasizes the significance of employing broad, open-ended questions like "Tell me everything that happened," as they effectively elicit comprehensive details while minimizing the risk of misinformation. Wh-questions, such as "Where was your mom?" are considered more favorable compared to option-posing questions like "Did you run away?" which interviewers are trained to avoid. Despite its crucial role, the current manual approach to question-type coding is both time-consuming and labor-intensive.

The introduction of automated coding represents a significant advancement, offering forensic interviewers and attorneys a swift means of obtaining measures of interview quality. This transition is particularly noteworthy given the traditional manual nature of the process. Earlier research in this field relied on mock transcripts, utilizing adults as child witnesses to train models. However, the human-machine reliability of these automated systems has yielded mixed results, indicating the ongoing need for refinement and further exploration to enhance the efficiency and accuracy of automated question-type coding systems.

## Problem for the Semester

Our team's initial model successfully discriminated among three question types: non-questions (e.g., "Please sit down."), option-posing questions involving yes/no and forced choice, and invitations & directives, which encompass broad narrative prompts, wh- and how questions. The current project focuses on advancing the model to include a fourth type, specifically targeting the distinction between invitations and directives. The preference for invitations stems from their broader nature, facilitating the extraction of more extensive narrative information. However, a significant challenge lies in the comparatively infrequent use of invitations, especially in legal contexts, resulting in an uneven distribution of question types.

## Design and Approach

To address the issue of data imbalance, we implemented a proactive strategy involving the oversampling of invitation examples to prevent potential bias within our dataset. This deliberate approach aimed to ensure the model receives ample exposure to instances of invitations, compensating for their relatively lower frequency. Furthermore, we prioritized the robust training of our model by incorporating a diverse dataset, covering a wide array of scenarios and contexts to enhance its overall adaptability. When it came to model selection and fine-tuning, we chose to employ RoBERTa from Hugging Face as the pre-trained model, capitalizing on its advanced features. The subsequent fine-tuning process focused on optimizing the model's performance using the oversampled dataset, aligning it more closely with the subtleties of invitation-based questions.

## Desired Outcomes and Benefits

The implementation of automated coding in the field of forensic interviews holds the promise of significantly enhancing efficiency and expediting processes for interviewers, attorneys, and expert witnesses. By automating the coding of question types, valuable time and resources can be saved, allowing these professionals to focus more on the substantive aspects of their work. 

The envisioned outcomes include streamlined workflows during interviews and legal proceedings, reducing the manual labor associated with question type coding. Moreover, the incorporation of transcription services into the automated system adds an additional layer of convenience, enabling quick and accurate documentation of interviews. Furthermore, the development of an instant feedback system promises to provide timely insights into interview quality, empowering practitioners to make real-time adjustments and improvements.

Overall, the integration of automated coding, transcription, and instant feedback systems represents a transformative step towards enhancing the effectiveness and efficiency of forensic interview processes.
