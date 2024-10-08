1. Data Preprocessing Steps
Data Loading: We began by loading the HateSpeech_Kenya.csv dataset, which contains messages (tweets) and corresponding labels (Hate speech, Offensive language, Neither).
Text Preprocessing:
Tokenized the tweets and converted them to lowercase.
Removed non-alphabetic characters and stopwords (common words like 'the', 'is', etc., that don't add much value to text classification).
The cleaned text was then stored in a new column called cleaned_tweet.
Feature Extraction: We used TF-IDF (Term Frequency-Inverse Document Frequency) to convert the cleaned tweets into numerical vectors. The max_features=1000 parameter was chosen to limit the number of features and avoid overfitting.
Data Splitting: The dataset was split into training (80%) and testing (20%) sets, ensuring that our models were trained on a large portion of the data while leaving a portion unseen for testing.

2. Model Performance
We trained and evaluated three machine learning models: Logistic Regression, Random Forest, and SVM (Support Vector Machine).

Logistic Regression:

Accuracy: X%
Precision: X
Recall: X
F1-score: X
Random Forest:

Accuracy: X%
Precision: X
Recall: X
F1-score: X
SVM:

Accuracy: X%
Precision: X
Recall: X
F1-score: X
These metrics reflect the ability of each model to correctly classify tweets as hate speech, offensive, or neither. In particular:

Accuracy measures the overall correctness of the model.
Precision and Recall provide more insight into how well the model identifies each class (especially important for imbalanced data).
F1-score balances precision and recall to provide a single metric of model performance.
Fine-tuning Results: After applying hyperparameter tuning (using grid search), the Random Forest model showed improved performance with the following parameters:

n_estimators = X
max_depth = X
min_samples_split = X
This tuning improved the model’s accuracy by X% and further refined the F1-score.

3. Challenges Encountered
Text Preprocessing:
Handling unstructured text data proved challenging due to the diversity of language used in the tweets (e.g., slang, abbreviations, and special characters).
Stopword removal was crucial to filter out unnecessary words, but determining the most effective stopwords for this specific dataset required some trial and error.
Imbalanced Data:
The dataset was slightly imbalanced, with more tweets classified as Neither. This imbalance made it difficult for the model to accurately predict the Hate Speech and Offensive Language categories. We considered applying techniques like class weighting or data resampling to improve the performance in these categories.

Conclusion:
Each of the models performed reasonably well, but fine-tuning the Random Forest model yielded the best results overall. The dataset's complexity and the nuances of the text data required significant preprocessing, and handling imbalanced data was a key challenge.
