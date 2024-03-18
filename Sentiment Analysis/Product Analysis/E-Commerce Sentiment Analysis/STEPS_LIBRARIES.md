Here's a detailed description of the steps carried out in the project:

1. **Loading and Preprocessing the IMDb Dataset**:
   - Initially, you loaded the IMDb dataset (`IMDB Dataset.csv`) into a Pandas DataFrame (`df`) and displayed the first 10 rows using the `head()` function.
   - You checked for any missing values in the DataFrame using `isnull().sum()`.
   - Then, you installed the NLTK library to perform natural language processing tasks.

2. **Training a Sentiment Classifier**:
   - After installing NLTK, you imported the necessary libraries and downloaded NLTK resources (tokenizers and stopwords).
   - Using the IMDb dataset, you trained a Naive Bayes classifier to classify movie reviews as positive or negative sentiments.
   - The IMDb dataset was preprocessed by tokenizing the reviews, removing stop words, and creating labeled feature sets.
   - The dataset was split into training and testing sets, and a feature extractor function was defined to convert reviews into feature sets.
   - The Naive Bayes classifier was trained using the training set, and its accuracy was evaluated using the testing set.
   - Finally, you determined the percentage of positive and negative reviews in the test set.

3. **Analyzing Flipkart Product Reviews**:
   - You loaded the Flipkart product dataset (`flipkart_product.csv`) into a DataFrame and dropped the "Price" column.
   - The modified DataFrame was saved to a new CSV file named `fp.csv`.
   - Next, you preprocessed the reviews in the Flipkart product dataset using the same preprocessing steps applied to the IMDb dataset.
   - The Naive Bayes classifier trained on the IMDb dataset was applied to the Flipkart product reviews to predict sentiments.
   - The predicted sentiments were added to the DataFrame, and the DataFrame with predicted sentiments was saved to a new CSV file named `fp_with_sentiment.csv`.
   - Additionally, you plotted a bar graph showing the average sentiment for 10 random products from the Flipkart dataset.

4. **Grouping Product Names and Sentiments**:
   - You grouped the DataFrame by both "ProductName" and "Predicted Sentiment" columns and applied the mode function to handle cases where the same product had multiple reviews with different sentiments.
   - The grouped DataFrame was saved to a new CSV file named `grouped_product_sentiment.csv`.

5. **Creating Separate CSV Files for Positive and Negative Sentiments**:
   - Finally, you filtered the grouped DataFrame to separate product names with positive and negative sentiments.
   - The product names with positive sentiments were saved to a new CSV file named `fp_pos.csv`, and those with negative sentiments were saved to `fp_neg.csv`.

6. **Displaying Results**:
   - You displayed the contents of `fp_pos.csv` and `fp_neg.csv` to verify the separation of product names based on sentiment.

This sequence of steps demonstrates how you processed the IMDb dataset to train a sentiment classifier and then applied the same classifier to analyze product 
reviews from Flipkart. Let me know if you need further clarification or assistance with anything else!

Below is a description of the libraries used in the project:

1. **Pandas**:
   - Pandas is a powerful data manipulation and analysis library for Python.
   - It provides data structures like DataFrames and Series, which are efficient for handling structured data.
   - Pandas is widely used for tasks such as data cleaning, transformation, and analysis.

2. **NLTK (Natural Language Toolkit)**:
   - NLTK is a leading platform for building Python programs to work with human language data.
   - It provides easy-to-use interfaces to over 50 corpora and lexical resources, such as WordNet.
   - NLTK includes various modules for tasks like tokenization, stemming, tagging, parsing, and classification.
   - It's widely used in natural language processing (NLP) tasks, including sentiment analysis, named entity recognition, and text classification.

3. **Matplotlib**:
   - Matplotlib is a comprehensive library for creating static, animated, and interactive visualizations in Python.
   - It provides a MATLAB-like interface for generating plots, graphs, histograms, and other visualizations.
   - Matplotlib is highly customizable, allowing users to create publication-quality figures with ease.
   - It's widely used in data analysis, scientific research, and data visualization projects.

4. **NumPy**:
   - NumPy is a fundamental package for scientific computing in Python.
   - It provides support for large, multi-dimensional arrays and matrices, along with a collection of mathematical functions to operate on these arrays.
   - NumPy arrays are more efficient than Python lists for numerical computations and are extensively used in numerical and scientific computing tasks.

These libraries collectively provide a robust foundation for performing data analysis, natural language processing, and visualization tasks in Python. They are widely adopted by data scientists, researchers, and developers for various applications in data science, machine learning, and beyond.
