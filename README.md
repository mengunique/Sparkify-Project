
### To be or not to be? Sparkify project on User Churn Prediction


### Motivation and synopsis
This project is part of the requirement for Data Scientist Nanodegree on Udacity as the final Captone Project. <br/>
Sparkify is a Music App. The sample dataset is a user behavioral log file with multiple user behavours like “add to playlist”, “thumbs up”, “downgrade”, “logout” and “cancel”. In the real-world setting, Sparkify company would understand what drives users to cancel the service, and potentially prevent user churn. 

Udacity created this case mimicking real-life app like Spotify or Pandora, and due to the sheer size of data, the project is carried out using Apache Spark distributed cluster-computing framework, using Python API for Spark, PySpark.

[Problem Statement]
The objective of the problem is to predict user cancellation or user churn rate. This is a good classification problem, because user either churn (1) or not (0). We will need to understand the data, and identify factors that will influence churn rate. 

### File Descriptions
Credits to Udacity for creating this problem and provided a smaller sample dataset to be played at local machine. 

There are 3 different folders with 3 files each 
- mini_sparkify_event_data.json (sample data file for 225 user behaviours log; data not uploaded as this is a standard file provided)
- Sparkify.ipynb
- README.md

### Analysis Results in Brief
We have selected 6 columns into the models.The first four coloumns are string datatype, so we have converted that into numeric values using String Indexer and One Hot Encoding. 
 1:- Gender
 2:- UserAgent
 3:- Status
 4;- Page
 5:- Level
 6:- ItemInSession

Splitting the dataset into train test set on a 80/20 basis, and perform grid search with 3-fold cross validation by fitting the defined CrossValidator object on the training data.

After running 3 classification models including Logistic Regression, Random Forest and Gradient Boost Tree models, we have used F1 score as a leading indicator to evaluate model rubustness. 
<br/>
Logistic Regression Model F1:0.8596 <br/>
Random Forest  Classifier F1:0.8455 <br/>
GBTClassifier  Classifier F1:0.9076 <br/>

Model accuracy result shows: <br/>
Logistic Regression Classifier Accuracy:0.8787 <br/>
Random Forest  Classifier Accuracy:0.8781 <br/>
GBTClassifier  Classifier Accuracy:0.9167 <br/>

Thus, GBTClassifier is a preferred model in this case. 

### Acknowledgements
A special thanks to a few super blogs on github and medium to help me better;
https://medium.com/@jiewwantan/sparkify-user-churn-prediction-using-pyspark-32be364e8296
https://medium.com/@lukazaplotnik/sparkify-churn-prediction-with-pyspark-da50652f2afc
        
### Author
April Li
- https://github.com/mengunique
- medium blog: 
https://medium.com/@limengapril/to-be-or-not-to-be-sparkify-project-on-user-churn-prediction-7dd58352cf88?sk=73f04486bbea47e8a61d9e0ee6954fb9


### Installation Remark 
The Jupyter Project highly recommends users to install [Anaconda](https://www.anaconda.com/distribution/)
since it conveniently installs Python, the Jupyter Notebook, and other commonly used packages for scientific computing and data science.

Use the following installation steps:
1. Download Anaconda.
2. Install the version of Anaconda which you downloaded, following the instructions on the download page.
3. To run the notebook:
jupyter notebook:
•Sparkify.ipynb

### Python libraries

The Jupyter Notebook files requires the following Python libraries:
1. Python 3
2. Pyspark
3. Pandas
4. Matplotlib
5. Seaborn
6. Jupyter notebook
