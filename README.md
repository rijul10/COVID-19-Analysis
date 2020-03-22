# COVID-19-Analysis
FLIPR Hack4.0
Solution Sheet

I have used the linear regression model on the dataset. I have carefully applied and analysed multiple models with the metric being Root Mean Square Error. The analysis is provided in the table below: -

Sr. No.	MODEL USED	RMSE
1	Linear Regressor	9.07
2	Artificial Neural Network	9.27
3	ElasticNet	9.32
4	DecisionTree Regressor	10.3
5	KNeighbors Regressor	10.3
6	Gradient Boosting Regressor	10.42

The artificial neural network contained 3 hidden layers with 256 neurons each. It had more than 1,00,000 trainable parameters and its metric was set to be validation loss.
Still, the linear regressor performed the best among all the models.

Linear Regression Model

Linear regression is a linear model, e.g. a model that assumes a linear relationship between the input variables (x) and the single output variable (y).
y=b0+b1*x1+b2*x2+⋯+bn*xn 
More specifically, y can be calculated from a linear combination of the input variables (x). When there is a single input variable (x), the method is referred to as simple linear regression. When there are multiple input variables, literature from statistics often refers to the method as multiple linear regression. I have used multiple linear regression as the number of inputs of my dataset were more than one. 	 

It is found in the python library scikit-learn and can be imported as follows:

from sklearn import linear_model


I have used the Vector Autoregression model for time series prediction. The Autoregression model is for the univariate datasets only. The data I had was spread on 7 days (20th march, 2020 – 26th march, 2020) and thus had to considered a multivariate dataset. Using this model, I have predicted the diuresis of people on 27th March. Using this, I trained a KNeighbor Regressor model to predict the infected probabilities of the people using the time series diuresis data. This model was then used to predict the infected probabilities of the test data.

Vector Auto Regression Model

Vector autoregression (VAR) is a stochastic process model used to capture the linear interdependencies among multiple time series. VAR models generalize the univariate autoregressive model (AR model) by allowing for more than one evolving variable. All variables in a VAR enter the model in the same way: each variable has an equation explaining its evolution based on its own lagged values, the lagged values of the other model variables, and an error term. VAR modeling does not require as much knowledge about the forces influencing a variable as do structural models with simultaneous equations: The only prior knowledge required is a list of variables which can be hypothesized to affect each other intertemporally.


