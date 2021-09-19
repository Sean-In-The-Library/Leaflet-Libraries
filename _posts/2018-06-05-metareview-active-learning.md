---
layout: post
title: Meta-review on active learning strategies in digital learning environments
thumbnail: "/img/og_activelearning.png"
---

After a few years of conducting experiments in the MOOC environment and often finding that we were not able to replicate major insights from prior studies (conducted in the lab, classroom, a specifically designed online learning environment), we had an inkling that MOOC environments are tougher to crack. In order to turn this inkling into a scientific study we conducted a meta-review of so-called active learning strategies (strategies that involve learners in the learning process, e.g. gammification, cooperative learning) in the MOOC and other online learning environments. This study ([preprint](https://chauff.github.io/documents/publications/CE2018-Davis.pdf)), led by [Dan Davis](https://dan7davis.github.io/), was just published in the [Computers and Education](https://www.sciencedirect.com/journal/computers-and-education) 
journal:

```bibtex
@article{CE2018ActiveLearning,
  author = {Dan Davis, Guanliang Chen, Claudia Hauff and Geert-Jan Houben},
  title = {Activating learning at scale: A review of innovations in online learning strategies},
  journal = {Computers \& Education},
  volume = {...},
  number = {...},
  pages = {...},
  year = {2018}
}
```

As a starting point to our meta-review we took [John Hattie's seminal work from 2008](https://www.taylorfrancis.com/books/9781134024124): _Visible learning: A synthesis of over 800 meta-analyses 
relating to achievement_ on learning strategies used to facilitate active learning. 
We considered **research published between 2009 and July 2017** that present empirical evaluations of these learning strategies.

We identified 7,706 papers in a first literature search round and used three criteria to determine whether a paper should be
in or out of our meta-review:

1. The learning  strategy  being  analyzed  must  have  been **scalable** (it does not require manual grading, feedback,
physical presence, etc.).
2. The evidence must come from empirical analyses of **randomized controlled experiments** with a combined
sample size of **at least ten** across all conditions. 
3. The subjects of the studies must be **adult learners**.

This resulted in **126** papers (1.6%) meeting our criteria; it turned out that the requirement of a 
randomized controlled trial was a very strict one that most papers failed. Often, reported experiments focused solely on
the developed learning intervention, instead of a comparison between a control and one or more experimental conditions.

Lets now look at a few key summary graphs of those 126 papers (ignoring the learning strategy specifics for now).

<img src="https://chauff.github.io/img/by_all.png" width="700px">

Above, we split the 126 papers according to the digital learning environment the reported experiments was conducted in
(take into account that for 2017 we only include papers published by July of that year). *Native environments*, i.e. software designed and implemented specifically for the experiment, turned out to be the most 
popular. MOOC-based experiments started to appear in 2014, MTurk-based experiments appeared at around the same time. 

<img src="https://chauff.github.io/img/by_env.png" width="700px">

How successful (i.e. how often is the intervention reported to perform better than the control condition) are the
different environments? In the graph above and all that follow, a "-" indicates studies reporting a significant negative effect of the intervention; the "+" indicates a significant positive effect of the intervention; and the "o" indicates findings without a statistically significant effect. It turns out that the native environments are the "best" to use to achieve significantly better results; MOOC environments do not fare too well here, more than half of the studies report a non-significant difference between control and experimental conditions. This may not be too surprising as MOOC environments are agnostic to the content topic, while native environments can be designed to fit specific types of content (e.g. language learning).

<img src="https://chauff.github.io/img/by_incentive.png" width="700px">

Above we considered how study participants were incentivized to participate: we found surprisingly many studies without
an incentive/compensation, followed by class-based incentives (credits or requirement for passing a class).

<img src="https://chauff.github.io/img/by_n.png" width="700px">

Lastly, we also checked whether the size of the sample has an impact: it turns out that the larger the sample, the more
likely null results appear to occur. One potential explanation here is the heterogeneity of the MOOC population (many
studies in the 501+ partiicpants category are MOOC-based) with respect to age, prior education, study time ... 
in contrast to class-based studies.

The paper contains more detailed analyses of the different activce learning strategies and how successful prior studies were, so go ahead and [read it](https://chauff.github.io/documents/publications/CE2018-Davis.pdf).
