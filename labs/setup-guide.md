# Setup Guide

This document is last updated on 3 September 2024.

## Setting up conda

It is often recommended for beginners to install the [Anaconda® Distribution](https://docs.anaconda.com/anaconda/),
which contains:

- conda,
  a specialized software for managing environments and packages;
- Anaconda Navigator, a desktop application;
- Python;
  and
- hundreds of packages.

Please consult [the official documentation](https://docs.anaconda.com/anaconda/install/)
for the installation steps appropriate for your machine.
It is sufficient to use graphical installers and to skip the steps marked optional.
The official site also provides
[how to verify your installation of Anaconda® Distribution](https://docs.anaconda.com/anaconda/install/verify-install/).

A common (and more complex) alternative of setting up conda
is by installing [Miniconda](https://docs.anaconda.com/miniconda/),
which contains only:

- conda;
- Python;
  and
- a minimal number of packages
  (*i.e.*, those that conda and Python depend on,
  and other generally useful ones).

[The official documentation](https://docs.anaconda.com/miniconda/miniconda-install/)
provides different installation instructions for different machines,
as well as verification of installations.
sanity-checking of your Miniconda installation.
You may skip the optional steps.

Whether you set up conda via the Anaconda® Distribution or Miniconda
is a matter of preference.
My preference for Miniconda is due to a history of owning machines with limited storage.
The [conda site](https://docs.conda.io/projects/conda/en/stable/user-guide/install/)
gives the following tip.

> If you are just starting out, we recommend installing conda via the Miniconda installer.

On the other hand, using the Anaconda® Distribution
allows you to manage conda environments through a graphical user interface
(*i.e.*, Anaconda Navigator)
instead of a command line interface
(as with using Miniconda).

If you find it more practical (at least for the time being)
to use conda through the Anaconda® Distribution,
check out the [official documentation for Anaconda Navigator](https://docs.anaconda.com/navigator/),
especially the following guides:

- [*Overview*](https://docs.anaconda.com/navigator/overview/),
- [*Getting started with Navigator*](https://docs.anaconda.com/navigator/getting-started/),
  and
- [*Tutorials*](https://docs.anaconda.com/navigator/tutorials/).

To learn more about using conda in a command line interface,
please consult the [User guide](https://docs.conda.io/projects/conda/en/stable/user-guide/index.html).
My go-to and frequently consulted resources are:

- [*Getting started with conda*](https://docs.conda.io/projects/conda/en/stable/user-guide/getting-started.html), 
- [*Using conda for your projects*](https://docs.conda.io/projects/conda/en/stable/user-guide/tasks/creating-projects.html),
  and
- [*Managing environments*](https://docs.conda.io/projects/conda/en/stable/user-guide/tasks/manage-environments.html).

## Creating a `cve154` environment

At this point,
you should have a terminal application wherein you can call `conda` commands.
For simplicity, let us call this terminal application
the conda-supporting terminal.

- If you installed the Anaconda® Distribution,
  you should be able to find
  (*e.g.*, via the Start Menu in Windows,
  or via the Launchpad in MacOS)
  Anaconda Prompt.
- If you installed Miniconda on Windows,
  you should be able to find Miniconda Prompt
  (or, in some cases, Anaconda Prompt (Miniconda)).
- If you installed Miniconda on MacOS,
  you should be able to call `conda` commands through the Terminal app.

In a conda-supporting terminal,
enter the following command:

```bash
conda create --name cve154 --channel conda-forge python=3.12.5 jupyterlab=4.2.4 numpy=2.1.0 scipy=1.14.1 matplotlib=3.9.2
```

This will create a conda environment named `cve154`
with Python (version 3.12.5) installed therein,
and the following Python packages:

- [JupyterLab](https://jupyterlab.readthedocs.io/en/stable/index.html) (version 4.2.4),
- [NumPy](https://numpy.org/) (version 2.1.0),
- [SciPy](https://scipy.org/) (version 1.14.1),
  andd
- [Matplotlib](https://matplotlib.org/) (3.9.2)

Moreover, conda will look for Python and the said packages in the conda-forge channel.

Follow the prompts to complete the process,
and make sure you are connected to the internet.

To verify that the environment is created,
you should see `cve154` in the result of running the command

```bash
conda env list
```

Of course,
the above-mentioned task of creating the `cve154` environment
can be accomplished through Anaconda Navigator
— and much easier at that.
You should be able to do it after reading
the guide [*Getting started with Navigator*](https://docs.anaconda.com/navigator/getting-started/)
and the tutorials
[*Managing environments*](https://docs.anaconda.com/navigator/tutorials/manage-environments/),
[*Managing packages*](https://docs.anaconda.com/navigator/tutorials/manage-packages/),
and
[*Managing channels*](https://docs.anaconda.com/navigator/tutorials/manage-channels/).
