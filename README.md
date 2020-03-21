### COVID-19 analyis

This repo contains some tools to analyse and model the spread of COVID-19 in italy


### Data

Clone the repo from the official italian autorities github account (Presidenza del Consiglio dei Ministri - Dipartimento della Protezione Civile). This should be updated on a daily basis. 

https://github.com/pcm-dpc/COVID-19

Run the EDA.ipynb notebook for an exploratory data analysis.

### The baseline model


The SIR epidemic model is a simple mathematical description of the spread of a disease in a population. 
The model divides the population of N individuals (fixed) into three categories, which vary as a function of time:

S(t) are those susceptible but not yet infected with the disease;
I(t) is the number of infectious individuals;
R(t) are those individuals who have recovered from the disease and now have immunity to it.

The SIR model describes the change in the population of each of these compartments in terms of two parameters, beta and gamma. 

&beta; describes the effective contact rate of the disease: an infected individual comes into contact 
with &beta;N other individuals per unit time (of which the fraction that are susceptible to contracting the disease is S/N). 

&gamma; is the mean recovery rate, namely 1/&gamma; is the mean period of time during which an infected individual can pass it on.

The differential equations describing this model were first derived by Kermack and McKendrick in 1927:

```
dS/dt = - β S(t)I(t)/N
dI/dt = β S(t)I(t)/N - γ I(t)
dR/dt = γ I(t)
```

## To do

- [x] find best &beta; and &gamma; with L-BFGS-B optimization, and study the evolution of R0 on time
- [x] data-driven modelling (time-series)
- [x] use Wuhan data to study the effect of quarantine on R0 trend
