#Using integer programming and portfolio optimization to pick a March Madness bracket

In this notebook I explore the use of an [integer program](http://en.wikipedia.org/wiki/Integer_programming) solver in Python to pick an optimal March Madness bracket.

I use the [cvxopt](http://cvxopt.org/) Python interface to the [glpk](https://www.gnu.org/software/glpk/) solver, both freely available. I also use pandas and numpy. Installing cvxopt and glpk was simple but not completely straightforward; see the appendix at the end for how I did it.

The file `bracket-05.tsv` is copied from [fivethirtyeight](https://github.com/fivethirtyeight/data/tree/master/march-madness-predictions-2015).

Read the notebook here: http://nbviewer.ipython.org/github/sharnett/march-madness-2015/blob/master/madness.ipynb

<hr>

##Installing cvxopt and glpk

I think this should do the trick.

### Ubuntu

```
sudo apt-get install libglpk36

export CVXOPT_BUILD_GLPK=1
export CVXOPT_GLPK_LIB_DIR=/usr/lib/x86_64-linux-gnu/
export CVXOPT_GLPK_INC_DIR=/usr/include/
pip install cvxopt

python
> from cvxopt.glpk import ilp
```

### Mac

```
brew install homebrew/science/glpk

export CVXOPT_BUILD_GLPK=1
export CVXOPT_GLPK_LIB_DIR=/usr/local/Cellar/glpk/4.52/lib
export CVXOPT_GLPK_INC_DIR=/usr/local/Cellar/glpk/4.52/include
pip install cvxopt

python
> from cvxopt.glpk import ilp
```