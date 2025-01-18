# 📚 **Fellowship.ai** Cohort 34 Submission _(NLP)_

Welcome to my repository made for the **Fellowship.ai Cohort 34** submission, focused on **NLP** task. 

The task given was to perform the sentiment analysis on `IMDb Dataset of 50K Movie Reviews` dataset.

---

## 🌟 **Project Overview**

This repository showcases sentiment analysis on IMDb datasets obtained from Kaggle. It includes two approaches:

1. **Modern Method**: Fine-tuning the dataset using the DistilBERT model.
2. **Traditional Method**: Leveraging logistic regression for sentiment analysis.

---
## 💾 Dataset Access
The IMDb dataset used in this project can be downloaded from Kaggle. Ensure you have Kaggle API credentials set up to access the dataset programmatically. You can find the dataset at the following link:

[IMDb Dataset of 50K Movie Reviews](https://www.kaggle.com/datasets/lakshmi25npathi/imdb-dataset-of-50k-movie-reviews/data)

To download the dataset using Kaggle's API, include the following script at the top of your notebook:
```python
!pip install kaggle
!mkdir ~/.kaggle
!echo '{"username":"YOUR_USERNAME","key":"YOUR_KEY"}' > ~/.kaggle/kaggle.json
!chmod 600 ~/.kaggle/kaggle.json
!kaggle datasets download -d lakshmi25npathi/imdb-dataset-of-50k-movie-reviews --unzip
```
Replace `YOUR_USERNAME` and `YOUR_KEY` with your Kaggle username and API key.

---
## 📂 **Notebooks**

### 🧠 **Modern Method**: Fine-Tuning DistilBERT
- **Notebook**: [sentiment_analysis_IMDB_Firoj.ipynb](./sentiment_analysis_IMDB_Firoj.ipynb)
- **Model**: [DistilBERT](https://huggingface.co/distilbert-base-uncased)
- **Description**: Implements a modern NLP approach by fine-tuning the IMDb dataset using Hugging Face's Trainer API.
- **Metrics**:
  - **Training Loss**: `0.1660` (after 3 epochs)
  - **Validation Loss**: `0.2743` (after 3 epochs)
  - **Training Details**:
    - Global Steps: `7500`
    - Training Samples per Second: `33.701`
    - Training Steps per Second: `2.106`
    - Total FLOPS: `1.59e+16`
  - **Evaluation Details**:
    - Evaluation Runtime: `77.1628 seconds`
    - Evaluation Samples per Second: `129.596`
    - Evaluation Steps per Second: `8.1`
  - **Confusion Matrix**:
    ```plaintext
                   precision    recall  f1-score   support

        Negative       0.93      0.93      0.93      4943
        Positive       0.93      0.93      0.93      5057

        accuracy                           0.93     10000
        macro avg       0.93      0.93     0.93     10000
        weighted avg    0.93      0.93     0.93     10000
    ```

---
### 📈 Traditional Method: Logistic Regression
- **Notebook**: [sentiment_analysis_IMDB_Firoj_trad.ipynb](./sentiment_analysis_IMDB_Firoj_trad.ipynb)
- **Model**: Logistic Regression
- **Description**: Explores a traditional machine learning approach for sentiment analysis.
- **Metrics**:
    - **Accuracy**: 0.8934
    - **Confusion Matrix**:
    ```plaintext
                   precision recall  f1-score   support

           0       0.90      0.88      0.89      4961
           1       0.88      0.91      0.90      5039

    accuracy                           0.89     10000
    macro avg       0.89      0.89     0.89     10000
    weighted avg    0.89      0.89     0.89     10000
    ```

---
## ⚙️ How to Run:

1. **Clone the repository**:
    ```bash
    git clone https://github.com/Firojpaudel/Sentiment_Analysis_IMDB.git
    ```
2. **Navigate to the project directory**:
    ```bash
    cd Sentiment_Analysis_IMDB
    ```
3. **Install the required libraries**: Ensure you have Python 3.8+ installed. Then run:
    ```bash
    pip install -r requirements.txt
    ```
4. **Run the notebook in Jupyter**:
    ```bash
    jupyter notebook
    ```
---
## ☕ Requirements

- Python 3.8+

- Jupyter Notebook

- Required Python libraries (in [requirements.txt](requirements.txt) file)

---
## ✅ Features

- Comparison of advanced NLP techniques with classic methods.

- Step-by-step setup instructions to reproduce results.

- Clear and structured documentation for quick understanding and usability. 
---
