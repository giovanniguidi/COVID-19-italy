### COVID-19 analyis

This is a simple analyis of the spread of COVID-19 in italy


### Data

Download data from the github account of the official italian autorities (Presidenza del Consiglio dei Ministri - Dipartimento della Protezione Civile) 

https://github.com/pcm-dpc/COVID-19

Run the notebook for an exploratory data analysis with some simple plots

### The model


The SIR epidemic model is a simple mathematical description of the spread of a disease in a population. 
The model divides the population of N individuals (fixed) into three categories, which vary as a function of time:

S(t) are those susceptible but not yet infected with the disease;
I(t) is the number of infectious individuals;
R(t) are those individuals who have recovered from the disease and now have immunity to it.

The SIR model describes the change in the population of each of these compartments in terms of two parameters, beta and gamma. 

Beta describes the effective contact rate of the disease: an infected individual comes into contact with βN other individuals per unit time (of which the fraction that are susceptible to contracting the disease is S/N). 

γ is the mean recovery rate, namelt 1/γ is the mean period of time during which an infected individual can pass it on.

The differential equations describing this model were first derived by Kermack and McKendrick [Proc. R. Soc. A, 115, 772 (1927)]:

dS/dt = - beta SI/N

dI/dt = beta SI/N - gamma I

dR/dt = gamma I