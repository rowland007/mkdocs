# Overview

MkDocs is a fast, simple and downright gorgeous static site generator that's geared towards building project documentation. Documentation source files are written in Markdown, and configured with a single YAML configuration file.

# Manual Installation

In order to manually install MkDocs you'll need Python installed on your system, as well as the Python package manager, pip. 

```
sudo [apt | dnf] install python-pip
pip install mkdocs
```

# mkdocs.yml Example

```
site_name: MkDocs Test Document
site_url: https://rowland007.github.io/
site_description: Testing out MkDocs tools. 
site_author: Randy Rowland
repo_url: https://github.com/rowland007/rowland007.github.io/
strict: true
theme: windmill

markdown_extensions:
  - smarty
  - attr_list
  - admonition
  - toc:
      permalink: True
plugins:
  - search:
      lang: en

nav:
  - About: index.md
  - Security:
    - GPG: security/gpg.md
    - Syncthing: security/syncthing.md
```
