An application of Pythagorean Expectation to Australian Rules Football
================

## Background

Pythagorean expectation (PE) is a sports analytics metric developed for
baseball that evaluates and estimates the proportion or number of games
a team “should” have won based on the number of runs scored relative to
runs allowed. In principle. PE allows us to analyse whether teams are
“under” or “over”-performing relative to their actual record.

The appeal of PE is in its relative simplicity, with the basic the basic
expectation formula:

$$ 
Win.percentage\_{it}= \\frac{points.scored\_{it}^2}{points.scored\_{it}^2+points.allowed\_{it}^2}
$$

where *i* is a given team at season *t*.

This formula can simplified and generalised to the following, where *k*
is an optimal exponent (which tends to differ from sport-to-sport).

$$ 
Win.percentage\_{it} = \\frac{1}{1+(\\frac{points.allowed\_{it}}{points.scored\_{it}})^k} 
$$

PE has been applied to sports beyond baseball, including American
Football, soccer and basketball, and empirically tends to be correlated
with actual win percentage. With that in mind, we take a dive into PE in
the Australian Rules Football (AFL) context and apply a simple
implementation of the formula to gather insights, including:

-   Determining an optimal *k* exponent for AFL;
-   The extent to which expected wins correlates with actual wins;
-   Understanding whether PE is useful in assessing the over or
    under-performance of teams, and
-   How useful over/under-performance is as a predictor of next season
    performance.
