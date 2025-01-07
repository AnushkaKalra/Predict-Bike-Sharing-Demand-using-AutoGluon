# Report: Predict Bike Sharing Demand with AutoGluon Solution
#### ANUSHKA KALRA

## Initial Training
### What did you realize when you tried to submit your predictions? What changes were needed to the output of the predictor to submit your results?
When I first tried to submit my predictions, I didn't achieve a highly optimized score which demonstrated that I needed to work better on categorization and EDA. Further emphasis on these and incorporation of new features helped me get a better optimization score.

### What was the top ranked model that performed?
The "hpo_model" has the highest score (0.51219) based on the data. This model used hyperparameter optimization (HPO) with settings for gradient boosting machines (GBM) and neural networks (NN), yielding the lowest score of the three models listed, indicating better performance.

## Exploratory data analysis and feature creation
### What did the exploratory analysis find and how did you add additional features?
The impact of weather conditions on bike utilization and the most popular times to hire bikes were perhaps two of the main areas where EDA focused.
After analyzing the data, I added some extra features to make the predictions better:
I broke down the timestamps into smaller parts like the hour of the day, the day of the week, and the month. This helped my model understand the repeating patterns in bike rentals. Further focus onto weather and season assisted even more.
Adding flags to show if it's a holiday or a working day, helped the model consider how rental patterns changed onspecial days.

### How much better did your model perform after adding additional features and why do you think that is?
The Kaggle score decreased from 1.80478 for the original model to 0.63013 for the model with extra features, indicating a considerable improvement in the model's performance.This improvement was probably made possible by the new features, which gave the model access to more pertinent data and improved forecast accuracy.

## Hyper parameter tuning
### How much better did your model preform after trying different hyper parameters?
As I adjusted the model, I saw a noticeable improvement in its performance. At the beginning, the model's score was 1.80478. The score increased to 0.63013 after additional elements were added and adjustments were made. The most significant improvement happened when I optimized the hyperparameters (hpo_model), which resulted in a score of 0.51219. This shows a big difference in the model's performance, with the final score being about 71.6% lower than the initial score.

### If you were given more time with this dataset, where do you think you would spend more time?
I would experiment more with the dataset to generate new features and further optimize the model's parameters if I had more time. This includes trying various feature combinations and fine-tuning additional parameters. Also, I might try using more complicated models or combining different models together to see if they make a big difference compared to the best model we have now.

### Create a table with the models you ran, the hyperparameters modified, and the kaggle score.
|model|hpo1|hpo2|hpo3|score|
|--|--|--|--|--|
|initial|value|value|value|1.80478|
|add_features|value|value|value|0.63013|
|hpo|GBM: num_leaves: lower=25, upper=64|NN: dropout_prob: 0.0, 0.5|GBM: num_boost_round: 100|0.51219|

### Create a line plot showing the top model score for the three (or more) training runs during the project.


![model_train_score.png](img/model_train_score.png)

### Create a line plot showing the top kaggle score for the three (or more) prediction submissions during the project.


![model_test_score.png](img/model_test_score.png)

## Summary
The 'hpo' model was the best model with a Kaggle score of `0.51219`.