## [Sarcasm Detection Classification From Headline News](#Introduction-1)
## [Sentiment Analysis for a Netflix Original show Reviews](#Introduction-2)
### Introduction 1

Sarcasm is a form of verbal irony that is intended to **mock** or convey the opposite meaning of what is actually said. Sarcasm can be risky in news headlines as it can
easily be **misinterpreted** or **offend certain readers** who might feel that the news organization is making light of a serious issue or mocking a particular group.
Hence, readers may be less likely to read or share the organization's content in future leading to losses and above all **harm the reputation**
of the news organization. It can also **undermine the credibility and professionalism of news organization** as it can come across as
unprofessional or biased. Threfore it is important for news organizations to carefully detect sarcasm from their headlines so as to consider the potential effect of it.

### Overview

The **main objective** is to build a binary classification model that can successfully detect 
whether or not a news headline is sarcastic. As a data scientist for a news agency, I aim to build a **Feed Forward Deep Neural Network** model
that will classify any new headlines as either Sarcastic or Not sarcastic to optimize the news headlines in a way that it does not create an impression of sarcasm for a reader.

--

The dataset has 12506 observations and two features. The **headlines column** contains all the news headlines whereas target column consists of class labels for each news headline.
The dataset is **balanced** so there is no need for sampling.
#### Summarization
1. I **cleaned** the data of any missing values and applied `langdetect` function to underatnd which language the data is in.
2. **Text Preprocessing** - just like data preprocessing, text preprocessing involves cleaning **text** data of all the noise anf wrong formats and tranforming text into a clean
clean and consistent format. Some of the techniques I used include: 
    * Lower Case conversion
    * Removing special characters
    * Tokenization
    * Filtering Stop words
    * Lemmatization                                                                    
all were achieved by the `nltk` library in python.

3. Text features was converted to a corresponding numerical representation using the **TF-IDF** method.
4. I then build the Feed Forward Deep Neural Network,consisting of 3 layers; for the binary classification problem, *sigmoid* activation function was used in the output
layer, a loss function of *binary_crossentropy* and *optimizer* of adam used.
5. Hyperparameters: epoch and batch size was set and the model was trained with a validation split.
6. An accuracy of about 99% was obtained, and compared to the text accuracy which was around 95%, suggesting that the model was pretty good. I then predicted on new headlines
text.
---

### Introduction 2
Sentiment analysis, also known as opinion mining, is a technique used to **analyze** and interpret the **emotional tone** or **attitude expressed in text data**.
It involves the use of natural language processing, machine learning, and computational linguistics to identify and extract subjective information from text.
Sentiment analysis is important for several reasons:
   * Understanding customer feedback: By analyzing customer feedback, businesses can identify the strengths and weaknesses of their products or services, as well as        areas for improvement.
   * Improving customer experience: By understanding customer sentiment, businesses can take steps to improve their customer experience, which can lead to increased        loyalty and higher customer satisfaction
   * Brand monitoring: Sentiment analysis can help businesses monitor their brand reputation online, by identifying negative sentiment and taking steps to address          issues that may be causing dissatisfaction among customers.
   * Crisis management: Sentiment analysis can also be useful in identifying potential crises before they become public, allowing businesses to take proactive measures      to address issues and prevent negative sentiment from spreading.
Overall, sentiment analysis can provide valuable insights into consumer attitudes and opinions, allowing businesses to make informed decisions and take proactive measures to improve their products, services, and reputation.
### Overview

The **main objective** is to perform sentiment analysis on Netflix movie reviews is to understand the emotional tone and attitude of the viewers towards the movies. By analyzing the sentiment of the reviews, Netflix can gain insights into how viewers perceive and react to their content.
For example:
   * If a particular movie receives overwhelmingly **positive reviews**, Netflix can use that information to promote the movie to other viewers who are likely to enjoy    * Similarly, if a movie receives **negative reviews**, Netflix can use that information to improve its recommendations and identify areas for improvement.
  
--

This dataset contains 25000 Text data Reviews and two features. The Text column contains all the customer reviews on a particular show, say Netflix Original show and a Target column that contains class labels for each of the reviews. The dataset is balanced and so there was no need for resampling.
#### Summarization

After perfoming Data Cleaning to the entire dataset and confirming that the reviws are in one common language, I went ahead and preprocess the Text data uisng various techniques such as: Lower case conversion, Removing special Characters/Punctuations, Word Tokenization, Removing stop words and Lemmatization.
I then visualized the most commonly used words in all Reviews using WorldCloud.
Lastly I performed Sentiment Analysis using the [VADER](https://towardsdatascience.com/sentimental-analysis-using-vader-a3415fef7664) method.

--
I was able to classify each of the reviews as either Negative or Positive based on their Polarity scores and the compound score, which is  an aggregation of (negative, neutral and positive scores).
I ran a random unseen review on the Vader function, and got the polarity scores.


