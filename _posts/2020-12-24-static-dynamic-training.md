---
layout: post
title: Static vs. Dynamic training
---
There are two main ways of training ML models called static and dynamic. Static modelling is offline, where a model trained once on data offline to be used for an extended period. In contrast, dynamic models are trained online, which mean new data is continuously coming into the model and is incorporated with smaller updates. These both have pros and cons. 

Static models are easy to build plus test with fast training using batching, which is nice and cheap. Another advantage of offline training is iterating until the model is good, where we can do cross-validation based on each unique sample fed into the model. However, it still also requires monitoring input at the inference level, because if the distribution of data changes model makes heuristic predictions. For example, in a finance model trained with years old records less likely to work optimally with new records, this, therefore, let such model stale. 

Contrast to this, dynamic models are continuously fed with training data overtime and regularly synced with updated versions. Therefore this sometimes is a much more complicated process, because it follows progressive validation rather than batch training and testing, which requires data quarantine capabilities and model rollbacks. Dynamic modelling adopts fast to change in nature or distribution of data, which ultimately helps avoid staleness issues.  


In a nutshell, If your data set truly isn't changing over time, choose static training because it is cheaper to create and maintain than dynamic training. However, many information sources really do change over time, even those with features that you think are as constant as, say, sea level. The moral: even with static training, you must still monitor your input data for change.

For example, consider a model trained to predict the probability that users will buy flowers. Because of time pressure, the model is trained only once using a dataset of flower buying behaviour during July and August. The model is then shipped off to serve predictions in production but is never updated. The model works fine for several months but then makes terrible predictions around valentines day because user behaviour during that holiday period changes dramatically.
