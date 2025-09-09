### Statistical Analysis of Language Corpora

This project, named **"Statistical Analysis of Language Corpora,"** is a Python-based solution that analyzes a multilingual corpus to validate empirical laws of language and assess the computational costs of storing linguistic data. It's a comprehensive project that provides a solid foundation for further NLP tasks.

---

### Introduction
[cite_start]The objective of this assignment is to perform a statistical analysis of language corpora[cite: 1]. [cite_start]The project focuses on verifying two key empirical laws of language: **Zipf's Law** (word frequency distribution) and **Heaps' Law** (vocabulary growth)[cite: 1]. It also includes an analysis of the computational resources required for large-scale linguistic data.

The project uses three corpora for its analysis: English, Gujarati, and Marathi, and provides a comparative study of their linguistic and computational properties.

---

### Problem Statement
[cite_start]The assignment requires the analysis of a multilingual corpus to extract quantitative insights using the empirical laws of language[cite: 1]. The specific tasks include:
1.  [cite_start]**Zipf's Law Analysis:** Analyze the word frequency distribution of the corpora to determine if they adhere to Zipf's law and to find the best-fit model (Zipf's law or Mandelbrot's approximation)[cite: 1]. [cite_start]This involves finding the alpha, beta, and C parameters and evaluating the fit using metrics such as R-squared, MSE, RMSE, and MAE[cite: 1, 2].
2.  [cite_start]**Stop Word Analysis:** Analyze the top 5% of words by frequency in each corpus to determine the percentage of stop words[cite: 2].
3.  [cite_start]**Heaps' Law Analysis:** Analyze the relationship between the vocabulary size (V) and the corpus size (N) to validate Heaps' law, and find the corresponding parameters[cite: 1].
4.  [cite_start]**Computational Cost Analysis:** Estimate the computational cost of storing linguistic data by calculating the memory required for vocabulary-document incidence matrices[cite: 1, 2].
5.  [cite_start]**Comparative Analysis:** Provide a concise discussion that compares the results across the languages, interpreting the differences in the context of linguistic phenomena and computational factors[cite: 1].

---

### Solution and Approach
[cite_start]The solution is a Jupyter notebook that follows a clear, step-by-step process[cite: 2]. The approach involves:
1.  [cite_start]**Data Preprocessing:** The raw corpora, which were extracted from XML format into text files, are preprocessed to remove special characters, punctuation, links, and numbers[cite: 2]. [cite_start]For Gujarati and Marathi, the script checks if a token exists in its respective Devnagari script before tokenizing the text[cite: 2].
2.  **Tokenization and Frequency Counting:** The preprocessed text is tokenized, and the frequency of each word is counted. [cite_start]These tokens, along with their frequencies and ranks, are stored in a pandas DataFrame for each language[cite: 2].
3.  [cite_start]**Model Fitting and Evaluation:** The script uses the `scipy.optimize.curve_fit` library to fit Zipf's law and Mandelbrot's approximation to the empirical data[cite: 2]. [cite_start]It then calculates and displays various metrics to evaluate the performance of both models[cite: 2].
4.  [cite_start]**Stop Word Analysis:** A function is used to identify and count the percentage of stop words in the top 5% of the most frequent words for each language, using the `stopwordsiso` library[cite: 2].
5.  [cite_start]**Data Storage Analysis:** The notebook includes a calculation of the memory required for a vocabulary-document incidence matrix for each corpus[cite: 2].

[cite_start]The notebook provides visualizations in the form of log-log plots that show the empirical data against the predicted frequencies from both Zipf's and Mandelbrot's models, allowing for a clear visual comparison of their fit[cite: 2].

---

### Technologies Used
* **Programming Language:** Python
* **Libraries:**
    * [cite_start]`pandas`: For data manipulation and creating DataFrames[cite: 2].
    * [cite_start]`numpy`: For numerical operations, especially in model fitting[cite: 2].
    * [cite_start]`matplotlib.pyplot`: For generating data visualizations (plots)[cite: 2].
    * [cite_start]`scipy.optimize.curve_fit`: For finding the optimal parameters for Zipf's law and Mandelbrot's approximation[cite: 2].
    * [cite_start]`re`: For regular expression-based text cleaning[cite: 2].
    * [cite_start]`wiki_dump_reader`: For extracting data from the corpora[cite: 2].
    * [cite_start]`indic-nlp-library`: For tokenization of Indic languages (Gujarati, Marathi)[cite: 2].
    * [cite_start]`stopwordsiso`: For stop word analysis[cite: 2].
    * [cite_start]`sklearn.metrics`: For calculating evaluation metrics like R-squared, MSE, RMSE, and MAE[cite: 2].
* [cite_start]**Platform:** Google Colab[cite: 1].

---

### How It Works - Process Steps
1.  [cite_start]**Mount Google Drive**: The notebook begins by mounting Google Drive to access the corpus files[cite: 2].
2.  [cite_start]**Install Libraries**: Necessary libraries like `wiki_dump_reader`, `indic-nlp-library`, and `stopwordsiso` are installed[cite: 2].
3.  [cite_start]**Data Preprocessing**: The raw text from the corpus files is read, and regular expressions are used to clean the data by removing unnecessary symbols, links, and numbers[cite: 2].
4.  [cite_start]**Tokenization**: The cleaned text is tokenized for each language (English, Gujarati, Marathi)[cite: 2].
5.  [cite_start]**Frequency Analysis**: The tokens are counted, and the word frequencies and ranks are computed and stored in a pandas DataFrame[cite: 2].
6.  [cite_start]**Zipf's & Mandelbrot's Analysis**: A non-linear least squares fit is performed to find the optimal parameters for both Zipf's Law and Mandelbrot's approximation[cite: 2]. The results are plotted on a log-log scale for visualization.
7.  [cite_start]**Performance Metrics**: The performance of each model is evaluated using R-squared, MSE, RMSE, and MAE to determine the best-fit model for each language[cite: 2].
8.  [cite_start]**Stop Word Analysis**: The top 5% of words in each corpus are analyzed to find the number and percentage of stopwords using the `stopwordsiso` library[cite: 2].
9.  [cite_start]**Memory Requirement Calculation**: The memory requirement for a vocabulary-document incidence matrix is calculated for each corpus based on vocabulary size and number of documents[cite: 2].
10. [cite_start]**Results and Discussion**: The notebook presents tables and plots with the calculated parameters and metrics, followed by a discussion interpreting the results and relating them to linguistic features and computational implications[cite: 1, 2].
