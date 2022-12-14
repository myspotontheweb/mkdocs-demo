# mkdocs-demo

Demo generating github pages website using [mkdocs](https://www.mkdocs.org/)

# Setup

The mkdocs-diagrams plugin depends on graphviz 

    sudo apt-get install graphviz

Configure a python virtual env

    python3 -m venv venv
    source venv/bin/activate
    
Install software

    pip install mkdocs mkdocs-material mkdocs-diagrams pymdown-extensions fontawesome_markdown
    
    
# Usage

Server locally on the following URL http://127.0.0.1:8000/

    mkdocs serve
    
Publish website to github pages: https://myspotontheweb.github.io/mkdocs-demo/

    mkdocs gh-deploy
    
Notes:

* mkdocs will automatically push to the branch "gh-pages" and configure the repo settings for github pages
