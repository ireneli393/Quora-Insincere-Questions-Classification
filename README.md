# Quora-Insincere-Questions-Classification

### Summary

#### 1. Introduction
The rise in user-generated content on platforms like Quora presents challenges in content moderation, particularly in distinguishing between sincere and insincere questions. Insincere questions can mislead or provoke rather than seek genuine answers. This project applies NLP techniques to identify features that differentiate sincere from insincere questions to improve automated moderation tools.

#### 2. Related Works
Previous research has explored how linguistic features and readability metrics can identify insincere questions. Studies by Rie et al. (2012) and Elena et al. (2020) focused on lexical diversity, while Julian et al. (2023) examined readability. This research extends these studies by combining methods like N-grams selection, LDA topic modeling, and readability metrics. Logistic regression, enhanced with SHAP for interpretability, is used to classify questions.

#### 3. Theory and Hypotheses
The study hypothesizes that linguistic features such as lexical diversity and readability can reveal the underlying intentions in questions:
- **Lexical Diversity:** Insincere questions will show different levels of diversity compared to sincere ones.
- **Readability:** Significant differences in readability scores between sincere and insincere questions are expected.

#### 4. Data and Methods
- **Data:** The dataset consists of over 1 million questions from Quora, categorized as sincere or insincere.
- **Representative N-grams Selection:** TF-IDF is used to identify the most representative unigrams and bigrams for each type of question.
- **Topic Modeling:** LDA identifies themes in questions, revealing underlying topics for sincere and insincere questions.
- **Logistic Regression and SHAP:** Logistic regression with k-fold cross-validation is used for classification, and SHAP helps interpret feature importance.

#### 5. Results and Discussion
- **Hypothesis Testing:** Significant differences were found in lexical diversity and readability. Insincere questions had a lower TTR but higher Guiraud Index and lower readability scores.
- **Representative Unigrams and Bigrams:** Insincere questions often included controversial terms, while sincere questions had more varied themes.
- **Topic Modeling:** Insincere questions focused on provocative and politically charged topics, while sincere questions addressed personal improvement, career advice, and educational content.
- **Logistic Regression and SHAP Analysis:** The model achieved an F1 score of 0.76 and accuracy of 0.84. SHAP analysis identified specific words contributing to classifications, showing that insincere questions often used direct, demanding language, while sincere questions reflected genuine curiosity and relational contexts.

#### 6. Conclusion
The study highlights linguistic differences between sincere and insincere questions, showing that insincere questions tend to be more complex and controversial. The logistic regression model, combined with SHAP, provides insights into how specific words influence question classification. Future research could explore cultural and contextual factors affecting language use and enhance machine learning techniques for better online content management.
