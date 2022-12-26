The apriori algorithm has been implemented based on the algorithm provided in the textbook Data Mining by Tan et al.(Second Edition). for candidate generation and pruning, frequent itemset generation and rule generation. It is present in the notebook in the github repository.

The algorithm followed is

![image](https://user-images.githubusercontent.com/34400175/209585620-bfd8b9cc-a2b3-406b-8c85-327e50980e66.png)

![image](https://user-images.githubusercontent.com/34400175/209585624-33291164-7b5b-48ac-b900-05b77d8c0ba6.png)

![image](https://user-images.githubusercontent.com/34400175/209585626-9d12a101-7bf4-42dd-b600-7bd88e5a0fbb.png)

Both the f(k-1)*f1 and f(k-1)*f(k-1) approaches have been implemented and it is observed that the f(k-1)*f(k-1) method has provided a lot of savings on the number of candidate sets generated as compared to f(k-1)*f1 which is better compared to the brute force method.

To illustrate this we used the example in the textbook and the kaggle dataset provided.

For the textbook example:

![image](https://user-images.githubusercontent.com/34400175/209585631-d6aa6e46-7e1b-4e4a-9e00-965057f38974.png)

For min_sup = 0.6 and min_conf = 0.9

![image](https://user-images.githubusercontent.com/34400175/209585636-1177a05c-8872-41d1-920b-a9bfadd5e8f5.png)

f(k-1)*f(k-1) produced 3 candidate sets less than f(k-1)*f1

For min_sup = 0.4 and min_conf = 0.9

![image](https://user-images.githubusercontent.com/34400175/209585672-ea9bce25-25e5-4265-8ed8-c13afd5b0bb3.png)

f(k-1)*f(k-1) produced 10 candidate sets less than f(k-1)*f1

For min_sup = 0.2 and min_conf = 0.8

![image](https://user-images.githubusercontent.com/34400175/209585677-96c8b522-f1d2-4b3c-8f05-b15e859b65c6.png)

f(k-1)*f(k-1) produced 18 candidate sets less than f(k-1)*f1

So we can say that there are a lot of savings when we use f(k-1)*f(k-1) method even if it is a small dataset. 
