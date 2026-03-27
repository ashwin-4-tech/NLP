# NLP
Natural Language Processing

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
