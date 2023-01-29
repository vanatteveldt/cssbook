# Quarto book for Computational Analysis of Communication

This is a Work-in-Progress quarto re-render of the original latex+ipynb sources of the CAC book. 

When it is finished, it should replace the latex and html versions of the book and become the new 'canonical' source. 

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
