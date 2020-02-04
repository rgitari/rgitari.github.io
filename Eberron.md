## "What brings you to our remote sanctuary?"
## Natural language Processing Project on Dungeons & Dragons Eberron Rising From The last War 

**Project description:** Using publicly available data on Airbnb listings, I have developed several models which predict the price for a listing given the characteristics of the property. These models could be used by various stakeholders, if Airbnb were to make these models or refinements of these models available to the appropriate stakeholders.

*Business use cases:* Firstly, current hosts can use this analysis to evaluate if their listings are mispriced and adjust their prices to charge optimally based on these factors. Secondly, Airbnb may also be able to introduce a tool that advertises to potential hosts and gives them a rapid and efficient method to approximate how much a host’s property could go for. Lastly property investors, and in particular speculators, will be able to use this analysis and develop it further to build models which predict prices and potentially develop around certain areas.

### 1. Model assumptions and variable selecttion 

Graphed a correlation matrix and I plan to remove the independent variables that have a correlation of more than 0.65 with another independent variable in order to prevent multicollinearity, which is an assumption which underlies one of the predictive models we are building (linear regression). 

<img src="images/Corr3.png?raw=true"/>

*** Regularization techniques 
```javascript
Linear regression model built using stepwise regression (both forward and backward).
As a method to prevent overfitting
```

### 2. Geographical representation of Airbnb listings across major US cities

<img src="images/Comb.png?raw=true"/>

```The geographical diversity of Airbnb listings. 
```

### 3. Model Evaluation 

```Final Model Selected is the XGBoost model.

```

It has the lowest RMSE (42%) and MAE (32%)  and also the highest R squared (62% among all the models. 
Which indicates that it has the best cross validated performance.

<img src="images/comparison.png?raw=true"/>

### 4. Final Model Performance  

<img src="images/finalmodel.png?raw=true"/>

The final model performance on unseen data (the test data) has a RMSE of 41%, a MAE of 32% and a R squared of 61.7%. These results are very encouraging as our model has kept very consistent results through both the evaluation stage and testing stage meaning it can be used for predictive analysis. 

### Future Scope
There are several limitations to the models I have developed. The future of this project could be increased in complexity and scope. One way I plan to do this is through some major variables our models fail to take into consideration such as amenities, description, customer reviews, all of which are characters. These are all factors we believe to be very important in determining the optimal price of a new listing, but to properly include them into our models would require advanced text analytics or natural language processing to convert them into usable data. Future research can focus on this to improve the predictive power of the models. 


