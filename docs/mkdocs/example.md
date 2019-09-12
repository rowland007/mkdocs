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