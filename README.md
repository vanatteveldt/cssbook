# Quarto book for Computational Analysis of Communication

This is a quarto re-render of the original latex+ipynb sources of the CAC book. 

It is now considered the 'canonical' source of the book, and we are using this version to publish the [cssbook.net](https://cssbook.net) open access version and to update it for a new version. 

There is a [github action](https://github.com/vanatteveldt/cssbook/actions) to automatically update [cssbook.net](https://cssbook.net) after each commit, so you can make small fixes directly on github and/or work locally and push your changes. 

# Setup

Steps needed to render the book:
 - Install quarto
 - Clone this repository
 - Activate the `renv` R virtual environment, e.g. using [renv/install.R]

On my system, the following works for these steps:

```
# Install quarto 
wget https://github.com/quarto-dev/quarto-cli/releases/download/v1.2.313/quarto-1.2.313-linux-amd64.deb
sudo apt install ./quarto-1.2.313-linux-amd64.deb

# Install prerequisites for R packages (might be incomplete, please add if you find more requirements)
sudo apt install gfortran cmake liblapack-dev libgsl-dev libpng-dev libpoppler-cpp-dev libmagick++-dev

# Clone the repository
git clone git@github.com:vanatteveldt/cssbook
cd cssbook

# Activate the renv
Rscript renv/install.R
```

# Render the book 

```
quarto render
```

# A note on caching

The first time to render the book will take a long time. 
After this, content is both *frozen* at the chapter level, and *cached* at the chunk level where sensible. 

Note that knitr caching for python does not preserve global variables, so python chunks that create objects used in another chunk should not be cached.
For R objects are cached so this is possible.

