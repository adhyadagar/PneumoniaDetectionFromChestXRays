# PneumoniaDetectionFromChestXRays

# Part 1: Background

# Part 2: Aim
- To analyze data from the NIH Chest X-ray Dataset and train a CNN to classify a given chest x-ray for the presence or absence of pneumonia.
- Prepare a report to describe the model, the data that it was trained on, and a validation plan for submission to the FDA for 510(k) clearance as software as a medical device.

# Part 3: Data
- Data is from the NIH Chest X-ray Dataset and consists of 112,000 chest x-rays with disease labels acquired from 30,000 patients.
- It is also available on https://www.kaggle.com/nih-chest-xrays/data
- The biggest limitation of this dataset is that image labels were NLP-extracted so there could be some erroneous labels but the NLP labeling accuracy is estimated to be >90%.

# Part 4: Methodology
- Recommend appropriate imaging modalities for common clinical applications of 2D medical imaging
- Perform exploratory data analysis (EDA) on medical imaging data to inform model training and explain model performance
- Establish the appropriate ‘ground truth’ methodologies for training algorithms to label medical images
- Extract images from a DICOM dataset
- Train common CNN architectures to classify 2D medical images
- Translate outputs of medical imaging models for use by a clinician
- Plan necessary validations to prepare a medical imaging model for regulatory approval

# Part 5: Evaluation Metrics 


# Part 6: Conclusion and Results


# This project includes the following files- 
 1. EDA.ipynb: Script for performing EDA.
 2. Build and train model.ipynb: Script for building and training your model.
 3. Inference.ipynb: Script for performing clinical workflow integration.
 4. .dcm files: They are the test files to test the clinical workflow integration.
 5. sample_labels.csv: This is the file to assess images in the pixel-level.
 6. FDA_Submission.pdf: Report for FDA clearance 

## Content of Inference.ipynb:

## Clinical Workflow Integration
 The imaging data for training the model was transformed from DICOM format into .png to help aid in the image pre-processing and model training steps of this project. In the real world, however, the pixel-level imaging data are contained inside of standard DICOM files.
 In this notebook I have creayed a DICOM wrapper that takes in a standard DICOM file and outputs data in the format accepted by the model. 
 The following checks are also included in the wrapper-
- Age
- Image acquisition type (i.e. X-ray)
- Image acquisition orientation (i.e. those present in your training data)
- Body part in acquisition

# FDA Submission
For this project, you will complete the following steps that are derived from the FDA's official guidance on both the algorithm description and the algorithm performance assessment. Much of this portion of the project relies on what you did during your EDA, model building, and model training. Use figures and statistics from those earlier parts in completing the following documentation.

 1. General Information:

 First, provide an Intended Use statement for your model
 Then, provide some indications for use that should include:
 Target population
 When your device could be utilized within a clinical workflow
 Device limitations, including diseases/conditions/abnormalities for which the device has been found ineffective and should not be used
 Explain how a false positive or false negative might impact a patient
 2. Algorithm Design and Function

 Describing fully trained algorithm and the DICOM header and including a flowchart to describe the following:

 - Pre-algorithm checks you perform on your DICOM
 - Preprocessing steps performed by your algorithm on the original images (e.g. normalization) (Augmentation is not included)
 - The architecture of the classifier
 - For each stage of your algorithm, the design and function.

 3. Algorithm Training

 Describe the following parameters of your algorithm and how they were chosen:

  Types of augmentation used during training
  Batch size
  Optimizer learning rate
  Layers of pre-existing architecture that were frozen
  Layers of pre-existing architecture that were fine-tuned
  Layers added to pre-existing architecture
  Also describe the behavior of the following throughout training (use visuals to show):

  Training loss
  Validation loss
  Describe the algorithm's final performance after training was complete by showing a precision-recall curve on your validation set.

  Finally, report the threshold for classification that you chose and the corresponded F1 score, recall, and precision. Give one or two sentences of explanation for why you chose this threshold value.

  4. Databases

  For the database of patient data used, provide specific information about the training and validation datasets that you curated separately, including:

  Size of the dataset
  The number of positive cases and the its radio to the number of negative cases
  The patient demographic data (as it is available)
  The radiologic techniques used and views taken
  The co-occurrence frequencies of pneumonia with other diseases and findings
  5. Ground Truth

  The methodology used to establish the ground truth can impact reported performance. Describe how the NIH created the ground truth for the data that was provided to you for this project. Describe the benefits and limitations of this type of ground truth.

  6. FDA Validation Plan

  You will simply describe how a FDA Validation Plan would be conducted for your algorithm, rather than actually performing the assessment. Describe the following:

  The patient population that you would request imaging data from from your clinical partner. Make sure to include:

  Age ranges
  Sex
  Type of imaging modality
  Body part imaged
  Prevalence of disease of interest
  Any other diseases that should be included or excluded as comorbidities in the population
  Provide a short explanation of how you would obtain an optimal ground truth
