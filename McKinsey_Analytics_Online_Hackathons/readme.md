## Problem Statement

Your client is an Insurance company and they need your help in building a model to predict the propensity to pay renewal premium and build an incentive plan for its agents to maximise the net revenue (i.e. renewals - incentives given to collect the renewals) collected from the policies post their issuance.

 
You have information about past transactions from the policy holders along with their demographics. The client has provided aggregated historical transactional data like number of premiums delayed by 3/ 6/ 12 months across all the products, number of premiums paid, customer sourcing channel and customer demographics like age, monthly income and area type.

 
In addition to the information above, the client has provided the following relationships:

    - Expected effort in hours put in by an agent for incentives provided; and
    - Expected increase in chances of renewal, given the effort from the agent.

 

Given the information, the client wants you to predict the propensity of renewal collection and create an incentive plan for agents (at policy level) to maximise the net revenues from these policies.

## EVALUATION CRITERIA

Your solutions will be evaluated on 2 criteria:

    - The base probability of receiving a premium on a policy without considering any incentive
    - The monthly incentives you will provide on each policy to maximize the net revenue 

### Part A:

The probabilities predicted by the participants would be evaluated using AUC ROC score.

 
### Part B:

The net revenue across all policies will be calculated in the following manner:

[formula-image](https://s3-ap-south-1.amazonaws.com/av-blog-media/wp-content/uploads/2018/07/Mckinsey_Image.jpg)


    - pbenchmark is the renewal probability predicted using a benchmark model by the insurance company
    - ∆p (% Improvement in renewal probability*pbenchmark) is the improvement in renewal probability calculated from the agent efforts in hours
    - ‘Premium on policy’ is the premium paid by the policy holder for the policy in consideration
    - ‘Incentive on policy’ is the incentive given to the agent for increasing the chance of renewal (estimated by the participant) for each policy


The following curve provide the relationship between extra effort in hours invested by the agent with Incentive to the agent and % improvement in renewal probability vs agent effort in hours.

1. Relationship b/w Extra efforts in hours invested by an agent and Incentive to agent. After a point more incentives does not convert to extra efforts.

Equation for the effort-incentives curve: Y = 10*(1-exp(-X/400))

2. Relationship between % improvement in renewal probability vs Agent effort in hours. The renewal probability cannot be improved beyond a certain level even with more efforts.

Equation for the % improvement in renewal prob vs effort curve: Y = 20*(1-exp(-X/5))

Note: The client has used sophisticated psychological research to arrive at these relationships and you can assume them to be true. 

Overall Ranking at the leaderboard would be done using the following equation:

Combined Score = w1*AUC-ROC value + w2*(net revenue collected from all policies)*lambda

Where -

	w1 = 0.7

	w2 = 0.3

	lambda is a normalizing factor


## Dataset

#### train.csv

It contains training data for customers along with renewal premium status (Renewed or Not?)

[]()

#### test.csv

Additionally test file contains premium which is required for the optimizing the incentives for each policy in the test set.

[]()

#### submission.csv

Please submit as per the given sample submission format only

[]()