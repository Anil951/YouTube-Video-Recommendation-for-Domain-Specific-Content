# YouTube Video Recommendation for Domain-Specific Content

Welcome to the YouTube Video Recommendation System project! This comprehensive system is designed to offer personalized and relevant video recommendations within a specific content domain. It leverages the YouTube API, Data analysis, Natural Language Processing (NLP) and LSTM.

## Project Overview

- **Objective:** To provide accurate and domain-specific video recommendations on YouTube by analysing the video analyics - mainly comments.
- **Specialization:** Focuses on maintaining content relevance within the same domain.
- **Key Features:**
  - Data Analysis and Insights: Utilizes the YouTube API to collect and analyze video data, extracting insights from video titles, tags, and search texts using NLP techniques.
  - Video Statistics Analysis: Gathers and processes video statistics, including view counts and likes, employing data analysis tools such as Pandas and Numpy.
  - User Engagement Enhancement: Implements text similarity of video titles, search texts, tags and sentiment analysis on user comments.
  - Video Ranking: Calculates normalized scores for videos based on collected data and user engagement, ensuring the best video recommendations are presented to first-time viewers within the specific domain.
 
## Project outline/flow

1. *Data Extraction using YouTube Data API :*
   Extract data from YouTube videos using the YouTube Data API, including video title, tags, comments, likes, dislikes, and comment count.

2. *Collecting Search Texts :*
   Gather the search texts or prompts used to find these videos on YouTube.

3. *Domain Verification Using NLP :*
   Check if all the videos are from the same domain.
   Perform domain verification processes:
    - Remove punctuation, duplicates, and stop words.
    - Convert text to lowercase.
    - Apply lemmatization, tokenization, and similarity checks.
    - Utilize NLP techniques to verify domain similarity:
      - Verify title similarity using NLTK NLP and spaCy.
      - Verify tag similarity using NLTK NLP and spaCy.
      - Check if search texts of videos are similar.

4. *NLP Analysis on Comments of All Videos :*
   Conduct Natural Language Processing (NLP) analysis on video comments.
   Sub-steps for NLP analysis:
    - Collecting Video Comments:
      Gather comments from YouTube videos.
    - Storing Comments in Pandas DataFrame:
      Create a Pandas DataFrame to store comments for each video.
    - Slang Words Extraction:
      Scrape and store slang words in a dictionary.
    - Text Preprocessing:
      For each valid comment in the DataFrame, preprocess the text by:
      - Converting text to lowercase.
      - Handling HTML entities.
      - Removing punctuation, numbers, and emojis.
      - Dropping rows with missing or NaN values.
      - Expanding contractions.
      - Correcting spelling and grammar mistakes.
      - Removing irrelevant text such as usernames and links.
      - Handling slang words (scraped in the previous step).
    - Language Translation and Transileration:
      Identify and translate non-English words in comments into English and transilerate texts into corresponding languages.
    - Sentiment Analysis:
      Utilize pretrained models **(BERT,Vader Lexicon)** and **LSTM Trained Model** to perform sentiment analysis on each comment by *Ensembling Learning*.
    - Scoring and Normalization:
      Assign scores to comments and calculate the total normalized score for each video.
    - **Video Ranking**:
      Rank videos based on their normalized scores.

***Present the best video recommendations to first-time viewers within the specific domain.***

## Technology Stack

- **YouTube Data API:** Used for video retrieval and data gathering.
- **Natural Language Processing (NLP):** Applied to analyze video titles, tags, and sentiment analysis on comments.
- **Data Analysis:** Utilizes Python tools like Pandas and Numpy.
- **LSTM (Long Short-Term Memory):** Implements models for Sentiment Analysis.
- **Python Programming:** This code is developed using Python Language.

## How to Use

1. Clone the main ipynb notebook:
   `yt_rank_main.ipynb`
2. API Setup:
   Obtain API keys and credentials from the `YouTube Data API`. Insert your credentials in the project.
3. To run this project, you'll need to install the following Python libraries and dependencies:
   `pip install -r requirements.txt`
4. Download the required resources from `static` folder containing
   - `lang_code_fullname.json` containing language codes for all 179 known languages.
   - `slang_words.json` containing slang words more than 2000.
   - LSTM Model for Sentiment Analysis,
     - `sentiment_model.h5`
     - `tokenizer.pkl`

## Contributing
We welcome contributions from the community to enhance the system's capabilities and accuracy. Feel free to submit pull requests and report issues on GitHub.

> [!NOTE]
> The recommendations and insights provided in this project are based on Natural Language Processing (NLP) analysis and may not be infallible.

