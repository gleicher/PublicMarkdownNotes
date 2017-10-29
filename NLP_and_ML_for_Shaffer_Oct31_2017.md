# Statistical Language Processing
Some notes to guide the conversation in Shaffer's group meeting for October 31, 2017.

## Some Machine Learning Vocabulary

### Some "types" of "Learning" Tasks / Models
+ description
+ prediction 
+ clustering (figuring out what groups there are)
+ confirmation (statistical explanation)
+ interpretation (explanation in common sense)
+ generative models (as generators, as predictors/classifiers)
+ embeddings

Some distinctions worth noting:
+ classification vs. clustering
+ classification vs. regression
+ predict vs. explain
+ generalization
+ generate vs. discriminate
	+ P(X|Y) vs. P(Y|X)
	+ generate: what is the distribution of things in the world? (given the class, how likely is this thing)
	+ discriminate: given this thing, how likely is it to be in the class

### More words we'll probably use
+ performance metrics
	+ simple (accuracy, precision, recall, MCC, ...)
	+ confidence-based AUC/PR, AUC/ROC
+ information gain
+ feature selection
+ feature engineering

## Some Basic Thoughts on Natural Language Processing
Warning: I am not a language expert.

### Why is language hard? 
A few top ones... you can think of more
+ context dependent
+ ambiguous (at all levels)
+ redundant (designed for errors)
+ multi-layered (syntax <-> semantics <-> higher level semantics)
+ many ways to say things
+ reference to other things
+ other communications modalities (intonation, gesture, common reference)
+ reference to shared knowledge 

### Low level work operations
+ tokenization
+ standardization
+ lemmatization (remove endings)
+ stemming (as a subset of lemmatization)
+ tagging / labeling
+ "Stop Words" removal

### Some standard tasks
+ sentiment analysis

### Some basic strategies
+ Bag of words models
+ Bag of feature models
+ Parsed representations
+ Semantic representations

## Some Statistical Language Stuff To Know

Operations on Bag of Words models
+ Text Frequency
+ Inverse Document Frequency
+ TF/IDF
+ Why not naively 
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTIwMTcyNjY4NzddfQ==
-->