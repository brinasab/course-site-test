---
title: "HW10: Analyzing text data"
date: 2022-11-21T13:30:00-06:00  # Schedule page publish date
publishdate: 2019-04-01

draft: false
type: post
aliases: ["/hw09-text_analysis.html"]

summary: "Collect text data and analyze it."
---



# Overview

Due by 11:59pm on November 29th.

# Accessing the `hw10` repository

Go [here](https://github.coecis.cornell.edu/cis-fa22) and find your copy of the `hw10` repository. It follows the naming convention `hw10-<USERNAME>`. Clone the repository to your computer.

# Your mission

Perform text analysis.

## Okay, I need more information

Perform sentiment analysis, classification, or topic modeling using text analysis methods as demonstrated in class and in the readings.

## Okay, I need some data sources

{{% callout note %}}

Some suggested text data you could use include:

* `gutenbergr`
* [Congressional Record for the 43rd-114th Congresses: Parsed Speeches and Phrase Counts](https://data.stanford.edu/congress_text)
* [Data for Everyone](https://www.figure-eight.com/data-for-everyone/) - a bunch of open-source data sets. Some contain text data, such as **New England Patriots Deflategate sentiment**.
* [Hate speech samples](https://github.com/t-davidson/hate-speech-and-offensive-language)
* [Last statements by Texas death row inmates](https://www.kaggle.com/mykhe1097/last-words-of-death-row-inmates)
* [Movie Review Data](http://www.cs.cornell.edu/people/pabo/movie-review-data/) - good for sentiment analysis
* [The musiXmatch Dataset](http://millionsongdataset.com/musixmatch/)
* Scrape tweets using `rtweet` (you know how to use the API now, right?)
* [State of the Union speeches](http://www.presidency.ucsb.edu/sou.php)
    * [`sotu`](https://github.com/statsmaths/sotu) - R package with all State of the Union speeches through 2016. Easier starting point.
* [Something from here](https://docs.google.com/spreadsheets/d/1I7cvuCBQxosQK2evTcdL3qtglaEPc0WFEs6rZMx-xiE/edit#gid=0) (h/t Chris Bail)

{{% /callout %}}

## How much do I really need to do?

Analyze the text for sentiment OR topic. Or build a statistical learning model using text features to predict some outcome of interest. You don't have to do all these things, just pick one. The lecture notes and [Tidy Text Mining with R](http://tidytextmining.com/) are good starting points for templates to perform this type of analysis, but feel free to **expand beyond these examples**.

# Submit the assignment

Your assignment should be submitted as an Quarto document using the `github_document` format. Whatever is necessary to show your code and present your results. Follow instructions on [homework workflow](/faq/homework-guidelines/#homework-workflow).

# Rubric

Needs improvement: Cannot get code to run or is poorly documented. Severe misinterpretations of the results. No effort is made to pre-process the text for analysis.[^justification]

Satisfactory: Solid effort. Hits all the elements. No clear mistakes. Easy to follow (both the code and the output). Nothing spectacular, either bad or good.

Excellent: Interpretation is clear and in-depth. Accurately interprets the results, with appropriate caveats for what the technique can and cannot do. Code is reproducible (i.e. if analyzing tweets, you have stored a copy in a local file so I can exactly reproduce your results as well as run it on a new sample of tweets). Uses a sentiment analysis or topic model approach not directly covered in class.

[^justification]: Or you provide no justification for keeping content such as numbers, stop words, etc.
