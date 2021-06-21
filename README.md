# ComputingCookbook

This is an introduction to our research work and basic software skillset that would be useful for projects.

To read the contents, access [this website]().

To contribute to the website / this repository, read the guidance below.

## Install
Install `Jupyter Book` to contribute to the repository. 

```bash
$ pip install -U jupyter-book 
```

## Contributing

### Writing content
Create your Markdown files / Jupyter notebooks. Reference them in the TOC (`_toc.yml`). 
See https://jupyterbook.org/intro.html for more guidance on how to write your pages.

For better version control, it is preferred that you write your Jupyter notebook using 
Markdown. A Jupyter notebook written entirely in Markdown needs a YAML frontmatter and looks like this:

````md
---
jupytext:
  cell_metadata_filter: -all
  formats: md:myst
  text_representation:
    extension: .md
    format_name: myst
    format_version: 0.13
    jupytext_version: 1.10.3
kernelspec:
  display_name: Python 3
  language: python
  name: python3
execution:
  timeout: 240
---

# Your title

```{code-cell}
code that will be executed like a Jupyter notebook cell
```

````

See https://jupyterbook.org/file-types/myst-notebooks.html for more information.

### Building
Every time you want to build:

```bash
$ jupyter-book build book
```

Note, if you installed `jupyter-book` with `-U` option, you might have to explicitly type:
```bash
$ $HOME/.local/bin/jupyter-book build book
```

You can now open the file `book/_build/html/index.html` to preview your changes.

## Updating Github Pages

If you have the right access permissions and the package `ghp-import` installed:
```bash
$ pip install -U ghp-import
```

then you can easily update the Github Pages after building:

```bash
$ ghp-import -n -p -f book/_build/html
```

## Built with
Using the awesome [Jupyter Book](https://jupyterbook.org/) and [Binder](https://mybinder.readthedocs.io/). Hosted on Github Pages.
