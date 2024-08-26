# IAAA Competition
all the code and data for the 2nd IAAA competition


## MRI
- DICOM is Digital Imaging and Communications in Medicine
- MRI creates these types of images:
1. T1 (T1-weighted images): fluid appears dark and fat appears bright. used to anatomical structures of the brain.
2. T2 (T2-weighted images): fluid appears bright and fat appears dark. used to detect edema, inflammation, and tumors.
3. FLAIR (Fluid-Attenuated Inversion Recovery): used to suppress the signal from cerebrospinal fluid (CSF) and make it easier to see lesions.
- Modality is imaging techniques like CT, MRI, X-ray, Ultrasound, etc.
- Study is each set of images taken during a single imaging session. for example if a person has a CT scan of the head and a CT scan of the chest, these are two different studies.
- Series is a set of images taken during a single imaging session using the same modality and protocol. for example, a T1-weighted MRI of the brain is a series.
- an example is a dataset that contains a study for each patient, and each study contains three series of T1, T2, and FLAIR images that each of series contains multiple slices of images.

## Data
- labling is series-level, meaning that if a single image in a dicom series is labeled as positive, the whole series is labeled as positive
- dataset link in Kaggle: [iAAA-MRI-Challenge](https://www.kaggle.com/datasets/iaaaplatform/iaaa-mri-challenge/data)


## Submission
- upload a zip file containing a submission.py file
- the server running the code is offline
- the command that runs the file is this:  
```bash 
python3 /iaaa/code/submission.py --data-dir /path/to/data-dir --predictions-file-path /path/to/submission.csv
```
- the output of the code should create a csv file with the following format:  
```csv
SeriesInstanceUID, prediction
```