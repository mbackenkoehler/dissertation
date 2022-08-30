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

### Hausdorff
* time-and-state space is finite
* Hausdorff constraints
* linear program (often more well-behaved)

## Linear control variates
* use the martingale as a secondary rv
* this rv's expectation is known (its 0) and often it is correlated with the target rv (i.e. a covariate)
* use the correlation in a linear model to _adjust_ the Monte Carlo estimate of the target rv
* task: choose a _good_ subset of covariates
* good trade-off between computational cost and variance reduction
* two algorithms:

### Filtering an initial set
* initial set of covariates based on time-weighting parameter distribution
* this set is shrunk during the initial iterations
* removal heuristics based on pairwise correlations between all RVs

### Sequential Monte Carlo
* goal: less dependence on lambda "prior"
* resample promising parameters for existing moments

## State-space aggregation
* interval-based macro-states
* assumption: uniform distribution within macro-states
* hyper-cube transition states make computation of rate transitions trivial
* method: use this approximation to make a rough analysis and refine

## Stationary distribution
* Lyapunov sets are too large
* Refine towards a FSP

## The bridging problem
* combine aggregate foward and backward probabilities
* refine and obtain a FSP tailored to initial and terminal constraints

## Aggregation for importance sampling