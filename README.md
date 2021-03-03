# My electrophoresis sense is tingling 🕷️.

## Predictive maintenance
When will an electrophoresis plant require maintenance? Predicting if it will require maintenance using previous values of sensor readings.

## Why this was done
Time series data is a new challenge for me and I wanted to combine this with a library I've been exploring `tsai` (fastai extension focused on time series). 

Why this problem can be summed up in this as "**maintenance costs ⏱️ and 💰**". 

* If you are running a manufacturing plant or in this case a electrophoresis plant, machinery will require maintenance. 
* If it is not maintained you can have delays in production/progress whether it's a fault that needs to be fixed or even clean up work if leakages occur. 
* Maintenance can be solved by having people on duty (night and day) to be ready in the event of a failure. 
* The issue with this is that it costs money to have someone on site nearly 24/7 and the people on duty aren't necessarily enjoying their work as nothing may be occuring. This model could lessen that.

## Who this benefits
* 👨‍🏭 **Plant management** - if you can identify periods of time that may require maintenance you do not have to be inefficient with time and monitor equipment and people all the time. As a plant manager you may need to know about 100 things that are occuring at the same time but if you can forecast some of them accurately you can reduce this number. As well as this maintenance crews can be deployed or told when to be on call rather than requiring them to be on site nearly 24/7 throughout the year, even holidays. If there is a high likelihood of equipment requiring maintenance and there isn't a part in the inventory you can order it before the maintenance is required stopping the potential delay from not have equipment up and running.
* 🛠️ **Maintenance crews** - no one wants to be on call or on site for hours at a time and not be required to repair anything. If the model forecast is accurate you can have them on site only when they are required thus making them not have to be on site when not needed, making them happier in the process.
* 🏭 **Company** - not requiring maintenance crews to be on site throughout the year saves on costs. This money can then be fed back into the business and better utilised.

## Idea used for the modelling
`tsai` contains `SlidingWindow`. This allows you to take the data and split it into subsets of data where the Xs are all inputs over the window period and Y is the value for e.g. the Y value after the period. It can be represented as this. I've found it very useful to setup data for time series work.
![image](https://user-images.githubusercontent.com/70057706/109543101-d66ff080-7abd-11eb-8f92-5b4aff5661e1.png)

## Residual Dynamics
During training and experiments I created a callback using `fastai`'s framework called `ResidualDynamics` ![repo](https://github.com/Lion-Mod/ResidualDynamics). I took inspiration from another callback `PredictionDynamics` which plots ground truth against predictions but I was keen to see residuals more clearly to see if the model is over or underpredicting.

Visually
Blue = residual dynamics
Green = prediction dynamics
![residualdynamicsexample](https://user-images.githubusercontent.com/70057706/109860509-2a154200-7c56-11eb-9f14-d273e4408ab7.gif)
