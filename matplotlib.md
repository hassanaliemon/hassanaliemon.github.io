The %matplotlib inline will make your plot outputs appear and be stored within the notebook.
According to [documentation](http://ipython.readthedocs.io/en/stable/interactive/plotting.html)


To set this up, before any plotting or import of matplotlib is performed you must execute the %matplotlib magic command. This performs the necessary behind-the-scenes setup for IPython to work correctly hand in hand with matplotlib; it does not, however, actually execute any Python import commands, that is, no names are added to the namespace.

A particularly interesting backend, provided by IPython, is the inline backend. This is available only for the Jupyter Notebook and the Jupyter QtConsole. It can be invoked as follows:

```py
%matplotlib inline

```
With this backend, the output of plotting commands is displayed inline within frontends like the Jupyter notebook, directly below the code cell that produced it. The resulting plots will then also be stored in the notebook document.

Reference: https://stackoverflow.com/questions/43027980/purpose-of-matplotlib-inline
