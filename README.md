# EmoCK
Facial expression recognition datasets with emotion categories 

## 🏆 Leaderboard

👉 [Click here to view the live leaderboard](https://tasneem-mselim.github.io/EmoCK/)

# 🧠 EmoCK / CK+ Facial Expression Recognition

## 📌 Overview
This competition focuses on facial expression recognition using the CK+ dataset, where participants classify emotions from facial images.

## 🎯 Task Description
Classify each image into one of 7 emotion classes:
anger, contempt, disgust, fear, happy, sadness, surprise.

## 🏆 Objective
Build a model that achieves the highest accuracy on unseen facial images.

## 🔗 Dataset Link
https://www.kaggle.com/datasets/shawon10/ckplus

## 📂 Dataset Description
CK+ is a standard benchmark dataset for emotion recognition with labeled facial expressions.

## 📁 Dataset Structure
train/ (labeled images), test/ (unlabeled images + predictions.csv)

### Public vs Private
- Public: train
- Private: test labels


## 📝 Submission Format
Your model must output a CSV file named `submission.csv`. It must strictly follow this structure:

| id | label |
| :--- | :--- |
| img_1.JPG | 3 |
| img_2.JPG | 1 |
| img_3.JPG | 6 |

### 🔍 Constraints:
*   **ID Match:** The `id` must match the provided test image names exactly.
*   **Target Range:** `label` must be an integer.

---

## 🛠 How to Submit Your Results

Follow these steps precisely to ensure your submission is evaluated correctly.

### 1- Fork the Repository
Click the **Fork** button at the top right of this repository to create your own copy.

### 2- Prepare Locally
Navigate to the `submission/` folder in your local environment. Ensure you have the following files in one directory:
1.  `encrypt_submission.py` (Provided in the repo)
2.  `public_key.pem` (Provided in the repo)
3.  Your generated `submission.csv`

### 3- Encrypt Your Submission
Open your terminal or CMD in that folder and run the encryption command:

```bash
python encrypt_submission.py submission.csv submission.enc submission.enc.key public_key.pem


This will generate two files:

- `submission.enc` → the encrypted submission  
- `submission.enc.key` → encryption key  

Both files are required for submission. Do **not** submit the original CSV.

### 4- Place Encrypted Files in Submission Folder

Upload these files to the `submission/` folder in your forked repository

### 5- Create a Pull Request
Your submission will be reviewed and evaluated, and the results will be added to the leaderboard.


Only one submission is allowed for each participant. Subsequent submissions will be automatically rejected



## 📏 Evaluation Metric
Accuracy, F1-score

## ✅ Allowed
CNNs, transfer learning

## ❌ Not Allowed
External emotion datasets, manual labeling

## 🧪 Baseline Model
2-layer CNN (Conv → MaxPool → Conv → MaxPool → Dense)

## 📚 References
Lucey et al., 2010

## 👩‍🏫 Organizer
Tasneem Selim
