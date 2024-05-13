## NAME : NIRAUNJANA GAYATHRI G R
## REG NO: 212222230096
## DATE:13/05/2024

# Project Based Experiment

## Objective:
Perform sentiment analysis using your Facebook data and filter the data that has only negative feedback for the code given in the following link.

## Program:

```
pip install pandas textblob
import pandas as pd
from textblob import TextBlob

# Load the CSV file into a DataFrame
df = pd.read_csv('fb_sentiment.csv')

# Function to perform sentiment analysis using TextBlob
def analyze_sentiment(text):
    blob = TextBlob(str(text))
    return blob.sentiment.polarity

# Apply sentiment analysis to each row in the DataFrame
df['Sentiment'] = df['FBPost'].apply(analyze_sentiment)

# Output the DataFrame with sentiment analysis results
print(df.head())

# Filter out rows with negative sentiment (label 'N')
negative_feedback = df[df['Label'] == 'N']

# Output the negative feedback
print(negative_feedback)

```

## Output:

![329918019-a6539c89-7efd-4679-b2d3-b7da9feb4393](https://github.com/niraunjana/Project-Based-Experiment-AAI/assets/119395610/492cb4b2-2eea-4479-b3eb-e68fb0da1afa)

![329918065-fd6249e6-f2ad-48e9-b3a9-13f9747c94ca](https://github.com/niraunjana/Project-Based-Experiment-AAI/assets/119395610/b1a2d0d2-4e9d-436e-963d-bd9227c56908)

## Inference:
Thus sentiment analysis using your Facebook data ias done and filtering the data that has only negative feedback for the code is done. 
