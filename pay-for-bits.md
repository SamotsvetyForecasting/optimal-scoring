---
title: "Pay for bits: Probably a Better Method for Rewarding Forecasters"
author: Nuño Sempere\footnote{Quantified Uncertainty Research Institute.}
date: \today
urlcolor: blue
---

# Motivation

In [Alignment Problems With Current Forecasting Platforms](https://arxiv.org/abs/2106.11248), Sempere and Lawsen outline a variety of problems with current forecasting platforms, whose scoring rules are found to either not be proper—as in the case of Good Judgment Open or CSET-Foretell (now INFER)—or incentivize distorting one's true probabilities to maximize the chances of placing in the top few positions which earn a monetary reward—as in the case of Metaculus. In addition, in almost all cases, forecasting platforms—or, for that matter, prediction markets—disincentivize collaboration.

In this working paper, we outline an incentivization method, "paying for bits", which combines features of prediction markets and forecasting platforms to produce a scoring rule that pays forecasters well, is proper, and nonetheless incentivizes collaboration. This scoring rule has both a discrete form—where resolution is either a yes or a no, and a continuous form—where resolution can be any probability between 0 and 1. 

In essence, we start out with the logarithmic scoring rule, and we add a few bells and whistles to make it collaborative. We also reinterpret it using the concept of a prediction market with an automatic market maker, which is a better abstraction because it deals more elegantly with bounding the potential loss.

In two accompanying papers, Amplify Samotsvety and Amplify Rootclaim, we use this continuous form like a lego-block: we combine it with other methods to build more powerful and general incentive schemes.

# Practical limitations of previous scoring rules

## Practical limitations of the Brier score.
The Brier score has limitations stemming from its deep theoretical inelegance. Sure, it is proper, but it also doesn't have desirable properties such as:

- Composability: The Brier score on "A" and the Brier score on "B given A" can't be straightforwardly related to the Brier score on "A and B"
- Comparability: The cummulative relative Brier score doesn't correspond to any particular meaning.
- Comparability II: The Brier score of the average guess will always be at least as good as the average of the Brier scores, and usually better. This incentivizes forecasters to forecast the average

Overall, the Brier score is a hack. [reword to be less informal]

## Advantages and limitations of the logarithmic scoring rule.

Define the log score as log(p/q), where p is the guess, and q is the comparison point. Normally the comparison point will be the aggregate, but making the comparison point the prior is much nicer.

The logarithmic scoring rule is proper and has desirable properties:

- Composability: The logarithmic score on "A&B" is the sum of the log scores on "A" and "B given A"
- Comparability: The cummulative relative log score corresponds to bits of information which would be added or removed
- Comparability II: The arithmetic mean of the log scores is the log score of the geometric mean of the guesses. If forecasters are rewarded in proportion to their log score, there is no advantage to forecasting the current crowd.

More general, for many nice theoretical properties, the log score will have them, whereas the Brier score will not. 

The only nice propert

## Advantages and limitations of previous comparison points
To determine the relative quality of forecasters, previously several comparison points have been used:
- The aggregate of other forecasters. E.g., relative scores.	
- Nothing (e.g., average or cummulative scores)

The first option has the advantage that it indeed produces a ranking. But it introduces a zero sum component.

The second option still generates a ranking. But it incentivizes forecasters to forecast on easier questions.

The alternative proposed throughtout this paper is:
- Improvement over the prior
- Weighted by importance

This creates a more meaningful metric: importance-adjusted bits of informations added to the decision-maker's initial forecast. From Bayesian probability theory, we get the strong hint that probabilities without priors don't really make sense, so that might be a hint that we want comparisons vis a vis a prior.

# Description of the method.

In the interest of brevity, we shall outline our method by means of an example, and the example shall be the question "Will the People's Republic of China have annexed at least half of Taiwan by 2050?", as operationalized by [Metaculus](https://www.metaculus.com/questions/5320/chinese-annexation-of-most-of-taiwan-by-2050/). Parts which justify or explain the use of other parts are explained first, even if they would come later in terms of time.

## The patron determines a rough prior to reduce potential forecasting reward.

Taiwan has been independent of mainland China since the 25th of October 1945, i.e., 76 years into the past. Per Laplace's law, the chances that this will change by 2050 is $1-(1-\frac{1}{(2021-1945)+1})^{2050-2021} \approx 32\%$. Lets take this $32\%$ as Rootclaim's initial probability. Note that per the [reference class problem](https://en.wikipedia.org/wiki/Reference_class_problem), other reference classes might have been chosen, so the point of this prior is not to be definitive, but rather to provide a starting point less arbitrary than 50\% from which forecaster reward might be computed in the next steps. 

By sharing this initial step, the 

In the case of a patron aiming to learn from sponsoring a forecasting tournament, the prior might represent the patron's initial probability. If the patron is unsophisticated and the question is not amenable to base-rate analysis, we may use a 50%. Alternatively, the patron may sub-contract the creation of the prior, for instance by paying other forecasters to quickly do so or by creating low-liquidity (and thus low-potential reward) prediction markets.

## Forecasters predict on the question

## The question gets a binary resolution 

## The question gets a probabilistic resolution and 

### Because of uncertain ontologies

### Because of probabilistic knowledge

### Because the question hasn't resolved yet

## Conclusion

---


Forecasters each predict in their own prediction market, seeded with funds by the patron. They thus have an incentive to collaborate.

Similarities to log score. There is an AMM rule which corresponds to log scoring?

https://www.cs.cmu.edu/~sandholm/liquidity-sensitive%20automated%20market%20maker.teac.pdf
