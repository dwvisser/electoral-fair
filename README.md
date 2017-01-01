Summary
=======

A project for automatically scraping these Wikipedia articles:

* [United States presidential election, 2016](https://en.wikipedia.org/wiki/United_States_presidential_election,_2016)
* [United States presidential election, 2012](https://en.wikipedia.org/wiki/United_States_presidential_election,_2012)
* [United States presidential election, 2000](https://en.wikipedia.org/wiki/United_States_presidential_election,_2000)

They are scraped for the state-level popular vote results, and then the methodology of my blog post,
[Fair, Efficient State-wise Electoral College Vote Allocation](https://dalevisser.wordpress.com/2016/12/08/fair-efficient-state-wise-electoral-college-vote-allocation/), is applied.

Instructions
============

The notebook was developed on Linux Mint, and the following instructions
should be easily translatable to other Linux environments, or even any system
that can run Anaconda.

1. Install [Anaconda](https://www.continuum.io/why-anaconda).
2. `conda env create -f environment.yml`
3. `source activate electoral-fair`
4. `jupyter notebook`
5. Open the notebook files and run them, or play with thems as you see fit.
   (That's the beauty of releasing this under open source license!)

