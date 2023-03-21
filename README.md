# _**Sentiment Analysis on Tweets**_


## **Project Description**

## **Observations**


## **Model Comparison**

* RMSE

\begin{array}{|c|c|} \hline
Target & CountVectorizer() & TfidfVectorizer() & Word Embeddings & Advanced DL \\ \hline
negative & 0.102 & 0.09 & 0.116 & 0.114 \\ \hline
neutral & 0.22 & 0.224 & 0.265 & 0.224 \\\hline
positive & 0.136 & 0.116 & 0.238 & 0.203 \\ \hline
compound & 0.278 & 0.228 & 0.456 & 0.43 \\ \hline
\end{array}

* MAE

\begin{array}{|c|c|} \hline
Target & CountVectorizer() & TfidfVectorizer() & Word Embeddings & Advanced DL \\ \hline
negative & 0.053 & 0.05 & 0.075 & 0.069 \\ \hline
neutral & 0.138 & 0.163 & 0.201 & 0.192 \\\hline
positive & 0.073 & 0.079 & 0.149 & 0.146 \\ \hline
compound & 0.191 & 0.202 & 0.346 & 0.33 \\ \hline
\end{array}

## **About the Models**
