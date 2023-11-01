# YouTube Video Recommendation for Domain-Specific Content

Welcome to the YouTube Video Recommendation System project! This comprehensive system is designed to offer personalized and relevant video recommendations within a specific content domain. It leverages the YouTube API, data analysis, Natural Language Processing (NLP), and machine learning to enhance the user experience.

## Project Overview

- **Objective:** To provide accurate and domain-specific video recommendations on YouTube by analysing the video analyics - mainly comments.
- **Specialization:** Focuses on maintaining content relevance within the same domain.
- **Key Features:**
  - Data Analysis and Insights: Utilizes the YouTube API to collect and analyze video data, extracting insights from video titles, tags, and search texts using NLP techniques.
  - Video Statistics Analysis: Gathers and processes video statistics, including view counts and likes, employing data analysis tools such as Pandas and Numpy.
  - User Engagement Enhancement: Implements machine learning models for spam comment detection and sentiment analysis on user comments.
  - Video Ranking: Calculates normalized scores for videos based on collected data and user engagement, ensuring the best video recommendations are presented to first-time viewers within the specific domain.
 
## Project outline/flow

1. Data Extraction using YouTube Data API
   Extract data from YouTube videos using the YouTube Data API, including video title, tags, comments, likes, dislikes, and comment count.

2. Collecting Search Texts
   Gather the search texts or prompts used to find these videos on YouTube.

3. Domain Verification Using NLP
   Check if all the videos are from the same domain.
   Perform domain verification processes:
    - Remove punctuation, duplicates, and stop words.
    - Convert text to lowercase.
    - Apply lemmatization, tokenization, and similarity checks.
    - Utilize NLP techniques to verify domain similarity:
      - Verify title similarity using NLTK NLP and spaCy.
      - Verify tag similarity using NLTK NLP and spaCy.
      - Check if search texts of videos are similar.

4. NLP Analysis on Comments of All Videos
   Conduct Natural Language Processing (NLP) analysis on video comments.
   Sub-steps for NLP analysis:
    - Collecting Video Comments:
      Gather comments from YouTube videos.
    - Storing Comments in Pandas DataFrame:
      Create a Pandas DataFrame to store comments for each video.
    - Slang Words Extraction:
      Scrape and store slang words in a dictionary.
    - Spam Comment Detection:
      Implement machine learning models to filter out spam comments.
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
    - Language Translation:
      Identify and translate non-English words in comments into English.
    - Sentiment Analysis:
      Utilize pretrained models to perform sentiment analysis on each comment.
    - Scoring and Normalization:
      Assign scores to comments and calculate the total normalized score for each video.
    - **Video Ranking**:
      Rank videos based on their normalized scores.

Present the best video recommendations to first-time viewers within the specific domain.

## Technology Stack

- **YouTube Data API:** Used for video retrieval and data gathering.
- **Natural Language Processing (NLP):** Applied to analyze video titles, tags, and sentiment analysis on comments.
- **Data Analysis:** Utilizes Python tools like Pandas and Numpy.
- **Machine Learning:** Implements models for spam comment detection.
- **Python Programming:** The system is developed using Python.

## How to Use

1. Clone this repository to your local machine:
   `pip install -r requirements.txt`
2. To run this project, you'll need to install the following Python libraries and dependencies:
   `pip install -r requirements.txt`
3. Run the Application:
   `python main.py`

## Contributing

We welcome contributions from the community to enhance the system's capabilities and accuracy. Feel free to submit pull requests and report issues on GitHub.



   

