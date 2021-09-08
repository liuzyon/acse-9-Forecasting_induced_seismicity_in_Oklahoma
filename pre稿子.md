# Start

Hi, I am Zhiyong LiU

The title of my individual project is to forecast induced seismicity in Oklahoma. The project was implemented under the guidance of Doctor Stephen P Hicks. So here I am very grateful to his help.

First, I will introduce my project briefly.

It is well known that human can cause earthquakes through industries. In this project, we used several datasets from industries as candidate factors to forecast earthquakes occurred. We also analyse feature importance of them. The data contains injection activities,  hydraulic fracturing activities, wells information and geological information such as depth to basement.



### METHODOLOGY

Now I will describe the techniques and tools used in this project.

 In coding, I used two main libraries to achieve the goal. The first is Pytorch, it is an optimized library for deep learning and tensor computation. I used it because it is convenient to construct neural network model with the feature of automatic derivation ([ˌderɪˈveɪʃn]). The second library used is Captum. I used it for interpreting the importance of factors to earthquke occurrence. It supports many interpretability algorithoms and presents them by vision, text and more.

Feedforward Neural Network is the shallowest form of neural netwok model. A single neuron in network represents a linear or logistic regression. There are some complex mathematical functions that linear or logistic regression cannot represent accurately... Such as complex nonlinear relationships. Neural Network is pretty suitable to deal with them. Each layer neurons multiply its corresponding weights, then they are added each other and the sum is input into an activate function, this is the mapping from current layer to one neuron in next layer, which give the ability to construct nonlinear complex relationships.



To select statistically significant feature from candidate factors, we used the stepwise logistic regression with VIF checking.Briefly, all features were initially excluded, Then, a feature is added in each iteration whilst keeping current features both satisfy p-value <0.05. Meanwhile, in each iteration, we also remains the VIF of current features < 5, even some new added feature required to be eliminated.This process continued until all features kept are statistically signiﬁcant.



In the model evaluation part, we used many measures in machine-learning to evaluate the models.The first is confusion matrix. It have four types which represent true negative prediction, false negative prediction, false positive prediction and true positive prediction. According to values of these four types. We calculated accuracy, precision, recall and F1-score to measure the performance of models. Precision refers to

Precision refers to how many the positive predictions predicted by the binary classifier are accurate. Recall refers to how many real positive samples are found out by the binary classifier.

Then, we also plotted the ROC curve to evaluate models independent of class distribution. 



### IMPLEMENTATION

Now I will state how I implemented this project.

Firstly I select the interest time and interest area for study. The time is 2011 to 2018 and the area is as the figure shows. I grid the interest area in 40 multiply 40 shape and each gridding region approximates to be square with 7 km in length.

By the gridding, I got 1600 samples and each of them represents one of the gridding regions in interest area. The target variable is based on seismicity, which represents the earthquake occurrence in spatial distribution. I assigned each gridding region a value of one if there is at least one earthquake occurred. Otherwise, if no earthquake occurred in this gridding region, we assigned it a value of zero.

In the end, we have 680 seismic regions and 920 nonseismic regions in generated datasets.



For each gridding regions, we collect the industry data and geological information shown in this table. You can see we get 18 candidate features. It involved injections, wells, depth to basement and **hydraulic** **fracturing activities.**



For the feature selection, we used forward stepwise regression which starts with one random feature and each iteration add one feature.
The threshold of P-value we set to 0.05 because it is a common use in statistically. The threshold of VIF is set to 5 because VIF between 1 and 5 indicates some correlation but not enough to be overly concerned about.



As for Models construction, we used two types of models: Neural Network model and logistic regression model.



we use a neural network model which has its input layer with 7 neurons, two hidden layers of 8 neurons per layer and an output layer with 2 neurons as shown in Figure. In general, 1-5 hidden layers will serve for most problems and using the same number of neurons for all hidden layers will suﬃce. Therefore, in this project, we choose to use two hidden layers and each layer has 8 neurons. 

The input features used are also based on the feature selecting result. We had seven input features for our training model by feature selecting result. It’s taken for granted that we set the number of neurons to 7, which represents each input feature. Because earthquake prediction problem is a binary classiﬁcation, so the loss function is set to be cross entropy and we use two neurons in output layer which one output neuron per class. The output represents the probability of the classes (earthquake or no earthquake). The learning rate and the batch size is optimized choice based on the attempts. The optimizer we set Adam because it is commonly used and have fast convergence rate.



