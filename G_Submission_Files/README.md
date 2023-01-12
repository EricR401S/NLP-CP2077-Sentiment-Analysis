# NLP-CP2077-Sentiment-Analysis

# Introduction

For our group assignment, we had to find a dataset on which we would apply a generative
model and a neural network model. Our dataset of interest was a set of the most recent 16,599
reviews on Cyberpunk 2077, which we scraped from the Steam game store on December 8, 2022,
by using the Steam API. As for how to scrape the data, we obtained the code from a Medium
article regarding review scraping from Steam, (Muller, 2021). Then we conducted data cleaning
on the dataset, which was then reduced to 16,460 reviews, classified as 10,964 recommended
reviews and 5,496 not recommended reviews. Since our reviews have labels of “Recommended”
and “Not Recommended”, we decided to construct a generative model based on an approach
combining bag of words with the Naive Bayes theorem of conditional probability (Ersoy, 2021)
and apply a discriminative model consisting of a bidirectional LSTM neural network model to
predict whether a review has a positive sentiment (recommended) or a negative sentiment (not
recommended). Our models would be trained on a training set of 67% of the data and tested on
33% of the data, and both of them would later be trained and tested in the same manner on a
synthetic dataset created by the generative model.

Steps to reproduce the experience:
1. Run the steam scraper (A_steam_scraper.py) (This step was completed, but if run again will generate a new dataset, it won't be the same as ours, since the scraper gets the most recent 16K reviews)
2. Master dataset created (cp2077_reviews.csv.zip)
3. Run the cleaning file for generative model (B_cleaning_gen_model.py)
4. Cleaned REAL dataset for the generative model created (cleaned_real_reviews.csv)
## Real Dataset
5. Run the generative model (C_Generative_Model.py) on the cleaned real review (cleaned_real_reviews.csv), we will get the accuracy result of generative model in print statement on command line and a csv file with all the new columns (test_with_new_columns.csv). If we opted to make the synthetic data, we will get a csv for the synthetic data (synthetic_reviews_all_trial_1.csv), but running this file will create a different result each time, because it is a stochastic generation of text. 
6. Run the Bi-LSTM model (lstm_new.ipynb) on the real data, as it has special cleaning (cp2077_reviews.csv.zip), path changing is maybe needed.
## Synthetic Dataset
7. Run the generative model (C_Generative_Model.py) on the synthetic review file (synthetic_reviews_all_trial_1.csv)
8. Run the Bi-LSTM model (lstm_new_synthetic.ipynb) on the synthetic review file (synthetic_reviews_all_trial_1.csv), path changing is maybe needed.
