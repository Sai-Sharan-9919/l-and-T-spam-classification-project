TITLE:    pandas data plotting

problem statement:   spam detection system

Description:

In the modern digital world, individuals receive a large volume of electronic messages daily, including SMS, emails, and instant messages. Many of these are unsolicited or harmful messages, commonly known as spam. Spam messages often include fraudulent links, misleading promotional content, or attempts to extract sensitive personal data. These can be not only annoying but also dangerous. To counter this, our project aims to build a Spam Detection System that can automatically classify messages as either spam or not spam using machine learning techniques.

This project uses the K-Nearest Neighbors (KNN) algorithm, a simple yet powerful machine learning approach based on instance-based learning. KNN classifies data based on the majority class of its nearest neighbors, making it easy to implement and interpret. Although commonly used for numerical data, KNN performs quite well on text classification tasks when proper preprocessing and feature extraction are applied.

The dataset used is the SMS Spam Collection Dataset, which contains over 5,000 text messages labeled as either “ham” (not spam) or “spam”. The raw data undergoes several preprocessing steps including:

Lowercasing text

Removing punctuation and numbers

Cleaning and normalizing words

After cleaning, the text data is converted into numerical features using the TF-IDF (Term Frequency-Inverse Document Frequency) vectorization technique. This step transforms the text into meaningful vectors based on word importance, allowing machine learning models to make informed classifications.

Following vectorization, the feature vectors are normalized to ensure distance-based algorithms like KNN work effectively. The dataset is then split into training and test sets using an 80:20 ratio. To address class imbalance, SMOTE (Synthetic Minority Over-sampling Technique) can be applied optionally to the training set, although in this project the model performs well without it due to sufficient data balance.

The core of the system is the KNeighborsClassifier from the Scikit-learn library, configured with n_neighbors=3 and the cosine distance metric. Cosine similarity is well-suited for text data as it considers the direction of vectors rather than their magnitude. The model is trained on the training data and evaluated on the test set using metrics like accuracy, precision, recall, F1-score, and a confusion matrix. The system achieves high accuracy (~94–96%), indicating strong performance in correctly classifying both spam and legitimate messages.

An interactive feature is also integrated into the program, allowing users to input custom messages and receive real-time predictions. This makes the tool practical and user-friendly for testing its functionality.

In summary, this project demonstrates the successful implementation of a real-world text classification system using KNN and NLP techniques. It showcases the power of simple algorithms when combined with thoughtful preprocessing and effective feature engineering. The system can be further enhanced with alternative models, web deployment, and integration with messaging platforms for real-time spam filtering.



OUTPUT:   

![Screenshot 2025-05-15 212404](https://github.com/user-attachments/assets/caa58822-dbfc-458d-b4f9-1fff46af13b3)
