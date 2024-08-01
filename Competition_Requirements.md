# ISIC-2024---Skin-Cancer-Detection-with-3D-TBP
Image-based algorithms to identify histologically confirmed skin cancer cases with single-lesion crops from 3D total body photos (TBP)

 
## Overview
In this competition, you'll develop image-based algorithms to identify histologically confirmed skin cancer cases with single-lesion crops from 3D total body photos (TBP). The image quality resembles close-up smartphone photos, which are regularly submitted for telehealth purposes. Your binary classification algorithm could be used in settings without access to specialized care and improve triage for early skin cancer detection.

## Description
Skin cancer can be deadly if not caught early, but many populations lack specialized dermatologic care. Over the past several years, dermoscopy-based AI algorithms have been shown to benefit clinicians in diagnosing melanoma, basal cell, and squamous cell carcinoma. However, determining which individuals should see a clinician in the first place has great potential impact. Triaging applications have a significant potential to benefit underserved populations and improve early skin cancer detection, the key factor in long-term patient outcomes.

Dermatoscope images reveal morphologic features not visible to the naked eye, but these images are typically only captured in dermatology clinics. Algorithms that benefit people in primary care or non-clinical settings must be adept to evaluating lower quality images. This competition leverages 3D TBP to present a novel dataset of every single lesion from thousands of patients across three continents with images resembling cell phone photos.

This competition challenges you to develop AI algorithms that differentiate histologically-confirmed malignant skin lesions from benign lesions on a patient. Your work will help to improve early diagnosis and disease prognosis by extending the benefits of automated skin cancer detection to a broader population and settings.

## Evaluation
Primary Scoring Metric
Submissions are evaluated on partial area under the ROC curve (pAUC) above 80% true positive rate (TPR) for binary classification of malignant examples. (See the implementation in the notebook ISIC pAUC-aboveTPR.)

The receiver operating characteristic (ROC) curve illustrates the diagnostic ability of a given binary classifier system as its discrimination threshold is varied. However, there are regions in the ROC space where the values of TPR are unacceptable in clinical practice. Systems that aid in diagnosing cancers are required to be highly-sensitive, so this metric focuses on the area under the ROC curve AND above 80% TRP. Hence, scores range from [0.0, 0.2].

The shaded regions in the following example represents the pAUC of two arbitrary algorithms (Ca and Cb) at an arbitrary minimum TPR:

![Gráfico_1](https://www.googleapis.com/download/storage/v1/b/kaggle-user-content/o/inbox%2F4972760%2Ff9089439a6256c84a1d98a83910a46a0%2FJiang.png?generation=1717599679915410&alt=media)

## Submission File
For each image (isic_id) in the test set, you must predict the probability (target) that the lesion is malignant. The file should contain a header and have the following format:

isic_id,              target
ISIC_0015657,         0.7
ISIC_0015729,         0.9
ISIC_0015740,         0.8
etc.


## Code Requirements
This is a Code Competition
Submissions to this competition must be made through Notebooks. In order for the "Submit" button to be active after a commit, the following conditions must be met:

CPU Notebook <= 12 hours run-time
GPU Notebook <= 12 hours run-time
Internet access disabled
Freely & publicly available external data is allowed, including pre-trained models
Submission file must be named submission.csv
Please see the Code Competition FAQ for more information on how to submit. And review the code debugging doc if you are encountering submission errors.
