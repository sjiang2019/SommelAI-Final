# SommelAI

### Steven Jiang and Tony DiPadova

## SommelAI Exploration and Visualization
The SommelAI Exploration and Visualization notebook contains the exploratory analysis that we performed on the dataset. The notebook contains the following:

* Overall distributions of price and quality
* Distributions and medians of price and quality by country and variety
* Correlational analysis of price and quality
* Textual description word frequencies
* Textual descriptions word cloud
* Topic modeling using Latent Dirichlet Allocation
* Aggregate metrics by state/country
* Geocoding wineries

## SommelAI Prediction
The SommelAI Prediction notebook contains various models for predicting price and quality with textual descriptions. In order to run the notebook, first download [Word2Vec](https://drive.google.com/file/d/0B7XkCwpI5KDYNlNUTTlSS21pQmM/edit). The notebook contains the following:

* Tokenizing and cleaning the textual descriptions
* Predicting Price from Descriptions
	* Multinomial Naive Bayes Classifier
	* SGD Classifier
	* Keras Classifier
	* Neural Network with LSTM and Word Embeddings 
* Predicting Quality from Descriptions
	* Multinomial Naive Bayes Classifier
	* SGD Classifier
	* Keras Classifier
	* Neural Network with LSTM and Word Embeddings 
	

## Website
We also visualize our findings and document our process on our [website](http://www.sommelai.com/). Our website contains the following:

* Interactive map with geocoded winery locations and aggregate metrics by state/country
* Select data visualizations
* An online tool for predicting wine quality and price using textual descriptions

## Dataset

The [Kaggle Wine Reviews](https://www.kaggle.com/zynicide/wine-reviews/data) dataset is composed of ~150,000 unique wine reviews and contains the following fields: country, description, designation, points, price, province, region 1, region 2, variety, and winery. Country, province, region 1, and region 2 refer to various degrees of specificity regarding the origin of the wine. Winery refers to the winery that produced the wine and designation refers to the vineyard within the winery from which the grapes were picked. The description field includes a description from a sommelier about the wine’s taste, smell, look, feel, etc. Finally, the variety field refers to the type of grape used to produce the wine. Using the aforementioned features, we hope to predict points, which is a proxy for quality, and price.

## Related Work
[Very quaffable and great fun: Applying NLP to wine reviews, Hendrickx et al.](www.aclweb.org/anthology/P16-2050)

Using textual reviews gathered from WineMag, Hendrickx et al. use lexical and semantic information to predict color, grape variety, price, and country of origin of various wines. Due to the fact that reviewers use similar descriptors, such as ‘fruity’, ‘notes of blackberry’, and ‘elegant’, wine reviews are consistent enough to draw conclusions about the wine itself. The researchers processed the textual data by combining a bag-of-words model with 100 topics generated from Latent Dirichlet Allocation and 100 clusters based on word embeddings from Word2Vec. The experiment resulted in high F-scores for each predicted category. Price was predicted categorically using ‘expensive’ and ‘cheap’ as the categories; however, the researchers mention that in the future it would be better to predict price as a regression task. Thus, we are hoping to extend their work by predicting price and quality as a regression task and by addressing the aforementioned questions.  

## Our Questions
* Are price and quality correlated?
* Do price and quality vary by region, variety, or winery? If so, to what extent?
* Can textual descriptions provided by sommeliers be used to predict wine price and quality?