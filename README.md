## [Sarcasm Detection Classification From Headline News](#Introduction-1)
### Introduction 1
Sarcasm is a form of verbal irony that is intended to **mock** or convey the opposite meaning of what is actually said. Sarcasm can be risky in news headlines as it can
easily be **misinterpreted** or **offend certain readers** who might feel that the news organization is making light of a serious issue or mocking a particular group.
Hence, readers may be less likely to read or share the organization's content in future leading to losses and above all **harm the reputation**
of the news organization. It can also **undermine the credibility and professionalism of news organization** as it can come across as
unprofessional or biased. Threfore it is important for news organizations to carefully detect sarcasm from their headlines so as to consider the potential effect of it.
### Overview
The dataset has 12506 observations and two features. The **headlines column** contains all the news headlines whereas target column consists of class labels for each news headline.
The dataset is **balanced** so there is no need for sampling. The main objective is to build a binary classification model that can successfully detect 
whether or not a news headline is sarcastic. As a data scientist for a news agency, I aim to to build a model
that will optimize the news headlines in a way that it does not create an impression of sarcasm for a reader.
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
