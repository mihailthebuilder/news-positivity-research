# News Positivity Research

This is a project that examines the performance of five pre-trained models for scoring the positivity of news sites:
- [AFINN](https://github.com/fnielsen/afinn)
- [VADER](https://github.com/cjhutto/vaderSentiment)
- [DistilBERT](https://huggingface.co/distilbert-base-uncased-finetuned-sst-2-english)
- [roBERTa](https://huggingface.co/cardiffnlp/twitter-roberta-base-sentiment)
- [BERTweet](https://huggingface.co/cardiffnlp/bertweet-base-sentiment)

AFINN and VADER are two popular dictionary-based models. DistilBERT is the default sentiment analysis model offered by Hugging Face in their [quick tour](https://huggingface.co/transformers/quicktour.html). roBERTa and BERTweet are two of the best performing models in the [TweetEval benchmark study](https://arxiv.org/pdf/2010.12421.pdf).

We're only looking at the landing pages (e.g. https://bbc.co.uk) and not the article pages (e.g. https://www.bbc.co.uk/news/uk-england-birmingham-58282348).

# [The data notebook](./data.ipynb)

# [The model notebook](./model.ipynb)

The [test.csv](./test.csv) file contains the test dataset. The text content in the dataset was gathered using the [data.ipynb](./data.ipynb) script, which was run on 3 websites: [bbc.co.uk](https:/bbc.co.uk), [thecanary.co](https://thecanary.co) and [positive.news](https://positive.news). For each text piece, I manually assigned a sentiment score of -1 if it was negative, and +1 if it was neutral or positive.