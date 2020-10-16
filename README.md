# Summary

A project for automatically scraping these Wikipedia articles:

* [United States presidential election, 2016](https://en.wikipedia.org/wiki/United_States_presidential_election,_2016)
* [United States presidential election, 2012](https://en.wikipedia.org/wiki/United_States_presidential_election,_2012)
* [United States presidential election, 2008](https://en.wikipedia.org/wiki/United_States_presidential_election,_2008)
* [United States presidential election, 2004](https://en.wikipedia.org/wiki/United_States_presidential_election,_2004)
* [United States presidential election, 2000](https://en.wikipedia.org/wiki/United_States_presidential_election,_2000)

They are scraped for the state-level popular vote results, and then the methodology
of my blog post,
[Fair, Efficient State-wise Electoral College Vote Allocation](https://dalevisser.wordpress.com/2016/12/08/fair-efficient-state-wise-electoral-college-vote-allocation/), is applied.

## Instructions

### View on Jupyter.org

The GitHub native rendering of the notebook doesn't always work, but there is always
[nbviewer.jupyter.org](https://nbviewer.jupyter.org/github/dwvisser/electoral-fair/blob/master/scrape-and-compute-all.ipynb)

### Docker

If you have Docker, the *jupyter/scipy-notebook* image on Docker hub has all needed
dependencies. The following assumes you have a typical UID = 1000. If not, you can
try adding `--user 5000 --group-add users` to the options in the command below. See
[here](https://jupyter-docker-stacks.readthedocs.io/en/latest/using/common.html) for
full details.

1. `docker run -it --rm -e JUPYTER_ENABLE_LAB=yes -p 8888:8888 --mount type=bind,source="$(pwd)",target=/home/jovyan/work jupyter/scipy-notebook:latest`
2. Open the notebook file under the *work/* folder and run it, or play with it as you
   see fit.

A [Dockerfile](Dockerfile) and [.devcontainer folder](.devcontainer) are provided,
which make it easy to launch the notebook inside Visual Studio Code using its
*Remote-Containers* extension, via the
`Remote-Containers: Open Folder in Container...` command.

### Anaconda

The notebook was developed on Linux Mint, and the following instructions
should be easily translatable to other Linux environments, or even any system
that can run Anaconda.

1. Install [Anaconda](https://www.continuum.io/why-anaconda).
2. `conda env create -f environment.yml`
3. `source activate electoral-fair`
4. `jupyter notebook`
5. Open the notebook files and run it, or play with it as you see fit.
