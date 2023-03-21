# _**Sentiment Analysis and Classification of Tweets using Deep Learning Models**_


## **Project Description**




### **Brief Summary about the Individuals**

* Joe Biden and Elon Musk are influential figures who have amassed millions of followers across various demographics. Their followers hold their statements and opinions in high regard, often viewing them as valuable advice for self-improvement. 

* In this context, the social media content they produce reaches not only millions of people in the US, but also individuals around the world.This is of particular interest to us, as people tend to be influenced by the opinions of these two individuals when making financial decisions.

## **Observations**

* Joe Biden has posted approximately **7.5K tweets**. After analyzing his tweets, it was discovered that he has a total of 2,874,090 retweets, averaging about 57,481 retweets per tweet. A word cloud generated from his tweets shows that most of them contain **positive language**, with a strong emphasis on his concern for the country, as evidenced by frequent mentions of **"nation"**,**"US"**, and **"America".**

* Elon Musk has posted around **21,000 tweets**, to date. After analyzing his tweets, it was found that he frequently discusses four key stocks: **Bitcoin**, **Dogecoin**, **Tesla**, and **Twitter**. Musk is certainly unique in his tweeting style, with most of his posts being controversial and containing a **mix of sentiments**. Additionally, he has recently faced issues with Twitter, which have gained public attention.

### **Word Cloud**

<img width="529" alt="image" src="https://user-images.githubusercontent.com/70052374/226695593-3817ee1d-04e9-4660-b1e3-3e419294e7d0.png">


* Based on the Word Cloud, it is evident that **"American"** is the word with the highest frequency of occurrence.

### **Histograms**

* **Histogram for Negative Score**

<img width="318" alt="image" src="https://user-images.githubusercontent.com/70052374/226705148-a9d7f0ad-da11-451b-8092-c54f7c827817.png">

- We can observe that the histogram for Negative Score is right-skewed.


* **Histogram for Neutral Score**

<img width="298" alt="image" src="https://user-images.githubusercontent.com/70052374/226705220-81d70a09-c59e-4b91-8b8a-8ff73ba233e5.png">

- We can observe that the histogram for Neutral Score is left-skewed.


* **Histogram for Positive Score**

<img width="302" alt="image" src="https://user-images.githubusercontent.com/70052374/226705310-d334d1f7-d33c-4d02-a431-72b05a9d0e5a.png">

- We can observe that the histogram for Positive Score is right-skewed.


## **Model Architecture**

### **Model-1A : CountVectorizer with Dense Neural Networks**

<img width="387" alt="image" src="https://user-images.githubusercontent.com/70052374/226707125-a4c084bd-c73f-4ecc-9bf2-9c9ccde0303d.png">


### **Model-1B TF-IDF with Dense layers**


<img width="389" alt="image" src="https://user-images.githubusercontent.com/70052374/226707339-04236e87-9782-4ccb-bd13-d847a6778872.png">


### **Model 2: Flattened Word Embeddings into a Dense Neural Network**

<img width="389" alt="image" src="https://user-images.githubusercontent.com/70052374/226707543-05b37ece-a942-4773-afd5-611e02a35cc7.png">

### **Model 3 : Advanced Deep Learning Model**

<img width="386" alt="image" src="https://user-images.githubusercontent.com/70052374/226708040-4bf77f6a-0d1a-41e7-8357-d836c1369ab6.png">



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
