# Machine Learning Homework - Exoplanet Exploration

![exoplanets.jpg](Images/exoplanets.jpg)

## Background

Over a period of nine years in deep space, the NASA Kepler space telescope has been out on a planet-hunting mission to discover hidden planets outside of our solar system.

To help process this data, you will create machine learning models capable of classifying candidate exoplanets from the raw dataset.

In this homework assignment, you will need to:

1. [Preprocess the raw data](#Preprocessing)
2. [Tune the models](#Tune-Model-Parameters)
3. [Compare two or more models](#Evaluate-Model-Performance)

- - -

### Reporting

After splitting the data in a train -test (75%-25%) data set, preprocessing the data and scaling the features, I've used 4 different categorical Machine learning models using the multiclass parameter for some of them as we had 3 classes (CONFIRMED, FALSE POSITIVE and CANDIDATE ) 

| Model                   | Accuracy |
| ----------------------- | -------- |
| **Logistic regression** | 0.898    |
| **Random Forest**       | 0.91     |
| **KNN**                 | 0.828    |
| **SVC**                 | 0.899    |

We can observe that the accuracy is overall the same with Random Forest perfroming a little bit better and KNN beeing the less accurate.

As we need to find the candidates, let's find out which models have a good precision and a good recall for the CANDIDATE predictions measured by the f1_score :

**Logistic Regression:**

​                				precision    recall     f1-score   support      

CONFIRMED             0.87          0.68         0.76       404

FALSE POSITIVE       0.75          0.89         0.82       435     

CANDIDATE              0.99           1.00         0.99       909       

accuracy                                                        0.90      1748     

macro avg                0.87            0.86         0.86       1748  

weighted avg            0.90           0.90          0.90      1748

​															#############################

**Random Forest:**

​                				precision    recall     f1-score   support      

CONFIRMED      		   0.84      0.77        0.80           404 

FALSE POSITIVE      	 0.81      0.85         0.83           435     

CANDIDATE       		   0.99      1.00         0.99           909       

accuracy                                                       0.91        1748     

macro avg    			     0.88      0.88          0.88        1748  

weighted avg                0.91      0.91           0.91       1748

​															#############################

**KNN:**

​                				precision    recall     f1-score   support      

CONFIRMED              0.69           0.51      0.59          404 

FALSE POSITIVE        0.63           0.77       0.69          435     

CANDIDATE               0.99           1.00       0.99         909       

accuracy                                                      0.83       1748     

macro avg                  0.77          0.76         0.76       1748  

weighted avg              0.83           0.83      0.82       1748

​															#############################

**SVC:**

​                				precision    recall     f1-score   support      

CONFIRMED                0.85        0.74        0.79       404 

FALSE POSITIVE           0.77        0.88       0.82       435     

CANDIDATE                  0.99        0.98       0.99       909       

accuracy                                                      0.90      1748     

macro avg                    0.87       0.87         0.87       1748  

weighted avg                0.90      0.90         0.90      1748



We Observe again not much difference between the models, but the Random Forest performs in better on every lines. Having also the hightest precision to detect False positives.

I can say that the model is relatively accurate making more than 90% correct predictions.

I've used gridsearch to optimalise the parameters but in general the accuracy didn't change much.

## Improvements ##

The models could be improved by having more data. I could also extend the models used to find one with a better accuracy like SGB or KERNEL approximation. 

-------------------------------------------------------------------------------------------

## Resources

* [Exoplanet Data Source](https://www.kaggle.com/nasa/kepler-exoplanet-search-results)

* [Scikit-Learn Tutorial Part 1](https://www.youtube.com/watch?v=4PXAztQtoTg)

* [Scikit-Learn Tutorial Part 2](https://www.youtube.com/watch?v=gK43gtGh49o&t=5858s)

* [Grid Search](https://scikit-learn.org/stable/modules/grid_search.html)

- - -

##### © 2019 Trilogy Education Services, a 2U, Inc. brand. All Rights Reserved.
