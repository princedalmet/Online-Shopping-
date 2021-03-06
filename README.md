
## Introduction

The growing popularity of online shopping has led to the emergence of new economic activities. To be successful in a highly competitive eCommerce environment, it is essential to understand customers’ online purchase intent.

In recent years, e-commerce has brought huge benefits to suppliers and consumers. Defined as the use of the Internet to sell products or services to individual consumers, e-commerce has profoundly changed the way people conduct their business.

Indeed, it has become an important full-fledged transaction channel. A recent survey of online shopping predicted that the total amount of direct sales to customers will exceed $ 240 billion by 2007. Major technological innovations in online shopping have changed transaction channels in the information age.

With the growth of online shopping, it has become important to understand the factors that influence a consumer’s intention to buy from a website rather than just browse. This emerging topic is of interest to both academics and machine learning practitioners.


## Data Preprocessing

importing the necessary libraries and the data

![1](https://user-images.githubusercontent.com/99526815/160539233-7899b218-1d86-4dfb-9353-e08ad4c26739.PNG)

![2](https://user-images.githubusercontent.com/99526815/160539303-e8b06647-d25d-4660-b1a1-3d070cb3ae45.PNG)

Now let’s apply the K-elbow method to determine the number of clustering groups:

![3](https://user-images.githubusercontent.com/99526815/160539330-839ee736-fdbf-4756-9e7b-b4ef8c8d85a5.PNG)

K Means Clustering

![4](https://user-images.githubusercontent.com/99526815/160539345-91b19b52-fefc-4791-a1a3-8e09765d8b19.PNG)

According to the graph above, the maximum curvature is at the second index, that is, the number of optimal clustering groups for the duration of the product and the bounce rates is 2. Once the number of clusterings determined, we apply the K Means method and plot the clusters:

Looking at this K Means grouping plot, we can say with certainty that customers who spent more time on a product-related website are very less likely to leave the website after viewing a single page.

Since K-Means is not a supervised learning method, we are adopting other ways of evaluating its clustering result. The leftmost column of the confusion matrix represents the actual label (True or False revenue), and the top row represents the expected clustering groups (uninterested customers or target customers):

![5](https://user-images.githubusercontent.com/99526815/160539424-078ba086-bd21-492f-ac53-c9ff01964edf.PNG)

![6](https://user-images.githubusercontent.com/99526815/160539438-e26b0f9a-9537-45ae-bd56-fed0c5d4b68d.PNG)

## Observations From Above Plots

From the confusion matrix, we can see that out of 10,422 failed incomes, 9,769 are grouped into uninterested customers or 94%. However, out of 937 successful incomes, only 284 are grouped as target customers or 15%. Also, the adjusted index score is not very high.

So it is clear that we have poorly bundled many successful revenue sessions as uninterested customers, which means when the high bounce rate combined with a short product-related page duration, there are still a lot of customers targets.
