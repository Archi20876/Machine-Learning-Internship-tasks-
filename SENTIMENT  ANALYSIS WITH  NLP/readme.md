Company: CODTECH IT solutions

Name: Archita Paul

Intern ID:CITSOD42

Domain: Machine Learning

Duration: 4 weeks

Mentor: Neela Santosh
### Sentiment Analysis Using Logistic Regression

This project focuses on building a sentiment analysis model using logistic regression to classify customer feedback into positive or negative sentiments based on review text data.

1. Data Loading and Preprocessing
The dataset was loaded using Pandas from a CSV file. The columns text and sentiment were renamed to verified_reviews and feedback respectively for clarity. Only rows containing "positive" or "negative" sentiments were considered for binary classification. The feedback column was mapped to numeric values: positive as 1 and negative as 0.
Missing values were checked and handled by filling null values with 0 and converting the data type to integers. The dataset also included irrelevant columns like Land Area (Km²) and Density (P/Km²), which were removed to focus solely on text-based sentiment classification.


3. Text Cleaning and Feature Extraction
Text data was cleaned using regular expressions to remove non-alphabet characters. All text was converted to lowercase, tokenized, and stemmed using the PorterStemmer from NLTK. This reduced words to their root forms, enhancing consistency in the data.A cleaned list of reviews called the corpus was created. To convert textual data into numeric format suitable for modeling, TF-IDF Vectorization was applied. The TfidfVectorizer was set to extract a maximum of 2500 features and remove common English stopwords.

3. Train-Test Split and Feature Scaling
The processed data was split into training and testing sets using an 80:20 ratio with train_test_split, ensuring random yet reproducible partitioning. Before training, MinMaxScaler was applied to normalize the feature values between 0 and 1, which helps improve the convergence speed and performance of the logistic regression model.

4. Model Training
A Logistic Regression model was implemented using scikit-learn’s LogisticRegression class. The model was trained on the scaled training data with the number of iterations increased to 1000 to ensure proper convergence. Logistic regression was chosen due to its simplicity, interpretability, and effectiveness for binary classification tasks like sentiment analysis.

5. Evaluation
The model was evaluated using both the training and testing accuracy scores, giving insight into how well it fits the training data and generalizes to unseen data. Predictions were made on the test set, and a confusion matrix was generated to visualize the classification performance.

The confusion matrix displayed the number of true positives, true negatives, false positives, and false negatives. To enhance understanding, it was visualized using ConfusionMatrixDisplay from scikit-learn, providing a clear overview of model accuracy and misclassifications.
