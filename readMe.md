# Skills and Non skill

### Task 
Seperate the technical skill from  non-technical skill.

### Key-Points 
1. Since dataset has no label it is clearly unsupervised.
2. Model to use can be 
    - Kmeans.
    - Dbscan
3. Text based clustering.


### Preprocess.

1. Some of the points contains (.) which is not useful removing them.
2. SOme have special character.
3. Lot of dublicates. 
4. Remove charcter such as .


WorkFlow:

1. Lower the words.
2. Check dublicates.
3. Remove punctuation.
4. Check dublicates.

Dublicates should be check multiple times as removing and preprocessing the text might result in 
re dublication.

### Fearturizing the data.

To featurize the text data various features can be used such as 
1. One hot encoding.
2. Tfidf.
3. word2vec

Here i used tfidf to featurize the data as one hot encoding creates much sparcity than tfidf and word2vec has creates the dimension to increased.

### Model
Model use is 
1. Kmeans where cluseter size is set to 2 

( 0 for non technical and 1 for technical).

2. Dimension of tfidf is reduce using pca and trained using Kmeans.


### Conclusion

1. Could use bert to extract the embedding vector for each word and apply cosine similarity or apply
Kmeans in embedded vector which could have given better result.
2. HyperParameter tuniing of k in kmeans could be done but there should be manual check for output to verify its validity.
3. Other featurizing could have been used
    Here i use only TFIDF but inspite of increasing dimension word2vec could be applied and dimension could have been reduced using PCA to train.
4. Feature Engineering could have been much better.


