# README.md

This is the repo for my Springboard capstone project files.

### Project Proposal: Formality in Reddit comments as a predictor of sarcasm
The problem of detecting sarcasm in text is of great interest to Natural Language Processing (NLP) practitioners and their clients. For example, consumer brands analyze online comments to gauge customer satisfaction and political campaigns seek to measure public reaction to policy proposals in user-created online content. Detecting sarcasm in text may also help disambiguate satire and related genres in the context of fake news detection.

When we use NLP techniques to measure sentiment in text, we think in terms of positive or negative (or neutral). Sarcasm, however, is a little more difficult to pin down. The literature is divided on how to define sarcasm, and on whether sarcasm is "net" positive or negative. Sometimes sarcasm is interpreted as positive by one person and negative by another. If sarcasm contains so much ambiguity that humans can't agree on what it is, do computers stand a chance of doing better?

In this study we analyze a large collection of online discussion forum comments to see if their degree of formality is associated with sarcasm. Formality here is defined as a text's conformance to certain standards of formal written English — specifically, correct spelling, proper punctuation, proper capitalization, formal grammar, and formal register (tone). If necessary in order to keep the study manageable, we will limit the number of elements of "formality" included as features in the model. Using these features as predictors, we seek to learn whether comments that are more (or less) formal than the average comment are more (or less) likely to be labeled as sarcasm.

Our dataset is A Large Self-Annotated Corpus for Sarcasm (SARC) <1>. SARC contains over 1 million sarcastic comments in a balanced set (equal number of non-sarcastic comments) and also an unbalanced set (100+ million non-sarcastic comments, the ratio found in the wild). SARC data is labeled via the self-annotating feature of Reddit by which authors indicate via an "/s" notation that all or part of their comment should be read as sarcasm.

Hypothesis: Reddit authors tend to spend more time crafting their sarcastic comments than their non-sarcastic comments, and thus sarcastic comments are characterized by greater degrees of formality.
- A counter hypothesis: Reddit authors tend to spend _less_ time writing their sarcastic comments, dashing them off in fits of righteous indignation, and thus include _less_ formality in their sarcastic comments than in their nonsarcastic comments.
- Either hypothesis, if true, would likely be helpful in predicting sarcasm.

We start by using one or two Supervised Machine Learning classification techniques such as Logistic Regression to establish a baseline for our model's accuracy in predicting sarcasm. We then use several Deep Learning techniques such as Deep Convolutional Neural Networks (CNN) and Long Short-Term Memory Recurrent Neural Networks (LSTM, RNN) to see if we can improve the model's accuracy. The final model is then productionized and deployed as a web service via an API.

Minumum computational resources needed to do this project: 

- Processing power (CPU): 4+ CPUs
- Memory: 32GB
- Specialized hardware such as GPUs: 1 GPU


This capstone project is undertaken in partial fulfilment of the requirements for the AI/Machine Learning Engineer Career Track Bootcamp at Springboard, under the mentorship of Jeff Hevrin.


<1> Unpublished SARC, Mikhail Khodak and Nikunj Saunshi and Kiran Vodrahalli, A Large Self-Annotated Corpus for Sarcasm, https://arxiv.org/abs/1704.05579, 2017.


### Dataset
The SARC dataset is hosted at https://nlp.cs.princeton.edu/SARC/0.0/main/.

We use version 0.0/main files, the balanced set for EDA and traditional ML techniques and the the unbalanced set for DL models. Files in main have been cleaned and filtered; note file sizes for raw files compared to main files in table below:

Index of /SARC/0.0/main		main	raw

Name						Size	Size
sarc.csv.bz2				11G		59G
stats.json					13M		23M
test-balanced.csv.bz2		19M	
test-unbalanced.csv.bz2		2.3G	
train-balanced.csv.bz2		78M	
train-unbalanced.csv..>		8.9G	
