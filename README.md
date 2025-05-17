# Naive-Bayes-Spam-Detector
Naive Bayes text classifier for email spam detection using raw files and scikit-learn. Parses real message bodies, transforms them to bag-of-words, and predicts spam vs ham with trained probabilities.

This project implements a basic but functional **Naive Bayes email classifier** that detects whether a given message is spam or ham (non-spam). It reads raw `.txt` files from directories, extracts the body of each email, and uses **bag-of-words vectorization** to feed a **Multinomial Naive Bayes** model using `scikit-learn`.

It’s a simple demonstration of how real-world spam filtering works — from reading messy files to making confident predictions.

---

## What This Project Does

✔ Parses actual email files from `spam/` and `ham/` folders  
✔ Extracts **only the message body** (ignores headers)  
✔ Builds a `pandas.DataFrame` of labeled email data  
✔ Converts the data into word-frequency vectors using `CountVectorizer`  
✔ Trains a **Naive Bayes** model on that vectorized data  
✔ Makes predictions and shows **class probabilities**

---

## Project Structure
├── spamorham.py # Main Python script
├── spam/ # Folder of raw spam emails (.txt) — not included
├── ham/ # Folder of raw ham emails (.txt) — not included

---

## ⚠️ Missing Folders Notice

> ⚠️ **NOTE**: I didn’t attach the `spam/` and `ham/` folders because they were too damn big.
>
> GitHub has upload size limits, and the dataset would’ve made the repo bloated.  
> To run this locally, make sure you create your own `spam/` and `ham/` directories and populate them with raw text email files.

---

## 🚀 How to Run

### 1. Install Dependencies

```bash
pip install pandas scikit-learn

your_project/
├── spamorham.py
├── spam/
│   ├── 00001.txt
│   ├── 00002.txt
├── ham/
│   ├── 00001.txt
│   ├── 00002.txt
