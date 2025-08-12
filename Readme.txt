📧 Spam Email Classifier – Project Overview
This project focuses on building a spam detection system using the Apache SpamAssassin Public Corpus.
It processes raw email data, transforms it into numerical features, and trains a machine learning model to classify emails as ham (non-spam) or spam.

📂 Dataset
 • Ham (Non-Spam) → Legitimate emails

 • Spam → Unwanted promotional/malicious emails

 • Downloaded from Apache SpamAssassin’s public datasets

 • Total: 2500 ham emails and 500 spam emails

🔹 Workflow Overview
1. Data Acquisition
 • Downloaded and extracted the ham and spam datasets.

 • Stored them in a local structured folder for processing.

2. Email Parsing
 • Used Python’s email parsing tools to read each email’s content and metadata.

 • Analyzed MIME types to understand if emails were in plain text, HTML, or multipart format.

3. Exploratory Analysis
 • Counted and compared the structure of ham vs spam emails.

 • Observed that spam emails had a higher occurrence of HTML content and links.

4. Data Splitting
 • Combined ham and spam emails into a single dataset.

 • Split into 80% training and 20% testing sets.

5. Text Preprocessing
 • Converted HTML to plain text for uniformity.

 • Standardized text by:

   •Lowercasing

   •Removing punctuation

   •Replacing URLs with a placeholder

   •Replacing numbers with a placeholder

   •Stemming words to their root form

6. Feature Extraction
 • Counted occurrences of each word in the training dataset.

 •Built a vocabulary of the most frequent words.

 •Represented emails as sparse vectors indicating word frequencies.

7. Pipeline Creation
 •Combined preprocessing and vectorization into a single Scikit-Learn pipeline.

 •Enabled easy transformation of raw emails into numerical features for model training.

8. Model Training
 •Used Logistic Regression as the classification algorithm.

 •Performed cross-validation to ensure stability of results.

9. Evaluation
 •Achieved high performance on the test set:

    •Accuracy: ~98.5%

    •Precision: 96.88%

    •Recall: 97.89%

📊 Key Insights
 •Spam emails tend to contain more HTML formatting, links, and marketing-related keywords.

 •The preprocessing pipeline is critical for improving model performance by cleaning and normalizing email content.

 •The model successfully balances precision and recall, reducing both false positives and false negatives.

📦 Tools & Libraries
 •Scikit-Learn – Model building & pipelines

 •NLTK – Word stemming

 •urlextract – URL detection

 •NumPy & SciPy – Data structures & sparse matrices

 •Python email module – Email parsing

🚀 Outcome
This classifier can be integrated into email systems to automatically detect spam with high accuracy.
It is flexible enough to adapt to different datasets and can be improved further by:

 •Adding more advanced NLP techniques (TF-IDF, word embeddings)

 •Using more complex models like SVMs or neural networks
