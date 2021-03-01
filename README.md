# My electrophoresis sense is tingling

## Predictive maintenance
When will an electrophoresis plant require maintenance? Predicting if it will require maintenance using previous values of sensor readings.

## Why this was done
Time series data is a new challenge and I wanted to combine this with a library I've been exploring `tsai` (fastai extension focused on time series). 

Simply put maintenance costs time and money. If you are running a manufacturing plant or in this case a electrophoresis plant, machinery will require maintenance. If it is not maintained you can have delays in production/progress whether it's a fault that needs to be fixed or even clean up work if something may overflow. Maintenance can be solved by having people on duty (night and day) to be ready in the event of a failure. The issue with this is that it costs money to have someone available and on site nearly 24/7 and the people on duty aren't necessarily enjoying their work as nothing may be occuring. This model could lessen that.

## Who this benefits
* 👨‍🏭 **Plant management** - if you can identify periods of time that may require maintenance you do not have to be inefficient with time and monitor equipment and people all the time. As a plant manager you may need to know about 100 things that are occuring at the same time but if you can forecast it accurately you can reduce this number. As well as this maintenance crew can be deployed or told when to be on call rather than requiring them to be on site nearly 24/7 throughout the year, even holidays. If there is a high likihood of equipment requiring maintenance and there isn't a part in the inventory you can order it before the maintenance is required stopping the potential delay from not have equipment up and running.
* 🛠️ **Maintenance crews** - no one wants to be on call or on site for hours at a time and not be required to repair anything. If the forecast is accurate you can have them on site only when they are required thus making them not have to be on site when not needed, making them happier in the process.
* 🏭 **Company** - not requiring maintenance crews to be on site throughout the year saves on costs. This money can then be fed back into the business or better utilised.
