# Sparkify Project

### Motivation
Customers just do not run a business, they keep businesses alive. While at times, it is easy to gather new customers, businesses run out of ideas or do not adapt to retain their sudden growth. Customer Retention is the formal term for retaining customer growth and minimizing churn in a business. Businesses these days use a variety of methods to minimize the churn rate like segmented marketing, tailored surveys, and personal interactions. But the factor beneath these methods is the data about the customers. The challenge is to find the right data and analyze a pattern/trend with churning customers.

### Description
This project will be using an event log data in JSON format from a music streaming service called Sparkify. The log contains different events performed by users in the music app. It leverage pySpark to build a model which can predict user churn.

### Outcome
The project builds three models such as Logistic Regression, Gradient Boosted Trees(GBT) and Random Forest Classifier.

Out of the three classifiers, Gradient Boosting Trees(GBT) classifier has accuracy and an F1 score of 94%. These results are on a subset of the large dataset. When run on a 12GB original dataset using the AWS EMR cluster, we have an accuracy of 83% and an F1 score of 80%.

With this model, it would be better for the company to look into the important features derived from GBTs such as total songs listened, thumbs up event and minimizing help page visits or giving good help articles would actually prevent the users from churning. Also, when it comes to predicting churn for music apps, it would also be good to consider the time pattern of app usage. For example, at what time, day, or part of the year users use the app a lot. When the log data is given for an entire year, this information would be much more useful for predicting churn.

### Packages used
pyspark, pandas, numpy, seaborn, datetime, matplotlib

### File Structure
- `Sparkify.ipynb` 
    - Jupyter notebook file run on the local machine with the small dataset (128 MB). This notebook contains exploration and model tuning methods
- `Sparkify_EMR.ipynb`
    - Jupyter notebook file run on AWS EMR cluster with the entire dataset(12 GB). This notebook contains the preprocessing and finalised model results.

### References

Thanks to Udacity for providing the opportunity and learning resources to work on this project. Following links/resources helped me to build this project successfully
 
- https://knockdata.github.io/spark-window-function/
- https://www.analyticsvidhya.com/blog/2016/02/complete-guide-parameter-tuning-gradient-boosting-gbm-python/
- https://stackabuse.com/gradient-boosting-classifiers-in-python-with-scikit-learn/
- https://spark.apache.org/docs/2.2.0/ml-classification-regression.html#gradient-boosted-trees-gbts
- https://stackabuse.com/gradient-boosting-classifiers-in-python-with-scikit-learn/
