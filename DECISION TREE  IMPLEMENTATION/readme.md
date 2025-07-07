*Company*: CODTECH IT solutions

*Name*: Archita Paul

*Intern ID*:

*Domain*: Machine Learning

*Duration*: 4 weeks

*Mentor*: Neela Santosh



### Decision Tree Classifier – Salary Prediction Project ###
1. Data Preprocessing
The dataset consisted of categorical features: company, job, and degree, along with a binary target variable salary_more_then_100k. To prepare the data for the model, Label Encoding was applied to convert the categorical values into numerical form. This step was essential for allowing the Decision Tree algorithm to process the data. The features (X) and labels (y) were then separated for training.

2. Train-Test Split
The data was split into training and testing sets using an 80:20 ratio to evaluate the model's ability to generalize to new, unseen data. The train_test_split function from scikit-learn was used with a fixed random state to ensure reproducibility.

3. Model Building
A Decision Tree Classifier was created using scikit-learn’s tree.DecisionTreeClassifier(). The model was trained on the training set using the fit() method. The Decision Tree algorithm worked by learning simple decision rules inferred from the feature values and splitting the data recursively.

4. Prediction and Testing
Once trained, the model was used to predict outcomes on the test set using the predict() method. A sample input was also tested manually to observe the model's prediction for specific combinations of company, job, and degree. The model returned binary outputs indicating whether the person earns more than 100K.

5. Accuracy and Evaluation
The accuracy of the model was checked using the .score() function, which provided a simple measure of correct predictions on the full dataset. To understand performance in detail, a classification report was generated. It showed key metrics such as:

  Precision: How many selected items were relevant.

  Recall: How many relevant items were selected.

F1-Score: Harmonic mean of precision and recall.

These metrics helped evaluate the balance between false positives and false negatives.

6. Visualization
One of the strengths of Decision Trees is their interpretability. The model was visualized using plot_tree() with feature names and class labels. The plotted tree clearly showed how the model split the data and made decisions based on feature thresholds, making it easy to understand the logic behind predictions.

7. Conclusion
This project demonstrated how a Decision Tree can be used for a classification problem involving categorical features. It covered the full pipeline — from data preprocessing and model training to performance evaluation and visualization. The approach was simple yet effective and helped reinforce key concepts in supervised learning, especially the importance of data encoding and model interpretability.
