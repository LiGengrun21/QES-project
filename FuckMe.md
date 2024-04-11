# Part 2

### Model Overview
- We do not make assumption and abstraction for this model.
- The difference between our model and the one from the paper is that, we do not use "Job Provider" and we divide jobs into different processes.
- There are two main parts in our model
	- Linear battery model. It is used to model the linear battery.
	- Job Processes. These processes include all the jobs need to be done.
- Our time unit is minutes. 

### Steps
- First we use python to extract the time intervals from the CSV flies. The time window we choose is from March 20, 2016, at 21:00 UTC to March 21, 2016, at 04:00 UTC, which lasts 10 hours. We transfer and store them in the model.
- Then we define all the parameters, constants, clocks, variables, and functions.
- We define some functions to calculate the cost for each job, which makes the code more clearly.
	- The main idea of the algorithm for calculating cost is based on how many jobs have been done so far and the ratio of X_Band and L_Band. 
- There are three parts in Linear Battery Model
	- battery is in normal situation
	- battery is fully charged
	- battery is not enough
- We have six processes for jobs. 
	- sun, is used to charge the battery. Based on attitude, there are two different charge power
	- UHF, is used to execute the UHF job
	- L_Band, is used to execute L_Band. We have two different L_Band jobs for two different locations
	- X_Band, is used to execute X_Band. We have two different X_Band jobs for two different locations
- Finally, we use 'par' to make them parallelly.

### Schedule
360 minutes (6 hours). 
	- We also try to set a bigger time window, but this will take more time, which is not convenient to debug. 

690k states done in 2 seconds

Job Schedule:
XBand_toulou
UHF
LBand_3F3
XBand_toulou
XBand_kourou
UHF
LBand_3F3
LBand_3F2
UHF
XBand_kourou
