<H3>Name: Senthil Kumar S</H3>
<H3>Register Number: 212221230091</H3>
<H3>Date: 13/05/2024</H3>
<H1 Align="center">Project Based Experiment<H1>
<H3>Objective :</H3>
  
Perform sentiment analysis using your Facebook data and filter the data that has only Positive feedback for the code given in the following link.

<H3>Program:</H3>
  
```py
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

# Filter out rows with positive sentiment (label 'P')
positive_feedback = df[df['Label'] == 'P']

# Output the negative feedback
print(positive_feedback)
```

<H3>Output:</H3>

![](o1.png)
![](o2.png)

<H3>Inference:</H3>
Thus sentiment analysis using Facebook data is done and filtering the data that has only positive feedback for the code is executed successfully.
