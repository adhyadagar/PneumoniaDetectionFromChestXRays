# PneumoniaDetectionFromChestXRays

# Part 1: Background

# Part 2: Aim
- To analyze data from the NIH Chest X-ray Dataset and train a CNN to classify a given chest x-ray for the presence or absence of pneumonia.
- Prepare a report to describe the model, the data that it was trained on, and a validation plan for submission to the FDA for 510(k) clearance as software as a medical device.

# Part 3: Data
- Data is from the NIH Chest X-ray Dataset and consists of 112,000 chest x-rays with disease labels acquired from 30,000 patients.

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

# This project includes the dollowing files- 
 1. EDA.ipynb: This is the file you will be performing the EDA.
Build and train model.ipynb: This is the file you will be building and training your model.
Inference.ipynb: This is the file you will be performing clinical workflow integration.
.dcm files: They are the test files to test the clinical workflow integration.
sample_labels.csv: This is the file that should be used to assess images in the pixel-level.
FDA_Submission_Template.md: This is the template for you to create the FDA submission. Please copy the template into your choice of editor. Finish the documentation, save it as a .pdf file, and upload.
Note: The NIH data for EDA and training is mounted in the Udacity Jupyter GPU workspace provided to you along with the code to load the data. Alternatively, you can download the data from the kaggle website and run it locally. You are STRONGLY recommended to complete the project using the Udacity workspace since the data is huge, and you will need GPU to accelerate the training process.