For the logistic regression model, there are few options that can be configured, and we used the methods in sklearn to build.



As for Models construction, we used two types of models: Neural Network model and logistic regression model.
we use a neural network model which has its input layer with 7 neurons, two hidden layers of 8 neurons per layer and an output layer with 2 neurons as shown in Figure. In general, 1-5 hidden layers will serve for most problems and using the same number of neurons for all hidden layers will suﬃce. Therefore, in this project, we choose to use two hidden layers and each layer has 8 neurons. 

The input features used are also based on the feature selecting result. We had seven input features for our training model by feature selecting result. It’s taken for granted that we set the number of neurons to 7, which represents each input feature. Because earthquake prediction problem is a binary classiﬁcation, so the loss function is set to be cross entropy and we use two neurons in output layer which one output neuron per class. The output represents the probability of the classes (earthquake or no earthquake). The learning rate and the batch size is optimized choice based on the attempts. The optimizer we set Adam because it is commonly used and have fast convergence rate.

For the logistic regression model, there are few options that can be configured, and we used the methods in sklearn to build.



### Results

In the final part, I will demonstrate the implementation results of project.

The visualization of all data in interest area and interest time are shown here. we found a rough spatial correlation between some of them. We ﬁrstly compared the depth to basement with earthquake activities, we found the lower left regions of interest area has a thicker sedimentary rocks than upper right regions. It is can be inferred that the induced seismicity may be related to depth to basement. Besides, the injection activities are similar to earthquakes activities in spatial distribution.The three black rectangular regions (marked by 1 to 3) represents the activities dense area, which are highly similar in spatial distribution, even in small area as rectangular area 3.

This is the last iteration in feature selection process. You can see that I selected out 7 statistically significant features and all selected features have the VIF less than 5. It involved water volume of hydraulic fracturing activities, number of hydraulic fracturing activities, depth to basement, the depth of wells, number of injections under basement, the depth of injections and volume of injections.This means we successfully eliminated features which are not statistically significant and there is also no high multicollinearity in selected features.

By the selected features, I used them to fit the logistic model and trained the neural network model. Then I used the measures introduced before to evaluate these two models. The results are show in table. 

We can see for all regions in interest area, the prediction accuracy intuitively indicates that NN model performs better than LR model. Besides, the similar precision values indicates that two models have similar ability to predict accurately for all seismic predictions. However, these two models have a large difference in recall value. This means that for all real seismic regions, the NN model has the probability of 80.7% to predict accurately. But LR model only have a probability of 53% to predict accurately, which is a terrible performance for binary classiﬁcation problem. Because precision and recall are contradictory and we want them both high, I used the F1-score which is the harmonic mean of precision and recall. The F1-score indicates NN model has a better comprehensive performance than LR model.

ROC and AUC can evaluate models without the affects of imbalance in datasets. The closer to left top **corner****, the performance better, which also corresponds to a larger AUC value. By the figure, we conclude that NN model also performs better than LR model** considering the effect of imbalance in class distribution.



The mapping results of predictions by two models are shown in Figure. Generally, three dense regions distribution mentioned are correctly predicted, even though the precision of regional outline is poor. Both logistic regression and neural network model can predict the spatial distribution of major earthquake regional clusters. However, in terms of true positive rate, these two models performs greatly diﬀerently by predicted maps comparison with true map. We want true positive rate to be closer to 1 (equivalently false negative closer to 0), which means we want to predict out more seismic samples among true seismic samples. After all, in practice, we tend to regard a region at the risk of seismicity as seismic rather than nonseismic, in order to prevent the property damage and casualties. Through the true seismic map in Figure, all gridding regions in the two blocks marked as 1 and 2 are almost seismic. neural network model indeed selected out almost all true seismic regions in these two blocks, but logistic regression model performs not well and it wrongly predicts many seismic regions to be nonseismic. This is not an ideal predictor in actual use.

Through the feature importance analysis in LR model and NN model, we found the depth to basement is the key predictor of the spatial distribution of seismicity. It is consistent with both models that seismicity is largely promoted with the reduce in depth to basement. The amount of hydraulic fracturing and the depth of wells are also found important, but they have opposite correlation with seismicity among these two models, which require to be further investigated. Furthermore, water volume in base of HF is additionally considered to be important and negatively correlated with earthquake occurrence through NN model.

Thank you for attending my project presentation.