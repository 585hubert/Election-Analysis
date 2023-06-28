# Election Analysis Toolkit

This GitHub page contains a series of notebooks which perform various data processing tasks. The code in this repository uses the 2023 Dutch provincial elections<br>
<br>
The code works with CrowdTangle Data, and assumes that the data collected
pertains to either public pages of the political parties, or pages of specific politicians from certain political parties. Election data is assumed to be scraped from some other sources; I hope to include more notebooks in future scraping some of the larger and more well known datasites in that regard.<br>
<br>
## Functions
- *List_Relevant_Messages*: Filters CrowdTangle data over a temporal range. Since the Dutch Provincial Elections were on 15/03/2023, the data was gathered from 15/12/2022 until the election day.
- *remove_emojis*: [See here.](https://stackoverflow.com/questions/33404752/removing-emojis-from-a-string-in-python)
- *sentiment_pred_score*: Sentiment Analysis model using cardiffnlp/twitter-xlm-roberta-base-sentiment, a multilingual language model trained on 198 million tweets in 8 different languages. The model, given a text input, ascribes a probability that it is either positive, neutral, or negative. Make sure to assign a GPU when running this.
- *hatespeech_pred_score*: Hate Speech Analysis using Rewire/XTC, which is a fine-tuned version of the T-XLM-RoBERTa model on a multilingual hate speech dataset.
- *Filter_Stopwords*: Removes stopwords, which are words which bear more of a grammatical function than contributing to the sentence content, such as articles, conjunctions, prepositions, etc. In this example, a Dutch stopword set is used.
- *Make_Word_Cloud*: Using the standard python library, a wordcloud is generated with the amalgamted messages of a given facebook page.
- *PlottingParams.ipynb*: This analyses how well the Facebook groups performed in terms of general activity, using the CrowdTangle score (which is a measure of actual activity vs. Facebook's predicted activity).
- Correlation searching, wherein the various CrowdTangle parameters are compared against other electoral data to see whether any meaningful patterns can be seen between Facebook activity and real life results.
- General functions for deriving average value, min/max of a list and standard deviation.
- (Miscellaneous functions for directory management, opening csvs, plotting bar charts, etc).

Additionally, there is a notebook included which scrapes the election results from wikipedia (this is yet to be optimised), and subsequently plots the data onto a map using GeoPandas. Make sure to have a valid SHAPE file, the one used here is NDL_adm.

## Future Functions

- *Keyword Detection*: Functions which enable to track certain styles of language, thus allowing for rhetorical analysis, and determining styles of leadership.
- *Detection of Algorithmic Manipulation*: Machine learning techniques to determine if certain pages are using algorithmic manipulation to boost their online presence.
- *Ad Campaign Analysis* - Using Facebook's advertiser tracking, we can also determine how much money certain campaigns are spending on Facebook.


