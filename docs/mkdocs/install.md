# Installing mkdocs

MkDocs is a fast, simple and downright gorgeous static site generator that's geared towards building project documentation. Documentation source files are written in Markdown, and configured with a single YAML configuration file.

You can try to install mkdocs via a package manager

```bash
sudo [apt | dnf] install -y mkdocs
```

However, all repositories seem to be out of date install a very old version. It is recommended to install it through ```pip```.

## Manual Installation

In order to manually install MkDocs you'll need Python installed on your system, as well as the Python package manager, ```pip```. 

```
sudo [apt | dnf] install python-pip
pip install mkdocs
```

Ensure you do not use ```sudo``` with ```pip```. It will make it difficult to use mkdocs as you will have to be root or use sudo each time. It will also make the owner root for the files it creates.
