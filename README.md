# Food Review System

<h1>Business/Real-world Problem</h1>
  
  <h2> Problem Statement </h2>
  
  <p>
    Given a food review by any user in text, classifying into different categories like Positive, Neutral and Negative . 
</p>

Dataset provided by Amazon contains food review and its ratings.
</p>
<p>
<b> Source: </b> https://www.kaggle.com/snap/amazon-fine-food-reviews
</p>

<h2>Real-world/Business objectives and constraints.</h2>


    1. Minimize multi-class error.
    2. Multi-class probability estimates(feature importance).
    3. No hard latency requirements.
    

<h3>Data Overview</h3>

<li> Source : https://www.kaggle.com/snap/amazon-fine-food-reviews </li>
<li>This dataset consists of reviews of fine foods from amazon. The data span a period of more than 10 years, including all ~500,000 reviews up to October 2012. Reviews include product and user information, ratings, and a plain text review. It also includes reviews from all other Amazon categories.</li></ol></li> 
    
<li>Reviews.csv: Pulled from the corresponding SQLite table named Reviews in database.sqlite  </li>
<li>database.sqlite: Contains the table 'Reviews' </li>

### Data includes:
* Reviews from Oct 1999 - Oct 2012
* 568,454 reviews
* 256,059 users
* 74,258 products
* 260 users with > 50 reviews:

<h2>Mapping the real-world problem to an ML problem</h2>

<p>
    There are rating given from 1 to 5, posing this to a Multi class classification problem. Ratings, 1 and 2 as Negative, 3 as Neutral, 4 and 5 as Positive.    
</p>

<h3>Performance Metric</h3>

Metric(s): 
* Multi class log-loss 
* Confusion matrix 
* AUC

<h3>Machine Learing Objectives and Constraints</h3>
<p> Objective: Predict the probability of each data-point belonging to each of the three classes.</p>
  
Constraints:
  * Class probabilities are needed
  * Penalize the errors in class probabilites => Metric is Log-loss


# Results
 Test AUC is 96
 
# Conclusion
<p>Used Bert model for feature extraction and passed these features to LSTM layers </p>
<p>For feature extraction from Bert, Used different combinations of hidden layers and its features like concatenation and average instead of CLS representation. This way of fine tuning has shown good performance and eventually a better generalized model </p>
<p> Used both TensorflowHub and HuggingFace for implementation </p>
  
