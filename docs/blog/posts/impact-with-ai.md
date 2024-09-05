---
title: How to drive impact with AI?
date: 2024-07-08
authors:
  - mike
---

Most AI projects fail. In my experience, they fail for three reasons:

1. Shaky foundation to build on
2. Poorly defined model "delivery" & objectives
3. Lack of TLC post deployment

Avoiding these three mistakes will play a **huge** role in your success (+ having a strong data science team or partner).


### Shaky Foundation
Let's mix metaphors a bit. AI/ML models have an endless appetite for data & will "eat" what they are given. Model performance heavily relies on quality of data they consume.

Checklist:

1. We need to source ingredients (data collection)
2. We need a kitchen (database)
2. We need a cook (data prep, analysis, and manipulation)
3. We need a server (deliver data to model)

Take predicting the proper amount to bid on a Google search ad. Do we collect past bids, relevant details, and clicks/conversions? Where is this data stored? Has anyone done exploratory data analysis on the data (bonus if automated data quality checks)?

### Poorly Defined
#### Delivery
We have two straight-forward options that meaningfully change the approach:

1. Make predictions on a schedule, store in a database (e.g predict nightly)
2. Make predictions on demand, log predictions for future evaluation

Both approaches work well. The choice is dependent on data availability and objectives.

#### Objectives
A seemingly straight-forward step can cause outsized "pain" when not done well.

Hint: An objective of "make thing better" is bad, "increase measureable aspect of thing" is good.

Expanding on our Google search ads example. We want to predict how much to bid on an ad. What do we want to happen? Bidding zero always minimizes cost, bidding $1M maximizes clicks...

There are many metrics to optimize. Thoughtfully aligning our objectives with larger business goals is critical.

We could have plenty of objectives. From increase clicks, conversions or customers; maximize return on ad spend or customer lifetime value; lower customer acquisition cost.

Each of these objectives has trade-offs. Increase conversions could blow up spend, maximize return on ad spend could drop customer growth meaningfully.

Say cost efficiency is business goal, optimizing revenue from conversion to acquisition cost is a good objective.


### TLC Post Deployment
Being able to deploy an AI model is exciting. It is easy to "set & forget" but AI models require continuous monitoring and optimization.

Staying up-to-date on 

* Does the input data to the model shift over time?
* Are my evaluation metrics changing?
* Did a model retraining "break" performance?
* Are we collecting the right data for future optimizations?

If these questions are managed, it is inevitable that performance will eventually degrade.
