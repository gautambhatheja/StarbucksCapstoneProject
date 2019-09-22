# StarbucksCapstoneProject
Capstone project for Udacity Nanodegree

### Table of Contents
1. [Installation](#installation)
2. [Project Motivation](#motivation)
3. [File Descriptions](#files)
4. [Instructions to implement the project](#instructions)
5. [Results](#results)
6. [Licensing, Authors, and Acknowledgements](#licensing)

## Installation <a name="installation"></a>
The code is written in python 3.6. And you will have to install the following libraries for the project:
* numpy
* pandas 
* json 
* datetime
* xgboost
* sklearn
* matplotlib
* json

## Project Motivation<a name="motivation"></a>
I was intrigued by the promotional offers that companies like Starbucks give to its customers. I found some questions very interesting like Who like Starbucks ? Do the offers given by Starbucks affect thier sales ? But the question that really caught my attention was, How much a typical person spend there ? And how well can I predict the expenditure ? So, I decided to explore myself, and it resulted in this project. 

## File Descriptions<a name="files"></a>

There are 2 files and one folder in this repository. They are:

1) Data Folder:
The data set that I have used contains simulated data that mimics customer behavior on the Starbucks rewards mobile app. This data set is a simplified version of the real Starbucks app because the underlying simulator only has one product whereas Starbucks actually sells dozens of products.

The data is contained in three files:

i) portfolio.json - containing offer ids and meta data about each offer (duration, type, etc.)
* id (string) - offer id
* offer_type (string) - type of offer ie BOGO, discount, informational
* difficulty (int) - minimum required spend to complete an offer
* reward (int) - reward given for completing an offer
* duration (int) - time for offer to be open, in days
* channels (list of strings)

ii) profile.json - demographic data for each customer
* age (int) - age of the customer
* became_member_on (int) - date when customer created an app account
* gender (str) - gender of the customer (note some entries contain 'O' for other rather than M or F)
* id (str) - customer id
* income (float) - customer's income

iii) transcript.json - records for transactions, offers received, offers viewed, and offers completed
* event (str) - record description (ie transaction, offer received, offer viewed, etc.)
* person (str) - customer id
* time (int) - time in hours. The data begins at time t=0
* value - (dict of strings) - either an offer id or transaction amount depending on the record

2) StarbucksCapstone.ipynb - Jupyter notebook file containg the full code and expaination about the full process followed in this project.

3) StarbucksCapstone.html - The Jupyter notebook file in HTML format for easy viewing.

## Instructions to implement the project<a name="instructions"></a>
1) Install the libraries required.
2) Download theJ upyter notebook file.
3) Download the data zip file in this repo and extract it.
4) Put the data folder in the folder where your Jupyter notebook file is.
5) Open the Jupyter notebook file and run the code. 

## Results<a name="results"></a>
I was able to make a model and predict the amount a new customer will spend on Starbucks app. I got the following results:
1) Baseline Random Forest model performance:-
* Train RMSE error: 43.40822633356865 
* Test RMSE error: 100.12625339540412

2) Tuned XGBoost model performance:- 
* Train RMSE error: 86.93099660022715
* Test RMSE error: 84.0456223669343

3) To showcase my project I have written a blogpost on Medium, the link for which can be found below:

## Licensing, Authors, Acknowledgements<a name="licensing"></a>
I must give credit to Udacity and Starbucks for the data. I am the author of this project. 

_References:
* https://xgboost.readthedocs.io/en/latest/
* https://matplotlib.org/
* https://stackoverflow.com/
* https://www.geeksforgeeks.org/
* https://scikit-learn.org/stable/index.html

