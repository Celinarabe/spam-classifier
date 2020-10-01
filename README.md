# spam-classifier

## Project Goal: 
Use support vector machines to build a spam email classifier

## Implementation Steps:
Step 1: Implement Gaussian Kernel as a similarity function between pairs of examples to create a non-linear decision boundary.

Step 2: Find optimal values for C (regularization parameter) and σ (rate of similarity) in multiplicative steps on the cross validation set.

Step 3: Normalizing and preprocessing of data
  - Lower-casing
  - Stripping HTML
  - Normalizing URLs - All URLs are replaced with the text "httpaddr"
  - Normalizing Email Addresses - All email addresses are replaced with the text "emailaddr"
  - Normalizing Numbers - All numbers are replaced with the text "number"
  - Normalizing Dollars - All dollar signs ($) are replaced with the text "dollar"
  - Word Stemming - Words are reduced to their stemmed form. (Ex: "discounts" and "discounting" are replaced with "discount")
  - Removal of non-words - Non-words and punctuation have been removed. All white spaces (tabs, newlines, spaces) have all been trimmed to a single space character.

*Raw Dataset: [SpamAssassin Public Corpus](http://spamassassin.apache.org/old/publiccorpus/)*

Step 4: Vectorize input data based on all words with at least 100 occurrences

Step 5: Train SVM on training data
