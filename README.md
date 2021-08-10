# tweet-sentiment-extraction

- The kaggle competition link: [Tweet Sentiment Extraction](https://www.kaggle.com/c/tweet-sentiment-extraction/overview).
- Extract support phrases for sentiment labels


## What files do I need?

You'll need **train.csv**, **test.csv**, and **sample_submission.csv**.
Please checkout [Kaggle data page](https://www.kaggle.com/c/tweet-sentiment-extraction/data)

## What should I expect the data format to be?

Each row contains the `text` of a tweet and a `sentiment` label. In the training set you are provided with a word or phrase drawn from the tweet (`selected_text`) that encapsulates the provided sentiment.

Make sure, when parsing the CSV, to remove the beginning / ending quotes from the `text` field, to ensure that you don't include them in your training.

## What am I predicting?

You're attempting to predict the word or phrase from the tweet that exemplifies the provided sentiment. The word or phrase should include all characters within that span (i.e. including commas, spaces, etc.). The format is as follows:

`<id>,"<word or phrase that supports the sentiment>"`

For example:

    2,"very good"
    5,"I am neutral about this"
    6,"bad"
    8,"if you say so!"
    etc.

## Files

*   **train.csv** - the training set
*   **test.csv** - the test set
*   **sample_submission.csv** - a sample submission file in the correct format

## Columns

*   `textID` - unique ID for each piece of text
*   `text` - the text of the tweet
*   `sentiment` - the general sentiment of the tweet
*   `selected_text` - [train only] the text that supports the tweet's sentiment
