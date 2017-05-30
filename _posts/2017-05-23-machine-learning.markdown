---
layout: post
title:  "Machine Learning"
date:   Tue May 23 12:32:54 PDT 2017
categories:
---

This is a HUGE topic. We cannot hope to teach it. Instead, we will introduce you to some of the historical context, terminology, links for further study, as well as a basic, hands-on introduction in python.

Several Terms:

- Artificial Intelligence
- Statistics
- Machine Learning [13][]
- "Data mining"
- Knowledge Discovery in Databases [3][]
- Deep Learning [12][]

![]({{ site.url | append:site.baseurl}}/image/Knowledge Discovery in Databases.png)

[3]: http://www.kdnuggets.com/gpspubs/aimag-kdd-overview-1996-Fayyad.pdf
[12]: http://www.mitpressjournals.org/doi/pdf/10.1162/COLI_a_00239
[13]: https://en.wikipedia.org/wiki/Machine_learning


> Machine Learning at its most basic is the practice of using algorithms to parse data, learn from it, and then make a determination or prediction about something in the world... rather than hand-coding software routines with a specific set of instructions to accomplish a particular task, the machine is “trained” using large amounts of data and algorithms that give it the ability to learn how to perform the task. [1][]

[1]: https://blogs.nvidia.com/blog/2016/07/29/whats-difference-artificial-intelligence-machine-learning-deep-learning-ai

