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
