Part 2

### Model Overview
- We do not make assumption and abstraction for this model.
- The difference between our model and the one from the paper is that, we do not use "Job Provider" and we divide jobs into different processes.
- There are two main parts in our model, 
  - Linear battery model. It is used to model the linear battery.
  - Job Processes. These processes include all the jobs need to be done.
- Our time unit is minutes. 

### Steps
- First we use python to extract the time interval from the CSV flies. The time window we choose is from March 20, 2016, at 21:00 UTC to March 21, 2016, at 04:00 UTC, which lasts 10 hours. We tranfer and store them in the model.
- Then we define all the parameters, constants, clocks, variables, and functions.
- We define some functions to calculate the cost for each job, which makes the code more clearly.
