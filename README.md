# Jupyter Notebook on Python

```shell
jupyter notebook
```

## Virtual Environment

```shell
python3 -m venv .venv
source .venv/bin/activate
```

## REPL

Visual Studio Code: `Cmd + Shift + P` -> `Python: Start REPL`:

```shell
>>> help(str)

>>> help(str.upper)
```

## The History of Python

* [Guido van Rossum: The Early Years of Python](https://youtu.be/xLVxoz-mQFs)
* [Guido van Rossum: The Modern Era of Python](https://youtu.be/rTTFh7HOlC0)
* [Guido van Rossum: BDFL Python 3 retrospective](https://youtu.be/Oiw23yfqQy8)

## PEPs

* [PEP 257 -- Docstring Conventions](https://www.python.org/dev/peps/pep-0257/)
* [PEP 440 -- Version Identification and Dependency Specification](https://www.python.org/dev/peps/pep-0440/)

## What I Don't Like About Python

TBD

## Tooling

* [Virtual Environment](virtualenv.md)

## VS Code Plugins

* [Python](https://marketplace.visualstudio.com/items?itemName=ms-python.python)
* [ImportMagic](https://marketplace.visualstudio.com/items?itemName=brainfit.vscode-importmagic)
* [autoDocstring](https://marketplace.visualstudio.com/items?itemName=njpwerner.autodocstring)
* [Django](https://marketplace.visualstudio.com/items?itemName=batisteo.vscode-django)

## Testing

* [pytest](pytest.md)

## Writing Documentation

* [reStructuredText Markup Specification](http://docutils.sourceforge.net/docs/ref/rst/restructuredtext.html)
* [Sphinx Extensions](https://www.sphinx-doc.org/en/master/usage/extensions/index.html)

```shell
pip install sphinx
sphinx-quickstart
# edit conf.py in doc/source
sphinx-build doc/source doc/build
sphinx-build -b doctest doc/source doc/build
```

## Copyright

Copyright (C) 2019 Andrey Krisanov. The notebook is licensed and distributed under the MIT license.
