# Week 6 – Natural Language Processing Pipeline and Text Classification

**Assignment:** Natural Language Processing Pipeline and Text Classification

## Assignment Overview

This assignment focuses on building a Natural Language Processing (NLP) pipeline to classify customer inquiries in the real estate industry. The objective is to automatically categorize customer messages into predefined inquiry categories using text preprocessing, feature extraction, and machine learning techniques.

## Business Problem

Real estate companies receive a large number of customer inquiries every day through websites, emails, and online forms. These inquiries may relate to property viewings, rental applications, mortgage information, maintenance concerns, neighbourhood information, or property pricing.

Manually reviewing and categorizing every inquiry can be time-consuming and may delay customer responses. By using NLP and text classification, the company can automatically identify the category of each inquiry and route it to the appropriate department. This improves operational efficiency, reduces response times, and enhances customer service.

## Dataset

**Dataset:** NLP Dataset 9 – Real Estate Inquiry Category

The dataset contains customer inquiries along with their corresponding inquiry categories. It includes one text column used for classification and several supporting business-related attributes.

### Important Features

* InquiryID
* InquiryDate
* Channel
* City
* PropertyType
* ClientType
* InquiryText
* LeadScore

### Target Variable

**InquiryCategory**

Categories include:

* Price_Question
* Rental_Application
* Mortgage_Info
* Viewing_Request
* Maintenance_Concern
* Neighbourhood

## Text Preprocessing

The following NLP preprocessing steps were applied to prepare the text data:

* Converted text to lowercase
* Removed punctuation
* Removed stopwords
* Tokenized text into individual words
* Applied lemmatization
* Created a cleaned text column for analysis

These steps help remove unnecessary information and improve the quality of the text data used for machine learning.

## Exploratory Text Analysis

Exploratory text analysis was conducted to understand common patterns in customer inquiries. This included:

* Identifying the most frequently used words
* Calculating word frequencies
* Creating visualizations of common terms
* Interpreting the relationship between frequent words and inquiry categories

The analysis provides insights into the main topics customers discuss when contacting a real estate company.

## Feature Extraction

TF-IDF (Term Frequency–Inverse Document Frequency) was used to convert text into numerical features.

Machine learning algorithms cannot process raw text directly. TF-IDF transforms text into a numerical representation while emphasizing important words and reducing the impact of common words that appear frequently across documents.

## Machine Learning Model

A Logistic Regression classifier was trained using the TF-IDF features extracted from the cleaned text.

### Steps Performed

1. Defined features (X) and target variable (y)
2. Split the dataset into training and testing sets
3. Trained the Logistic Regression model
4. Generated predictions on the test dataset
5. Evaluated model performance

## Model Evaluation

The model was evaluated using:

* Accuracy Score
* Confusion Matrix
* Classification Report

These metrics help determine how effectively the model can classify customer inquiries into the correct categories.

## Business Interpretation

The model successfully predicts the category of customer inquiries based on the text provided by the customer. Automating this process can help real estate companies respond more quickly and direct inquiries to the correct team without manual intervention.

The analysis showed that customer inquiries frequently focus on pricing, rentals, mortgages, property viewings, maintenance issues, and neighbourhood information. These insights can help businesses better understand customer needs and allocate resources more effectively.

## Limitation

One limitation of this project is the relatively small dataset size. With only a limited number of inquiry records, the model may not capture all possible variations in customer language. A larger dataset would likely improve model performance and generalization to real-world applications.

## Technologies Used

* Python
* Pandas
* NLTK
* Scikit-learn
* Matplotlib
* Seaborn
* Jupyter Notebook

## Conclusion

This project demonstrates how Natural Language Processing and Machine Learning can be used to automate text classification in a real estate business environment. By transforming raw customer inquiries into structured information, organizations can improve efficiency, reduce manual effort, and provide faster customer service.

