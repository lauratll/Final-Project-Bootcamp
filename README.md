<img src="https://bit.ly/2VnXWr2" alt="Ironhack Logo" width="100"/>

# An NLP Analysis on the Reviews of a restaurant Scrap from Tripadvisor
*Laura Trapero*

**Data Analytics Bootcamp, May 2021, Remote**

## Content
- [Project Description](#project-description)
- [Hypotheses / Questions](#hypotheses-questions)
- [Dataset](#dataset)
- [Cleaning](#cleaning)
- [Analysis](#analysis)
- [Model Training and Evaluation](#model-training-and-evaluation)
- [Conclusion](#conclusion)
- [Future Work](#future-work)
- [Workflow](#workflow)
- [Organization](#organization)
- [Links](#links)

## Project Description

Understanding customers’ feedback and knowing what your strengths and weaknesses are is key to any business.

In this projects we will scrap from Tripadvisor the reviews from a sustainable restaurant in Amsterdam (De Kas) and use NLP to get quick and valuable insights. A model will be constructed to predict the score of the reviews, to help us understand the imporantance of the features on determinining weather a reviews is good or bad. 

## Questions
* How can a restaurant get valuable insights from their costumers reviews?
* How are the features better valuated by costumers? 
* Pinpoint possible problems and increase the deliver a more customized customer experience. 


## Dataset
* The data of the reviews was scrap from Tripadvisor. It has 1038 rows/reviews with its ID, Date, Score and Title.
* It has no duplicates and the majority of the reviews are positive. There is a major class unbalanced on the Rated Score.
*

## Cleaning
* Clean text for NLP methods:
	- remove special characters
	- remove extra spaces
	- remove digits
	- remove urls's
	- convert to lower case

* Pre-processing:
	- Create a corpus
	- Tokenization
	- Lemmatization
	- Remove non-meaningful words


	- Classify reviews in:
		-   positive reviews > 3
		-   negative reviews < 3

	- Down & up sampling 

## Analysis
* Metrics as the lenght and number of characters are measure to include in the model.
* A bag of words technic is used, frecuency of words, to be represented in a word cloud in positive and negative reviews.
* TF-IDF ( Term Frequency- Inverse Dense Frequency) with ngrams 2 and 3 is calculated to obtain the most weighted words/combination of words accrording to the TF-IDF score. Those are used also to be entered in the model. 
* Those words are used to analize content with more meaning when using 2-3 g to pintpoint useful customers feedback.

## Model Training and Evaluation


* Random forest models and logistic regression models for classification are implemented. Cross validation is used and the performance of the models is compare chaangind its hyperparamenters. 
* The most frequent word obtaind from the words frecuency and TF-IDF are encoded accroding to the presence in each review(1,0), and added to the data frame to be able to train the model.
* Models are trained with the 5 class of score and with scores transformed to binary variable (positive, no positive). 
* The results are really bad. Bad predictions, with really low kappa values.
* Predicts better the majority class
 

## Conclusion

* We were able to gather lots of insights from the reviews.
* Other models need to be applied.
* More data need to be gather.

## Future Work

- Get more reviews from other sites like Yelp, google and local ones.

- Use more complex models and NN 

- Time Series Analysis

- Themes Impact Analalysis

- NLP on the Reviews Title

- Embeding methods: represent reviews as vectors representation to be able to apply clustering algorithms to detect topic and other methods like Word2Vec Architecture Implementation (word representations in Vector Space )


## Links


[Repository](https://github.com/lauratll/Final-Project-Bootcamp)   
[Trello](https://trello.com/b/eKsF60Lz/final-project-bootcamp)  
