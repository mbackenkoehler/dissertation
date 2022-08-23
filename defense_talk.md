# Dissertation Talk

## Motivation and goals
* small volumes (biological systems: die-out scenarios, switches, gene states, ...) (informatics: queueing models) require stochastic descriptions
* stochasticity often ignored in the large volume approx.
* create _reliable_ methods for continuous-time discrete population processes
* hint at approximative descriptions using moments and direct state aggregation

## Model class
* discrete states, continuous-time
* long-term dynamics 
	* Foster-Lyapunov functions -> local augmentation

## Moment dynamics
* Less variables to consider, stochasticity still represented (however: cannot be directly numerically integrated...)
* partial integration along with time-weighting yield constraints involving moment time-integrals

## Mean first-passage times
* occupation measure and exit time distributions
* linear moment constraints imply a martingale (Doob's thm.)
* positive measures have PSD _moment matrices_
* this yields an semi-definite program that can give bounds on all moments
* alternative: if the time-and-state space is finite, use Hausdorff constraints

## Linear control variates
* 

## State-space aggregation

## Stationary distribution

## The bridging problem

## Aggregation for importance sampling