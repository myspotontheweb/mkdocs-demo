# mkdocs-demo

Demo generating github pages website using [mkdocs](https://www.mkdocs.org/)

# Setup

Configure a python virtual env

    python3 -m venv .venv
    source .venv/bin/activate
    
Install software

    pip install mkdocs mkdocs-material mkdocs-diagrams mkdocs-kroki-plugin pymdown-extensions fontawesome_markdown
    sudo apt-get install graphviz
    
# Usage

Server locally on the following URL http://127.0.0.1:8000/

    mkdocs serve
    
Publish website to github pages: https://myspotontheweb.github.io/mkdocs-demo/

    mkdocs gh-deploy
    
Notes:

* mkdocs will automatically push to the branch "gh-pages" and configure the repo settings for github pages

# Maintenance

There is a Github Actions workflow configured to update the website associated with this repository

* [.github/workflows/ci.yml](https://github.com/myspotontheweb/mkdocs-demo/blob/main/.github/workflows/ci.yml)

The library dependencies, used by this job can be periodically updated by running this command:

    pip freeze > requirements.txt

