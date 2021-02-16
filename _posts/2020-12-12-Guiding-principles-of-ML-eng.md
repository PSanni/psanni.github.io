---
layout: post
title: Guiding principles for ML engineering
---

This blog post is intended to introduce the most essential rules of ML engineering. It presents a style of machine learning or prepares you for production-level modelling. Remember, most of the problems you will face in ML pipeline will, in fact, be engineering problem. Even with all knowledge and resource of machine learning, most of the success comes from great approach of modelling you follow. This strictly is not limited to great feature engineering, but it also includes other design principles. 

### 1. Its also cool launching product without Machine Learning

That's right, you don't need a complex machine learning system for a simple solution, a classic heuristic approaches are acceptable. 
For instance, if you are building a recommendation system for your online grocery store, you don't need a neural network-based solution.
Simple, matrix-factorization techniques are acceptable, in-fact in the case of limited data, they still outperform NN's in term of performance. 
Therefore, if machine learning is not absolutely required for your product, don't use it until you have data.
  
### 2. Have baselines

The first or baseline model provides the most significant boost or threshold to your product, so it doesn't need to be fancy. Baseline model should be the simplest solution you can think about the problem. Then you can gradually improve with new possible solutions. However, while building a new model, it should be more infrastructure-focused; otherwise, you might run into many more issues than expected. Even before making the baseline model, you need to determine: 

  1. A fist cust as to what "good" and "bad" mean to your system. 
  2. How to get the example to your learning algorithm. 

The first point is mainly concerned with the use of adequate evaluation metrics. For example, while ranking documents given a query, Mean Average Precision is more useful than the simple precision-recall graph. This does also includes choosing classification thresholds and etc. Last but not least, have multiple baselines consist of different modelling approach is also benificial. 

The above two principles are mainly concerened before machine learning scenario. Further on outlined principles are concerned with design strategies. 

### 3. Your First Pipeline

When presented with ML problem, it is fun to think about all the imaginative machine learning you are goind to do. It is also natural to come up with fancy ideas but remember, it will be hard to figure out what is happening if you don't first define and trust your pipeling. The well defined ML flow ensures the less difficul learning when modelling grows. Keep the first model simple (principle 2) and have infrastructure right, should be the third most step before kicking in with real modelling. 
