# ACM Research Coding Challenge (Fall 2020)

## No Collaboration Policy

**You may not collaborate with anyone on this challenge.** You _are_ allowed to use Internet documentation. If you _do_ use existing code (either from Github, Stack Overflow, or other sources), **please cite your sources in the README**.

## Submission Procedure

Please follow the below instructions on how to submit your answers.

1. Create a **public** fork of this repo and name it `ACM-Research-Coding-Challenge`. To fork this repo, click the button on the top right and click the "Fork" button.
2. Clone the fork of the repo to your computer using . `git clone [the URL of your clone]`. You may need to install Git for this (Google it).
3. Complete the Challenge based on the instructions below.
4. Email the link of your repo to research@acmutd.co with the same email you used to submit your application. Be sure to include your name in the email.

## Question One

![Image of Cluster Plot](ClusterPlot.png)
<br/>
Given the following dataset in `ClusterPlot.csv`, determine the number of clusters by using any clustering algorithm. **You're allowed to use any Python library you want to implement this**, just document which ones you used in this README file. Try to complete this as soon as possible.

Regardless if you can or cannot answer the question, provide a short explanation of how you got your solution or how you think it can be solved in your README.md file.

## Research

I did not know much about Python and Github before this challenge, so naturally I created a Github account and research on how to use it. I downloaded Git and was able to clone the fork of the repo into my computer, and from there I used Colaboratory because it is the only Python editor I used prior to this challenge through ExploreML. 

For the clustering algorithms, I researched through Google and found this link about 10 commonly used clustering algorithms. I looked into BIRCH and was going to use the algorithm, but one of the parameters asked for an estimate of number of clusters, which defeat the purpose of this challenge. So I researched DBSCAN and think it was good to use because it finds the number of clusters based on the parameters of minimum distance between points and the minimum number of points to make a cluster.

Sources used: https://machinelearningmastery.com/clustering-algorithms-with-python/
              https://scikit-learn.org/stable/auto_examples/cluster/plot_dbscan.html#sphx-glr-auto-examples-cluster-plot-dbscan-py

## Solution

The libraries I used was sklearn.cluster, matplotlib, numpy and pandas.

First I read the .csv file into the dataframe. I then create the DBSCAN model and fit the data into it. By extracttring the number of unqiue labels from the model, I can determine the number of clusters in the data, which is 2. I added the 'cluster labels' column into the data frame to plot the new graph.
