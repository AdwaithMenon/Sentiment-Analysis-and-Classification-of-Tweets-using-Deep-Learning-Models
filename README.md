# _**Sentiment Analysis on Tweets**_


## **Project Description**

## **Observations**


## **Model Comparison**

### **RMSE**

<img width="592" alt="image" src="https://user-images.githubusercontent.com/70052374/226693662-2432fdce-a446-4cb1-a867-25a9ce686074.png">


### **MAE**

<img width="596" alt="image" src="https://user-images.githubusercontent.com/70052374/226693756-457c1e10-8b92-4729-b601-40fb04bfbcea.png">


* Upon examining the RMSE and MAE values for the test data, it is evident that both CountVectorizer() and TfidfVectorizer() produce similar results.

* Out of the four models considered, **CountVectorizer()** and **TfidfVectorizer()** are the most effective, as they exhibit lower RMSE and MAE values along with high R-squared values.

* Moreover, these models demonstrate higher accuracy in predicting the **Negative** and **Positive** scores, compared to the Neutral and Compound scores.




## **About the Models**

* Regarding the model architecture, we have observed some enhancements after making changes. Specifically, increasing the number of layers has led to improved performance, although not to a significant extent

* Adding dropouts after the neural network layers resulted in a slight increase in the R-squared value, although not as much as anticipated. Even though overfitting remained a concern, these adjustments were still beneficial. Additionally, improvements were observed after decreasing the patience value, reducing the batch size, and limiting the batch size.

* Due to the small size of the dataset, the addition of SimpleRNN layers to the model architecture resulted in a slight improvement.

* The primary challenge we face is the limited size of our dataset, which only contains 4,000 tweets. However, the model's performance improved slightly when the data size is increased from 2,000 to 4,000 tweets. Therefore, increasing the dataset significantly could lead to improved model performance in accurately capturing sentiments.

* It can be concluded that Deep Learning Models are capable of replicating the logic of the nltk SentimentIntensityAnalyzer() for positive and negative scores.
