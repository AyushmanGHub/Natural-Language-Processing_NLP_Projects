# Statistical Analysis of Language Corpora

## Introduction
This project performs statistical analysis of multilingual corpora to verify key empirical laws of language:  
- **Zipf's Law** and **Mandelbrot's Approximation** (word frequency distribution)  
- **Heaps' Law** (vocabulary growth)  

It also analyzes computational resource requirements for large-scale linguistic data. The study uses **English, Gujarati, and Marathi corpora** for comparative analysis.

## Problem Statement
The project aims to extract quantitative insights from multilingual corpora using empirical language laws. Tasks include:

1. **Zipf's Law and Mandelbrot Approximation Analysis:** Fit Zipf’s Law and Mandelbrot’s approximation; estimate parameters (α, β, C) and evaluate with R², MSE, RMSE, MAE.  
2. **Stop Word Analysis:** Analyze top 5% frequent words to determine stop word percentage.  
3. **Heaps' Law Analysis:** Validate vocabulary growth with corpus size and estimate parameters.  
4. **Computational Cost Analysis:** Estimate memory required for vocabulary-document incidence matrices.  
5. **Comparative Analysis:** Discuss cross-language differences in linguistic and computational properties.  


## Solution and Approach
The solution is implemented in a Jupyter Notebook and follows these steps:
1. **Data Preprocessing:** Clean text, remove unwanted characters, and ensure proper script handling for Indic languages.  
2. **Tokenization & Frequency Counting:** Tokenize corpora and compute word frequencies and ranks.  
3. **Model Fitting:** Fit Zipf’s Law and Mandelbrot’s approximation using non-linear least squares.  
4. **Evaluation:** Compare models using statistical metrics and visualizations.  
5. **Stop Word Analysis:** Compute percentage of stop words in the top 5% words.  
6. **Memory Estimation:** Calculate memory for vocabulary-document incidence matrices.  
7. **Results & Discussion:** Present parameters, plots, and comparative insights.  

## Results
- Log-log plots comparing empirical data vs. fitted models  
- Parameters and evaluation metrics for each model and corpus  
- Stopword percentage across languages  
- Estimated computational storage costs  
- Comparative discussion of English, Gujarati, and Marathi corpora

## Technologies Used
- Python, pandas, numpy, matplotlib, scipy  
- wiki_dump_reader, indic-nlp-library, stopwordsiso, scikit-learn  
- Google Colab   
