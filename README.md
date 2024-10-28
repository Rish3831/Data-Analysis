# ECC Topic Modeling and Text Summarization Project

This project focuses on analyzing survey responses collected by Essex County Council, using topic modeling and text summarization techniques to uncover key themes and actionable insights. The report details the data collection, preprocessing, topic modeling, and summarization methods employed.

## Project Overview

The primary objectives of this project are to:
1. **Identify Main Topics**: Use Latent Dirichlet Allocation (LDA) to reveal underlying topics within survey responses.
2. **Summarize Text**: Apply abstractive text summarization techniques to condense responses into actionable insights.

## Table of Contents

- **Data Collection**
- **Data Preprocessing**
- **Topic Modeling with LDA**
- **Abstractive Text Summarization**

## Data Collection

Data was gathered through an online survey hosted on Citizen Space, where participants provided feedback on various parts of Essex County Council's draft strategy. Responses included both agreement/disagreement ratings and free-text comments. The collected data consisted of raw text requiring extensive preprocessing before analysis.

## Data Preprocessing

Preprocessing steps included:

1. **Dropping NaN Values**: Removing rows or columns with missing values to ensure data integrity.
2. **Lowercasing**: Converting text to lowercase to standardize text data.
3. **Special Character Removal**: Eliminating special characters to reduce noise.
4. **Stopword Removal**: Removing common words (e.g., "and", "the") that do not contribute to the core meaning of responses.
5. **Lemmatization**: Converting words to their base form using NLP libraries to ensure uniformity.
6. **Vectorization**: Transforming text data into numerical format using Gensim for compatibility with machine learning models.

## Topic Modeling with LDA

Latent Dirichlet Allocation (LDA) was used to identify topics within the survey responses:

- **Model Building**: Preprocessed data was added to the LDA model to assign probabilities to words, facilitating topic formation.
- **Optimal Topic Count**: Set at 15 topics to balance coverage and specificity, providing a clear thematic structure without overcomplicating the model.
- **Output**: Generated topics represent distinct themes within the survey data, enabling ECC to identify major concerns and areas for improvement.

## Abstractive Text Summarization

Text summarization was performed to condense lengthy responses into actionable summaries:

1. **Tokenization**: Sentences were segmented for summarization using the `pipeline` function from the Hugging Face Transformers library.
2. **Summarization Process**: Relevant sentences were selected based on topic scores and combined to create short summaries.
3. **Final Action Points**: Leveraging the Open Llama 7B model from Hugging Face, summaries were further condensed into key action points using a pre-configured prompt.

## Key Tools and Libraries

- **NLTK**: Used for stopword removal and lemmatization.
- **Gensim**: For text vectorization and LDA modeling.
- **Transformers**: Hugging Face library for abstractive text summarization.
- **Open Llama 7B**: Model for generating concise action points.

## Usage

1. **Data Preprocessing**: Run preprocessing scripts to clean and vectorize the survey responses.
2. **Topic Modeling**: Apply the LDA model on preprocessed data to generate topics.
3. **Text Summarization**: Use the summarization pipeline to extract main points from responses, then condense further with Open Llama.

## Results and Insights

The project reveals key topics in survey responses and provides brief summaries of each. These insights help inform ECC on public opinion, facilitating targeted actions to improve service and communication.

## Contact

- **Name**: Rishwanth Mithra
- **Email**: rishwanth.mithra22@gmail.com
- **Phone**: 07424809676

---

This project provides a systematic approach for Essex County Council to analyze survey responses and derive actionable insights efficiently.