![](https://blogs.nvidia.com/wp-content/uploads/2016/07/Deep_Learning_Icons_R5_PNG.jpg.png)

Machine Learning techniques: Linear Regression, K-means, Decision Trees, Random Forest, PCA, SVM and finally Artificial Neural Networks (ANN), and many more...

![](http://main-alluviate.rhcloud.com/wp-content/uploads/2016/06/Periodic-Table.png)

([link](http://main-alluviate.rhcloud.com/wp-content/uploads/2016/06/Periodic-Table.png))


## ANN -> DL

[Artificial neural network](https://en.wikipedia.org/wiki/Artificial_neural_network)

![](http://nikhilbuduma.com/img/neuron.png)


<https://www.linkedin.com/pulse/computer-vision-research-my-deep-depression-nikos-paragios>

<http://cs.stanford.edu/people/karpathy/convnetjs>

<http://playground.tensorflow.org>


> Deep learning is a form of machine learning that uses a model of computing that's very much inspired by the structure of the brain. Hence we call this model a neural network. The basic foundational unit of a neural network is the neuron, which is actually conceptually quite simple. [2][]

[2]: http://nikhilbuduma.com/2014/12/29/deep-learning-in-a-nutshell


## Machine Learning

<http://scikit-learn.org/stable/index.html>

- Supervised
  + There is a training set which gives information about the target categories and their characteristics
- Unsupervised
  + The characteristics and number of targets is decided from the data or parameters rather than a training set.
  + i.e., the algorithm needs not have training, but evaluates the input set to make sense of its contents labels

### Types

- Baselines (think [Placebo](https://en.wikipedia.org/wiki/Placebo) or [Control Group](https://en.wikipedia.org/wiki/Treatment_and_control_groups).. See [4][]) 
	+ Dummy classifiers for baseline
		* To check whether our classifier is actually better than these for our data
		* These classifiers measure nothing and provide the "baseline" accuracy
	+ Random
		* The output of the classifier is completely random
	+ ZeroR (Majority predictor) [5][]
		* Always predicts the most frequent label in a dataset
		* Predicts the mean (for a numeric class) or the mode (for a nominal class)
		* Zero rules (zero branches in a decision tree)
	+ RandomPrior
		* Use the distribution of the training data to generate random classification
- Nearest Neighbor Classifiers [8][]
  + Find what is the nearest neighbor in multidimensional space
  + No clustering at all, just nearest one matters
  + Can be supervised or unsupervised (i.e. we know how many categories there are or we don't)
  + k-nearest neighbors
    * Count several of the nearest neighbors
  + k-NN voting
    * Majority voting
      - Count number of each label in the k-nearest neighbors
      - The label most represented in the nearest neighbors is picked
    * Distance weighted
      - Adding a weight to each "vote" depending on the distance
      - Further neighbors have less weight on the vote
  + Distance/Proximity/Similarity
    * Euclidean distance
    * [Minkowski distance](https://en.wikipedia.org/wiki/Minkowski_distance)
    * [Mahalanobis distance](https://en.wikipedia.org/wiki/Mahalanobis_distance)
      - Adjust for the dynamic ranges of each feature
  + Performance
    * Quick to train, but slow to perform (all the work happens on `predict`)
    * The decision boundaries depend on k
    * When number of dimensions is large, distance starts becoming meaningless
- Generative probabilistic approaches
  + Essentially design generators that can provide measurements that are similar to the test data set
  + Fitting probabilistic models to data
  + Gaussian Mixture Model [7][]
    * Each label is considered a multidimensional gaussian distribution
    * Estimate the parameters of this distribution
    * There may still be an area of overlap of the two distributions and this will be the source of error for the classifier
  + Naive Bayes classifier [6][]
    * Like GMM but making a separate model for each feature
    * Useful if the features are not highly correlated
- Decision Hyperplanes
  + Linear Classifiers
  + Essentially finding an optimal linear decision boundary
  + Support Vector Machine [9][]
    * SMO
    * Several hyperplanes might be used to separate the training data optimally
    * The "optimal" one with minimum error is chosen
    * Effective on high dimensional spaces
  + Perceptron
    * Multilayer perceptron networks AKA Neural Networks
    * Can be used to iteratively find the optimal hyperplanes
    * Classification is done by a "learned" weighing vector to the feature vector plus a bias.
  + Regression
  + (For many estimators, including the SVMs, the standard deviation for each feature must be normalized to 1 to get good prediction.)
- Desicion Trees
  + A desicion path is followed from the root to a leaf according to input data to determine a final output value
  + Desicion tree learning [10][]
    * Several techniques
    * Most popular: Gini impurity
      - Used in the CART algorithm (Classification and regression tree) [11][]
      - "Gini impurity is a measure of how often a randomly chosen element from the set would be incorrectly labeled if it were randomly labeled according to the distribution of labels in the subset"
  + Simple to understand and interpret
  + Can be tweaked after a tree has been automatically generated
  + Some complex problems can generate very complex trees
- Clustering
  + Clustering is the output of [cluster analysis](https://en.wikipedia.org/wiki/Cluster_analysis)
  + Distance based clustering
    + The number of clusters is a parameter
    + Hierarchical clustering
    + Essentially distance clustering
    + K-means clustering
    + Separate data in clusters according to distance
    + Clusters are represented by a "centroid" which may not match an actual vaue
    + This centroid minimizes the distance to all its member points
  + Distribution based clustering
    + Model clusters as Gaussian distributions
    + Gaussian Mixture Model is a type of this
  + Density based clustering
    + Like distance based clustering
    + But adds additional rules about density to cluster groups
  + Many others
- Representation Learning
  + aka [Non-Linear Dimensionality Reduction](https://en.wikipedia.org/wiki/Nonlinear_dimensionality_reduction)
  + Discover better lower dimensional representations of the data
  + [Principal component Analysis](https://en.wikipedia.org/wiki/Principal_component_analysis)
  + [SOM (Self-Organizing Maps)](https://en.wikipedia.org/wiki/Self-organizing_map)
  + Kohonen Maps [15][]
  + Manifold learning 
- Preprocessing
  + Resampling
  + Normalize
- Metrics
  + Testing
    * Cross-validation
      - Folds
      - k-fold validation
        + The original training set is separated into k equal sized groups
        + Then one of the groups is used as testing data, and the rest of the groups are used separately as training data
        + The test group is classified against each testing subgroup and with itself
        + A value of 10 for k is common
      - <https://en.wikipedia.org/wiki/Cross-validation_%28statistics%29>
    * Use training set
    * Use additional set
    * Percentual split
  + Confusion matrix [16][]
  + Error and presicion
    * Accuracy
      - Percent of correct identifications

## Deep Learning for Audio/Visual work

...The really cool stuff:

- <https://deepdreamgenerator.com/gallery>
  + <https://github.com/google/deepdream/blob/master/dream.ipynb>
- <https://magenta.tensorflow.org/>
  + <https://magenta.tensorflow.org/sketch_rnn>
  + <https://magenta.tensorflow.org/nsynth>
  + <https://magenta.tensorflow.org/nsynth-instrument>
  + <https://magenta.tensorflow.org/2016/12/16/nips-demo>


[4]: https://www.quora.com/What-does-baseline-mean-in-machine-learning
[5]: http://www.saedsayad.com/zeror.htm
[6]: https://en.wikipedia.org/wiki/Naive_Bayes_classifier
[7]: https://en.wikipedia.org/wiki/Mixture_model
[8]: https://en.wikipedia.org/wiki/K-nearest_neighbors_algorithm
[9]: https://en.wikipedia.org/wiki/Support_vector_machine
[10]: https://en.wikipedia.org/wiki/Decision_tree_learning
[11]: http://statweb.stanford.edu/~lpekelis/13_datafest_cart/13_datafest_cart_talk.pdf
[14]: http://scikit-learn.org/stable/modules/manifold.html
[15]: https://www.mat.ucsb.edu/g.legrady/academic/courses/06w259/projs/cs/MAT259-paper.pdf
[16]: http://www.dataschool.io/simple-guide-to-confusion-matrix-terminology/


## Further Research

* <https://medium.com/intuitionmachine>
* <http://www.deeplearningpatterns.com/doku.php/overview>
* <https://en.wikipedia.org/wiki/Design_pattern>
* <https://orange.biolab.si>
* <http://scikit-learn.org/stable>
* <http://www.shogun-toolbox.org>
* <http://www.cs.waikato.ac.nz/ml/weka>
* <https://wiki.python.org/moin/PythonForArtificialIntelligence>
* Machine Learning for [Music Information Retrival](https://en.wikipedia.org/wiki/Music_information_retrieval)
  + <https://www.youtube.com/watch?v=HjOKIegKS5c>
  + <https://www.youtube.com/watch?v=Jmrc1TrFZPE>
  + <https://www.youtube.com/watch?v=dQvP_pD46hE>
* <http://norvig.com>
  + <http://www.norvig.com/ipython/README.html>
* <https://aiexperiments.withgoogle.com>
* datasets:
  + <https://archive.ics.uci.edu/ml/datasets.html>
  + <http://www.audiocontentanalysis.org/data-sets>
* Hidden Markov Models
  + <http://www.blackarbs.com/blog/introduction-hidden-markov-models-python-networkx-sklearn/2/9/2017>
