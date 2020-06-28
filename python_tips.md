# Python Tips/Tricks

## IDE
one of the best IDE (and it works with anaconda) is [intellij][intellij_website], you can use it or use [PyCharm][pycharm_website] which is almost the same. when you download the IDE use the community version. The IDE is very great for debugging as well as syntax correction/auto-complete and support other languages including Fortran and c++
## Anaconda
you can install [Anaconda][anaconda_website] by downloading the installation file. See the [cheatsheet][conda_cheatsheet] for most used commands. Try always when it's possible to install packages from ``conda-forge`` source. Below an example.
```shell script
$ conda install -c conda-forge packages_name
```

## Jupyter Lab
### How to activate interactive plots
1. Install nodejs, e.g. ``conda install nodejs``
1. Install ipympl, e.g. ``pip install ipympl``
1. run:
    ```shell script
    $ export JUPYTERLAB_DIR="$HOME/.local/share/jupyter/lab"
    ```
1. Install extensions:
    ```shell script
    $ jupyter labextension install @jupyter-widgets/jupyterlab-manager
    $ jupyter labextension install jupyter-matplotlib
    ```
1. Enable widgets:
    ```shell script
    $ jupyter nbextension enable --py widgetsnbextension
    ```
1. Restart JupyterLab.
1.  Decorate your Jupyter notebook file with ``%matplotlib widget``

for more info visit [this page](https://stackoverflow.com/questions/50149562/jupyterlab-interactive-plot)


[//]: # (These are reference links used in the body of this note and get stripped out when the markdown processor does its job. There is no need to format nicely because it shouldn't be seen. Thanks SO - http://stackoverflow.com/questions/4823468/store-comments-in-markdown-syntax)
   [intellij_website]:<https://www.jetbrains.com/idea/download/>
   [pycharm_website]: <https://www.jetbrains.com/pycharm/download/>
   [anaconda_website]: <https://www.anaconda.com/products/individual>
   [conda_cheatsheet]: <https://docs.conda.io/projects/conda/en/latest/user-guide/cheatsheet.html>
