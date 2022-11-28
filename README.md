# CS301HW3
Gradient Boosting 

We use gradient boosting when we have features such as weight, temp, and time ( variable x ) to learn some prediction function F(x). The first benefit of gradient boosting is it can be used for any continuous variable we are trying to predict. When boosting we learn F(x) as the sum of some N weak learners. 

![image](https://user-images.githubusercontent.com/91106087/204181899-3ff2b971-c014-4dfc-88b7-1e1715655654.png)

F(x) = ∑ Mi=1 fi(x) 

A weak learner is used to train other weak learners to create an accurate model. Each learner will inherit and learn from their predecessor. 

One thing to consider before starting is to define your loss function. Decide some kind of loss function where you have the true label (y) and prediction (y^)  which is the output of our gradient boosting function (the higher the loss function the worst your predictions are and vice versa). One condition that it needs to satisfy is that it must be differentiable. 

We start initially with a very weak learner F1(x) = f1(x) = y--  .
When we pick a weak learner we are aiming to go towards a direction where we have decreasing lost. Get some ri^ = dL(yi, yi^) / dyi^ | yi = F(xi) 

![image](https://user-images.githubusercontent.com/91106087/204181929-fa386b5b-b3e1-4389-96cb-73d1e9396efc.png)


We then need to fit the new learner; each new one is trained on the same features as the last. 

[r1^~x] approx. which is 

![image](https://user-images.githubusercontent.com/91106087/204181959-86a2c368-2ab8-4724-acb4-3876db50f2f2.png)

Next, we figure out how much f2 to add to the prediction (increment or decrement). 

![image](https://user-images.githubusercontent.com/91106087/204181990-a4a7c333-5699-4baf-a5c8-31b4c058fabb.png)

Lastly, the new model

![image](https://user-images.githubusercontent.com/91106087/204182063-42cce959-c0cf-4f0a-97ba-91478b05a16a.png)

And we redo and start with a new ‘ r ‘. 
