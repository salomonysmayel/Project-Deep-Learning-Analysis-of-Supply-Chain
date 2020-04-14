
## Deep Learning Analysis of Supply Chain 

The goal of this project is to explore the idea that the systematic study of the movement in prices of businesses that comprise the supply chain of a certain company can lead to predicting the stock's price of this very company. Since a supply chain is "A network between a company and its suppliers to produce and distribute a specific product to the final buyer. This network includes different activities, people, entities, information, and resources". We believe that we can estimate  what is happening at "certain point on a river by seeing what is happening upstream and downstream". If the biggest clients of a certain company are not performing so well, it could be expected, at least in the short term that their biggest supplier will suffer undesirable consequences. What effect could have on a business the fact that their biggest suppliers are having trouble, because lets say, the procure of certain commodity is becoming more expensive due to climate or political unrest in a certain country, and this commodity is essential for the manufacture of an element that is needed for a final product. As an example, Silicon to manufacture semiconductors that are needed to build a laptop. We could then consider this as a fundamental analysis with an approach towards the supply chain, were we understand clearly how the pieces are connected. We propose building machine learning models were the features are the pieces that constitute the supply chain of a company that we take as the target. We are offering an alternative for prices forecasting that can give an edge for equities pricing using Machine Learning.

To test the Deep Learning model Intel corp was used as the target. the features were as follows:

Suppliers: Applied Materials, Taiwan Semiconductor Manufacturing.
Distributors: Arrow Corporation, Avnet, inc, Synnex Corporation.
Clients: Dell, HP, Lenovo

Also the model was tested against an analysis were the features are stock's closing prices for companies that are direct competitors to Intel: Advanced micro Devices, NVIDIA, Qualcomn, Broadcom, Micron Technologies and Texas Instruments. Set off our model to predict the closing price of Intel using historic prices from these competitors and compared the results with the supply chain analysis by calculating the correlation between predicted prices and real prices for both analyses. Also, in parallel to the Neural Network we ran a Machine learning regression algorithm to also have a comparison between model's outcomes for reference during our testing.

For the Neural Network we optimized our hyper-parameters by trial an error, until we found a set up that would minimize error without over or under-fitting the model without taking to much computational time.

The followin image shows the deep learning model set up used.


![model setup](/images/model.png)


We use K-fold validation to ensure that the test sample that we are using is not too contrasting from our test sample in terms of variance.

To measure the performance of our model we plotted the mean absolute error vs the number of epochs, to check how the average of the absolute differences between target values and the predictions evolve with the epochs. As shown bellow

![MAE_vs_epochs](/images/MAE_vs_epochs.png)

We also compared the loss with the number of epochs, for train and validation, so that we know depending on how both curves are interacting, if we are under-fitting, overfitting or setting up our model just right. While training we want our curves to converge.

![loss_vs_epochs](/images/loss_vs_epochs.png)

The results for our model showed that the prediction of stock prices using the supply chain approach proved to be more accurate when compared to the forecasting of prices using the closing prices of Intel's competition. And also, as expected, the regression using deep learning proved to be more accurate that the simple machine learning skitlearn regression model.

Just by looking at the plot we can see that the blue points corresponding to the deep learning algorithm fit a line better than the same blue dots on the second graph for the competitors analysis, also we can see how more accurate the model is compared to the regression model using sckit Learn, represented on both graphs by the orange dots.


Price forecasting model results with Supply Chain 

![supply_chain](/images/supply_chain.png)


Price forecasting model results with competition companies

![competition](/images/competition.png)

To actually see in numbers the differences between the two models, we calculated the correlations of all the results, as shown below.

![correlation_sc](/images/correlation_sc.png)

The correlation between predicted by deep learning model and real values for the supply chain analysis was 0.9872
The correlation between predicted by linear regression model and real values for the supply chain analysis was 0.8614

![correlation_comp](/images/correlation_comp.png)

The correlation between predicted by deep learning model and real values for the competitors analysis was 0.9602
The correlation between predicted by linear regression model and real values for the competitors analysis was 0.8277

The following is a partial view of the results for predicted values compared to real values for different closing prices on the historical data for Intel's closing price.

![results](/images/results.png)

Given our positive results, we feel confident saying that our model  using supply chain as an analytics source of information for deep learning models to forecast equities prices is a very promising approach to investment analysis. With higher quality data we believe that we can construct and offer a very profitable model for investors.
