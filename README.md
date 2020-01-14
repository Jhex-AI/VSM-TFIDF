## Vector Space Model using Term Frequency-Inverse Document Frequency

A simple implementation of a vector space model where documents (text) is converted into vectors. Term frequency-inverse document frequency [TF-IDF] is used for the vectorization.

## Writeup

The set of documents that we have,

```python
docA = "When Antony saw that Julius Caesar lay dead"
docB = "The world saw the demise of Julius Caesar" 
docC = "Antony saw Julius Caesar lay dead"
docD = "It was him my cat"
```

Final Cosine Similarity Plot comparing A with B,C,D.

![](https://github.com/Ittery/Vector-Space-Model-TF_IDF/blob/master/Plot.jpg)

We can infer that Document C is the most similar with A, Document B is less similar to A compared to C and finally Document D is not at all similar with A.

**Note: Cosine Similarity is not a very accurate measure to find similarity among documents**

The reason being, for a  query suppose ```"the cat ate the mouse"``` and a document containing ```"the mouse ate the cat food"```. Looking at the words, we can say these documents are similar as this particular document contains all the words in the query but they are semantically dissimilar in meaning. When a user searches for a particular query, we can't simply return documents/results using word/text match. This is the drawback of cosine similarity for search based systems. 

Refer: [Semantic Similarity Ranking](https://github.com/Ittery/Semantic-Similarity-Ranking) to see a simple implementation for fixing this issue.
