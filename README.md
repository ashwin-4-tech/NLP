
### Task 1: Conceptual Understanding

1. **What is the difference between "Love" and "love" in NLP?**
   In standard NLP tokenization, they are treated as two distinct unique identifiers (IDs) because of case sensitivity. Lowercasing helps consolidate their semantic meaning.

2. **What happens if stopwords are not removed?**
   If not removed, high-frequency words (the, is, a) can dominate the statistical analysis, making it harder for models to focus on the unique keywords that define a document's topic.

3. **Scenarios where removing stopwords is harmful:**
   - **Sentiment Analysis**: Removing words like "not" or "no" can change "I am not happy" to "I happy", completely reversing the sentiment.
   - **Machine Translation**: Stopwords are crucial for the grammatical structure and fluency of the translated sentence.

4. **Stemming vs. Lemmatization:**
   - **Stemming**: Chops off suffixes (e.g., 'playing' -> 'play'). It is fast but often results in words that aren't in the dictionary.
   - **Lemmatization**: Uses a dictionary (morphological analysis) to find the root word (e.g., 'better' -> 'good'). It is more accurate but computationally heavier.


# 5-Step Sentiment Analysis Pipeline

### Step 1: Data Acquisition & Loading
We use `kagglehub` to download the IMDb dataset and `pandas` to load it into a DataFrame. This step ensures we have a structured format to work with.

### Step 2: Exploratory Data Analysis (EDA)
In this phase, we analyze the dataset's characteristics:
- Checking for **null values** to ensure data integrity.
- Verifying **class balance** (e.g., ensuring we have an equal number of positive and negative reviews) to prevent model bias.

### Step 3: NLP Preprocessing
Raw text is noisy. We clean it by:
- **Lowercasing**: Standardizing text.
- **HTML/URL Removal**: Removing non-textual noise using Regular Expressions.
- **Tokenization**: Breaking sentences into words.
- **Stopword Removal & Lemmatization**: Removing common words (is, the) and reducing words to their root form (e.g., 'rocks' to 'rock').

### Step 4: Feature Engineering
Machine Learning models require numbers, not text. We use:
- **Label Encoding**: Converting 'positive'/'negative' labels to 1 and 0.
- **Vectorization**: Using **TF-IDF** (Term Frequency-Inverse Document Frequency) and **Bag of Words** to create numerical representations of the reviews.

### Step 5: Model Training & Evaluation (Next Step)
We will train multiple models (Logistic Regression, Naive Bayes, etc.) and compare them using metrics like **Accuracy**, **Precision**, and **F1-Score**.
