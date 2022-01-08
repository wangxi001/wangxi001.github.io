---
layout: post
title: << Physical Models of Living Systems >> by Philip Nelson
---
Sin^2 + Cos^2 = 1
This book introduces various classical mathematical models of biological systems. 

It is a great book if you have already been exposed to biology, statistics and modeling.

My favoriate part of is about its visulization of real data. Sometimes having those figure in memory can be quiet helpful when you see it again in one's own research.

## 1. Virual clearance after anti-HIV drug treatment

The goal is to test if HIV is under fast reproduction and evolution in human body. AIDS patients typically experience a long latency period with low viral load that can take up to 10 years, before symptoms appear.

<img src="/Physical-Models/Fig.0.3.png" alt="drawing" width="500"/>

When antiretroviral drugs are used on patients, as we can see, the balance of HIV production and clearance in their body is disrupted, as virus concentration drops rapidly on a semilog plot. It implies that the immune system is clearing virus at a tremendous rate. 

However, this rapid fall doesn't start at the moment the drug is administered. The reasoning behind is that although drugs block HIV from infecting new T cells, the cells already infected can still release virus. T cell infection is also when reverse transcription of occurs. It is the main source of mutation, so what we actually want to know is the clearence rate of infected T cells.

<img src="/Physical-Models/Fig.1.2.png" alt="drawing" width="500"/>

We can draw equations for change of infected cell quantity:

<img src="/Physical-Models/Eq.1.1.png" alt="drawing" width="190"/>

amd change of virus concentration:

<img src="/Physical-Models/Eq.1.2.png" alt="drawing" width="160"/>

Replacing *N*<sub>I</sub> in the second equation give us: 

<img src="/Physical-Models/Eq.1.3.png" alt="drawing" width="200"/>

It shows that the virus concentration is determined by two exponential terms and their parameters *k*_I, *k*<sub>V</sub>. Long time behavior of the equation will be dominated by the one with smaller parameter. 

In the case *k*<sub markdown="1">I</sub> >> *k*<sub markdown="1">V</sub>, releasing of new virus from infected T cells quickly shuts off. Residual virus drop exponentially depends at rate *k*<sub markdown="1">V</sub>. 

In the other case *k*<sub markdown="1">V</sub> >> *k*<sub markdown="1">I</sub>, exisiting virus are quickly cleared. The clearance rate later is only controlled by *k*<sub markdown="1">I</sub>.

By fitting data to the model, we can show 1/*k*<sub markdown="1">I</sub> is much smaller than 10 years. We can further show that the infection rate of virus is so fast that make is possible for the population of virus to carry every possible single nucleotide mutation at the same time. It explains why HIV can be resistant to any single drug, and motivate the treatment of drug combinations.


/
/
/

PS: Here's how I feel about probabilistic modeling vs deep learning.
  
### Probabilistic modeling text books:
  
We have a problem -> and some experimental data -> We make some assumptions about the systems -> We derive a set of equations/do some simulations -> We comapre results with data to find optimal parameter -> We have a model, now make some new predictions
  
### Deep learning text books:

We have a problem -> We have some data, labeled as 0/1 -> Neural network is ready to go -> ... -> Boom! We trained a model!  


