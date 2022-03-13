---
title: "Foresee Samotsvety: Probably Better Methods for Rewarding Forecasters"
author: Nuño Sempere\footnote{Quantified Uncertainty Research Institute.}
date: \today
urlcolor: blue
---

# Motivation

In [Alignment Problems With Current Forecasting Platforms](https://arxiv.org/abs/2106.11248), Sempere and Lawsen outline a variety of problems with current forecasting platforms, whose scoring rules are found to either not be proper—as in the case of Good Judgment Open or CSET-Foretell (now INFER)—or incentivize distorting one's true probabilities to maximize the chances of placing in the top few positions which earn a monetary reward—as in the case of Metaculus. In addition, in almost all cases, forecasting platforms—or, for that matter, prediction markets—disincentivize collaboration.

Against that backdrop, [Reciprocal Scoring: A Method for Forecasting Unanswerable Questions](https://papers.ssrn.com/sol3/papers.cfm?abstract_id=3954498), Karger et al. describe a method to ellicit predictions in situations in which resolutions are outright not possible, or very far away. They provide some preliminary evidence of its effectiveness in the form of a small randomized trial. However, in the post-peer-review discussion phase in social media, Karger et al.'s method was met with a lukewarm reception from the community of forecasting practitioners, which has grown to view methods which resemble Keynesian Beauty Constests with suspicion.

In this working paper, we outline an alternative incentivization method, "amplify Samotsvety"[^1], which roughly looks as follows:

- There is a trusted central authority which cares about its long-term reputation. This central authority is trusted, but has limited capacity. 
- Forecasters are then rewarded according to a scheme where they forecast on all questions, the central authority predicts on only a few questions chosen randomly, and then forecasters are rewarded according to the proximity of their predictions to that central authority. 

This scheme has the advantage that forecasters can be rewarded speedily for questions which either have no objective resolution or happen far in the future. In addition, if the trusted authority has long horizons, it can be rewarded when the question resolves in the future, or according to the best guess of a future forecasting system.

[^1]: Samotsvety is Russian for "semi-precious stones". It is also the name of a forecasting team in which the authors are involved. 

# Description of the method

In the interest of brevity, we shall outline our method by means of an example, and the example shall be the question "Will the People's Republic of China have annexed at least half of Taiwan by 2050?", as operationalized by [Metaculus](https://www.metaculus.com/questions/5320/chinese-annexation-of-most-of-taiwan-by-2050/). 

## Samotsvety determines a rough prior of all questios, in order to reduce potential reward.

Taiwan has been independent of mainland China since the 25th of October 1945, i.e., 76 years into the past. Per Laplace's law, the chances that this will change by 2050 is $1-(1-\frac{1}{(2021-1945)+1})^{2050-2021} \approx 32\%$. Lets take this $32\%$ as 's initial probability. Note that per the [reference class problem](https://en.wikipedia.org/wiki/Reference_class_problem), other reference classes might have been chosen, so the point of this prior is not to be definitive, but rather to provide a starting point less arbitrary than 50\% from which forecaster reward might be computed in the next steps. In the case of a patron aiming to learn from sponsoring a forecasting tournament, the prior might represent the patron's initial probability.

## Forecasters attempt to foresee Samotsvety's future forecast.

Forecasters spend some effort trying to come up with forecasts which beat the prior. Because each forecaster will be independently rewarded, 

## Samotsvety predicts on a randomly chosen number of questions

Samotsvety

## Forecasters are paid or punished according to how much their probability moves from the prior to Samotsvety's forecast.

## Optionally, after a time, reality is observed, and Samotsvety itself is paid or punished in proportion to their accuracy.

# Discussion of the method

## More on the central authority

## More on the forecasters

## Evidence base and comparison to Karger et al.'s method

## Conclusion

In conclusion, the proposed method of amplifying an expensive but Bayesian approximator has the benefit of appearing more grounded, and not having the weird loops in Karger et al.'s reciprocal scoring proposal—or in other Keynesian beauty contest designs. Further, the existence of Rootclaim provides proof of existence of sch trusted Bayesians approximators. We look forward to someone implementing the method.

***


