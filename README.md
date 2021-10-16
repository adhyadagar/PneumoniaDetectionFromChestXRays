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

