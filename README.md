# crypto-pca

This is a project that initially started as a Principal Component Analysis of cryptocurrency prices but evolved into an exploration of machine
learning algorithms that could be used to classify an asset as a cryptocurrency or equity. 

There aren't really any remarkable differences between the principal components of the cryptocurrencies and the principal components
of the equities. If we look at the covariance graph, however, it's evident that cryptocurrencies covary with each other more than
equities covary with each other.

Here are a couple of the strategies I used: 
K-means clustering of mean of the percent daily return of an asset against standard deviation of the percent daily return. This 
algorithm yielded much less interesting results than I was anticipating. Since the Sharpe ratio of equity and cryptocurrencies
ended up being approximately the same, the plot of mean against standard deviation indicated that equities and cryptocurrencies
could be discerned from each other by using the mean or standard deviation on their own.

My favorite classification algorith was the one that involved using the Kullback-Leibler divergence.
I started reading All of Statistics by Larry Wasserman in my free time and I learned about the Kullback-Leibler divergence. 
This is a measure of how similar two probability distribution functions are. Even though visually, the histogram of 
cryptocurrency and equity percent daily returns are nearly undiscernable from eachother, the Kullback-Leibler divergence captures
some features of the crypto and equity pdfs that aren't visually evident. Moreover, when we use the histogram of the crypto
and equity percent daily changes, we lose information on time. The fact that the Kullback-Leibler still identifies
cryptocurrency pdfs as being close to each other and indentifies cryptocurrency pdfs as being far from equity pdfs is pretty
neat.
