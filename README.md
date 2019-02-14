<a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-nc-sa/4.0/88x31.png" /></a><br />This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/4.0/">Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License</a>.

# Sentiment Annotation Guidelines

This repository contains:
 
- RuSentiment dataset for sentiment analysis of Russian social media;

- guidelines for annotation of sentiment in social media, with which RuSentiment was produced. There are two versions, one with examples in Russian (VKontakte social network) and one with English examples from Twitter. The guidelines were prepared as part of [RuSentiment project](http://text-machine.cs.uml.edu/projects/rusentiment/) by [Text Machine Lab for NLP](http://text-machine.cs.uml.edu). 

Both RuSentiment and the guidelines are available for non-commercial use.

Project page: http://text-machine.cs.uml.edu/projects/rusentiment/

Paper: "Rogers, A., Romanov, A., Rumshisky, A., Volkova, S., Gronas, M. and Gribov, A., 2018. RuSentiment: An Enriched Sentiment Analysis Dataset for Social Media in Russian. In Proceedings of COLING 2018 (pp. 755-763)." [PDF](http://aclweb.org/anthology/C18-1064) | [BibTex](https://dblp.uni-trier.de/rec/bibtex/conf/coling/RogersRRVGG18)

Highlights of our annotation policy:

 - negative and positive sentiment classes cover both implicit and explicit sentiment, both for expressing emotion and attitudes;
 - neutral class (unmarked for sentiment);
 - speech act class: social media posts often include formulaic greetings, thank-you posts and congratulatory posts, which may or may not express the actual sentiment of the sender;
 - "skip" class for unclear cases, noisy posts, content that was likely not created by the users themselves (poems, lyrics, jokes etc.).
 - cases of mixed sentiment are annotated for the dominant sentiment of the post, and the guidelines cover 6 frequent cases of mixed sentiment to improve inter-annotator agreement;
 - hashtags and smileys are *not* treated as automatic sentiment labels.
 
For Russian these guideines yielded annotation speed of 250-350 posts per hour, with Fleiss kappa of 0.654 for randomly selected posts. See paper for details on how active learning influenced the inter-annotator agreement.
