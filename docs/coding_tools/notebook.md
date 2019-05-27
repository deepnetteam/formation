
Jupyter notebook
==============

We usually write python scripts and functions in `.py` files, and execute them using an IDE or the command line. There are three main limitation that [Jupyter notebook](https://jupyter.org) has successfully addressed, making it our tool of choice when writing and sharing code.

## Debugging code
**Problem:** Run your code, it runs once and closes afterward. From this point, if you want to get insight on variables, states, and such in the middle of the algorithm, your only choice is to rerun your code and add a few debugging statements. This is time consuming, and inefficient, especially when your code depends on a lot of big libraries that take a good few seconds to load each time you run your script again.
**Solution:** A notebook is composed of cell that can be run in any order, at any point. By dividing your script in multiple sub parts, you can effectively check the state of your environment at any time. And you only need to load libraries once !

## Sharing results
**Problem:** A simple python script requires to be run on one's computer to see the results, which can prove complicated if they are specific libraries requirements or a long computing time.

**Solution:** A notebook saves the output of each cell, making it possible to share the results you obtained on your own computer. Because it also *supports plotting via pyplot, PIL and more*, you can use notebook as a real presentation tool.
As a bonus, notebook file are *already supported by Github and Gitlab*, making them that much of a better code sharing tool.

## Sharing code and environments
**Problem:** If you're starting with deep learning, you may have a hard time installing the correct working environment. If you choose to take collaborative coding into account, this choice can become a real headache...
**Solution:** [JupyterHub](https://jupyter.org/hub) Allows us to share working environments as well as code, 
