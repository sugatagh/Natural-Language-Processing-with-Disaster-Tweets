# Natural Language Processing with Disaster Tweets

## Project Report

**https://sugatagh.github.io/dsml/projects/natural-language-processing-with-disaster-tweets/**

## Kaggle Notebook

**https://www.kaggle.com/sugataghosh/natural-language-processing-with-disaster-tweets**

## Overview

- Disaster-related tweets have the potential to alert relevant authorities early on so that they can take action to reduce damage and possibly save lives.

- In this project, we attempt to predict whether a given tweet indicates a real disaster or not.

- A detailed [**exploratory data analysis**](https://en.wikipedia.org/wiki/Exploratory_data_analysis) on the dataset is carried out.

- We consider a number of [**text normalization**](https://en.wikipedia.org/wiki/Text_normalization) processes, namely **conversion to** [**lowercase**](https://en.wikipedia.org/wiki/Letter_case), **removal of** [**whitespaces**](https://en.wikipedia.org/wiki/Whitespace_character), **removal of** [**punctuations**](https://en.wikipedia.org/wiki/Punctuation), **removal of** [**unicode characters**](https://en.wikipedia.org/wiki/List_of_Unicode_characters) (including [**HTML**](https://en.wikipedia.org/wiki/HTML) tags, [**emojis**](https://en.wikipedia.org/wiki/Emoji), and [**URL**](https://en.wikipedia.org/wiki/URL)s starting with [**http**](https://en.wikipedia.org/wiki/HTTP)), **substitution of** [**acronyms**](https://en.wikipedia.org/wiki/Acronym), **substitution of** [**contractions**](https://en.wikipedia.org/wiki/Contraction_(grammar)), **removal of** [**stop words**](https://en.wikipedia.org/wiki/Stop_word), [**spelling**](https://en.wikipedia.org/wiki/Spelling) **correction**, [**stemming**](https://en.wikipedia.org/wiki/Stemming), [**lemmatization**](https://en.wikipedia.org/wiki/Lemmatization), **discardment of non-alphabetic words**, and **retention of relevant** [**parts of speech**](https://en.wikipedia.org/wiki/Part_of_speech).

- We implement [**bag of words**](https://en.wikipedia.org/wiki/Bag-of-words_model) text representation and extend the analysis to bag of [**bigrams**](https://en.wikipedia.org/wiki/Bigram) as well as a mixture representation incorporating both words and bigrams.

- Next, we implement [**TF-IDF**](https://en.wikipedia.org/wiki/Tf%E2%80%93idf) text representation. Similar to the previous setup, we carry out unigram, bigram, and mixture analysis.

- Finally, we use [**word2vec**](https://en.wikipedia.org/wiki/Word2vec) embedding for text representation.

- For each text representation setup, we apply a number of [**classifiers**](https://en.wikipedia.org/wiki/Statistical_classification), namely [**logistic regression**](https://en.wikipedia.org/wiki/Logistic_regression), [**k-nearest neighbors classifier**](https://en.wikipedia.org/wiki/K-nearest_neighbors_algorithm), [**decision tree**](https://en.wikipedia.org/wiki/Decision_tree), [**support vector machine**](https://en.wikipedia.org/wiki/Support_vector_machine) with [**radial basis function kernel**](https://en.wikipedia.org/wiki/Radial_basis_function_kernel), [**random forest**](https://en.wikipedia.org/wiki/Random_forest), [**stochastic gradient descent**](https://en.wikipedia.org/wiki/Stochastic_gradient_descent), [**ridge classifier**](https://en.wikipedia.org/wiki/Ridge_regression), [**XGBoost classifier**](https://en.wikipedia.org/wiki/XGBoost), and [**AdaBoost classifier**](https://en.wikipedia.org/wiki/AdaBoost), and compare their performances in terms of the average [**F1-score**](https://en.wikipedia.org/wiki/F-score) obtained from $5$ repetitions of $6$-fold [**cross-validation**](https://en.wikipedia.org/wiki/Cross-validation_(statistics)).

- The **support vector machine** classifier with a **radial basis function kernel** acting on the embedded data obtained through the **word2vec** algorithm produces the best result in terms of the average $F_1$-score obtained from $5$ repetitions of $6$-fold cross-validation. It achieves an average $F_1$-score of $0.783204$.