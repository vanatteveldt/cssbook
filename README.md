# Quarto book for Computational Analysis of Communication

This is a Work-in-Progress quarto re-render of the original latex+ipynb sources of the CAC book. 

When it is finished, it should replace the latex and html versions of the book and become the new 'canonical' source. 

# Setup

Steps needed to render the book:
 - Install quarto
 - Clone this repository
 - Set up a pythoon virtual env and install the `requirements.txt` file

On my system, the following works for these steps:

```
# Install quarto
wget https://github.com/quarto-dev/quarto-cli/releases/download/v1.2.313/quarto-1.2.313-linux-amd64.deb
sudo apt install ./quarto-1.2.313-linux-amd64.deb

# Clone the repository
git clone git@github.com:vanatteveldt/cssbook
cd cssbook

# Set up python virtual environment
python -m venv env
env/bin/pip install -r requirements.txt
```

# Render the book

```
RETICULATE_PYTHON=env/bin/python quarto render --to html
```
