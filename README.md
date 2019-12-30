# Project_2_Group_2

# Project-2

When it comes to price forecasting for stocks usually we think of historic prices and fundamental data as our main sources of information to build a model to predict prices. We offer a more exacting approach. We want to pay spacil attention to the supply chain of companies. The idea is that by focusing on the supply chain we can predict stock price movements. A company 


We believe that the sistematic study of the movememt in prices of businesses that comprise the supply chain of a certain company can lead to predicting the stock's price of this very company. Since a supply chain is "a network between a company and its suppliers to produce and distribute a specific product to the final buyer. This network includes different activities, people, entities, information, and resources. The supply chain also represents the steps it takes to get the product or service from its original state to the customer". We believe that we can see a lot of what is happening at "certain point on a river by seeing what is happening upstream and downstream". If the biggest clients of a certain company are not performing so well, it could be expected, at least in the short term that their biggest supplier will suffer undesarible consecuences. Or what effect could have on a bussness the fact that their biggest suppliers are having trouble, because lets say, the procure of certain commodity is becoming more expensive due to climate or political unrest in a certain country, and this commodity is essential for the manufacture of an element that is needed for a product. lets say, Silicon to manufacteure semiconductors that are needed to build a laptop. We could then consider this as a fundamental analysis with an approach towards the supply chain, were we understand clearly how the pieces are connected, we propose building machine learning models were the features are the pieces that constitute the supply chain of a company that we take as the target. We are offering an alternative for prices forecasting that can give an edge for equities pricing using Machine Lerarning.

To test our Deep Learning model we used the company Intel as our target. the features were, for supply chain as follows:

Suppliers: Applied Materials, Taiwan Semiconductor Manufacturing.
Distributors: Arrow Corporation, Avnet, inc, Synnex Corporation.
Clients: Dell, HP, Lenovo

We also wanted to test the model against an analysis were the features are stock's closing prices for companies that are direct competitors to Intel: Advanced micro Divices, NVIDIA, Qualcomn, Broadcom, Micron Technologies and Texas Instruments. We set off our model to predict the closing price of Intel using historic prices from these competitors and compared the results with the supply chain analysis. We calculated the correlation betwen predicted prices and real prices for both analises and compared them. Also, in parallel to the Neural Network we ran a Machine learning regression algorithm to also have a comparison beteewn model's outcomes for reference during our testing.

For the Neural Network we optimized our hyperparameters by trial an error, until we found a set up that would minimize error without over or underfitting the model without taking to much computational time.

The followin image shows the deep learning model set up used.

![table](https://github.com/salomonysmayel/Project_2_Group_2/images/blob/master/model.png "model")

We use K-fold validation to ensure that the test sample that we are using is not too contrasting from our test sample in terms of variance.

To measure the performace of our model we plotted the mean absolut error vs the number of epochs, to check how the average of the absolute differences between target values and the predictions evolve with the epochs. As shown bellow

IMAGE 2

We also compared the loss with the number of epochs, for train and validation, so that we know deppending on how both curves are interacting, if we are underfitting, overfitting or setting up our model just right.

IMAGE 3 

The results for our model showed that the prediction of stock prices ussing the supply chain approach pproved to be more acurate when compared to the forecasting of prices using the closing prices of Intel's competition. And also, as expected, the regression using deep learning proved to be more accurate that the simple machine learning skitlearn regression model.

IMAGES 4 AND 5 

Given our positive results, we feel confident saying that our model  using supply chain as an analitics source of information for deep learning models to forecast equities prices is a very promissing approach to investment analysis. With higher quality data we believe that we can construct and offer a very proffitable model for investors.
