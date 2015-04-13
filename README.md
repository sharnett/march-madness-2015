#Using integer programming and portfolio optimization to pick a March Madness bracket

In this notebook I explore the use of an [integer program](http://en.wikipedia.org/wiki/Integer_programming) solver in Python to pick an optimal March Madness bracket.

I use the [cvxopt](http://cvxopt.org/) Python interface to the [glpk](https://www.gnu.org/software/glpk/) solver, both freely available. I also use pandas and numpy. Installing cvxopt and glpk was simple but not completely straightforward; see the appendix at the end for how I did it.

The file `bracket-05.tsv` is copied from [fivethirtyeight](https://github.com/fivethirtyeight/data/tree/master/march-madness-predictions-2015).