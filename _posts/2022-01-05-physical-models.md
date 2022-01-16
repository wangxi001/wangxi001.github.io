---
layout: post
title: << Physical Models of Living Systems >> by Philip Nelson
---


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

It shows that the virus concentration is determined by two exponential terms and their parameters *k*<sub> I </sub>, *k*<sub>V</sub>. Long time behavior of the equation will be dominated by the term with smaller parameter value.

In the case *k*<sub markdown="1"> I </sub> >> *k*<sub markdown="1">V</sub>, releasing of new virus from infected T cells quickly shuts off. Residual virus drop exponentially depends at rate *k*<sub markdown="1">V</sub>. 

In the other case *k*<sub markdown="1">V</sub> >> *k*<sub markdown="1">I</sub>, exisiting virus are quickly cleared. The clearance rate later is controlled by *k*<sub markdown="1">I</sub>.

By fitting data to the model, we can show 1/*k*<sub markdown="1">I</sub> is much smaller than 10 years. We can further show that the infection rate of virus is so fast that make is possible for the population of virus to carry every possible single nucleotide mutation at the same time. It explains why HIV can be resistant to any single drug, and motivate the treatment of drug combinations.

  
## 2. Counting fluorescent molecules in a cell

The fluorescent intensity of molecules depend on their number. However, it is difficult to find the normalization constant &alpha; for this proportional relationship. 

To solve that, people noticed that during cell division, the cell's volume splits into nearly equal halves. In a daughter cell, the number of fluorescent molecules *M*<sub>1</sub> is binomial according to *P*<sub>binom</sub>(*M*<sub>1</sub> ;1/2, *M*<sub>0</sub>).

Thus the variance of &Delta;*M* = *M*<sub>1</sub> - *M*<sub>2</sub> and fluorescent intensity *y* = &alpha;*M* are given by:

<img src="/Physical-Models/Binomial.1.png" alt="drawing" width="320"/>

<img src="/Physical-Models/Binomial.2.png" alt="drawing" width="290"/>

Fitting the last equation to different *y*<sub>0</sub> will allow estimation of &alpha;.

<img src="/Physical-Models/Fig.4.2.png" alt="drawing" width="400"/>

## 3. Bacteria genetics: Lamarckian vs Darwian inheritance

Until the turn of 20th century, people were still actively debating about the nature of inheritance. One pole held that heritable changes occur spontaneously in an organism, and that evolution is the result of enviromental selection applied to such mutation (Darwian). The other extreme held that organisms activly create heritable changes in response to enviromental stress (Lamarckian). 

**S.Luria** and **M.Delbruck** set out to explore these two hypotheses before DNA was determined as genetic material. They worked on bacterial resistance. They created a large collection of separate culture of *E.Coli*. After proliferating for a while, bacterias were challenged by a virus called phage. The scientists then counted the number of survivors in each culture.

<img src="/Physical-Models/Fig.4.7.png" alt="drawing" width="500"/>

***H1***, the Lamarckian hypothesis argues that whether a bacteria become resistant is a random decision independent of others, given that mutations only arise at phage challenge stage. Obeserving m survivors should distributes as a Poisson random variable. 

<img src="/Physical-Models/Fig.4.6.png" alt="drawing" width="250"/>

However, the result did not look like poisson because it had some 'outliers' at large m. It is also named as jackpot distribution.

***H2***, the Darwian hypothesis, implies early mutants will be amplified during proliferation, as mutations are spontaneous.

<img src="/Physical-Models/Fig.4.8.png" alt="drawing" width="450"/>

Plotting simluation result of ***H2*** on semilog form confirms it's more consistent than poisson model. It properly represents randomness in inheritance. Another way to see the failure of ***H1*** is to note that experimental data have sample mean = 30 but
 variance = 6000.
 
The mutation rate can also be estimated from the simulation to be on the order of 10<sup>-8</sup>.

## Single partical reconstruction in cryo-electron microscopy
 
/
/
/

PS: Here's how I feel about probabilistic modeling vs deep learning.
  
### Probabilistic modeling text books:
  
We have a problem -> and some experimental data -> We make some assumptions about the systems -> We derive a set of equations/do some simulations -> We comapre results with data to find optimal parameter -> We have a model, now make some new predictions
  
### Deep learning text books:

We have a problem -> We have some data, labeled as 0/1 -> Neural network is ready to go -> ... -> Boom! We trained a model!  


