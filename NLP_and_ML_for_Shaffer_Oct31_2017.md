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

Some classes of situations:
+ supervised learning
+ unsupervised learning
+ semi-supervised learning
+ active learning
+ interactive learning

Some distinctions worth noting:
+ classification vs. clustering
+ classification vs. regression
+ predict vs. explain
+ generalization
+ generate vs. discriminate
	+ P(X|Y) vs. P(Y|X)
	+ generate: what is the distribution of things in the world? (given the class, how likely is this thing)
	+ discriminate: given this thing, how likely is it to be in the class

Some specific models:
+ prediction as function approximation
	+ generalization
+ Linear models (classifiers, regressors)
	+ SVMs vs. Linear Disciminants (LDA) vs. Logistic Regression
+ Non-Linear models (and kernels)
+ Rule-based models
+ Decision Trees
+ Neural Network Models
	+ "Deep"-ness
	+ Fancy architectures (convolution, recurrence, LSTM)

Performance Analysis:
+ testing generalization vs. testing ...
+ cross validation, bootstrapping, holdout, ...

User-Centric Issues in Modeling and ML
+ Interpretability
+ Explanations
+ Interpretable Models

### More words we'll probably use
+ performance metrics
	+ simple (accuracy, precision, recall, MCC, ...)
	+ confidence-based AUC/PR, AUC/ROC
+ information gain
+ feature selection
+ feature engineering
+ latent features / concepts

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
+ Why not naively use the document/word matrix?
	+ sparsity issues
	+ synonyms, other ways to say it, ...

Alternatives to Bag of Words
+ Sliding windows
+ chunked texts
+ Skip-Grams
+ recursive models

Simple Methods - why/why not
+ rules/dictionaries
+ interpretability

Latent Semantic Analysis (LSA)
+ Do PCA on Word Vector Matrix

Topic Modeling
+ as a general concept
	+ documents in topics
	+ documents as mixtures of topics
	+ topic space as an embedding for documents
	+ words as evidence that a document is in a topic
+ Latent Dirichlet Allocation (LDA) models
	+ The Naive version: 
		+ document matrix (embedding), word matrix (embedding)
	+ The "real" version (with the dice game)
+ Serendip & Serendip Slim
	+ https://github.com/uwgraphics/SerendipSlim
	+ http://vep.cs.wisc.edu/serendip/
+ What topic models is/is not good for
	+ Why topic models are not good for classification
+ Fancier forms of topic models
	+ Semi-Supervised Topic Models
	+ Na
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTE4MTY1NTgyNzddfQ==
-->