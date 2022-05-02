# Virtual Environment

## Installing Python and pip

```shell
brew install python@3
brew install python@2
```

Another option is [pyenv – Simple Python version management](https://github.com/pyenv/pyenv):

```shell
brew install pyenv
pyenv install 3.7.2
pyenv install 2.7.14
pyenv global 3.7.2
```

_Pipenv integrates with `pyenv` and will automatically install missing Python versions_
_if they’re required by a Pipfile._

## Pip

```shell
# install the package in your home directory
pip install --user requests
# list the packages you already have installed
pip freeze
# uninstall the package
pip uninstall requests
# install a package without copying the package's file
pip install -e <directory>
pip install -e git+https://github.com/rgalanakis/goless.git\#egg=goless
```

---

## venv

[Docs](https://docs.python.org/3/library/venv.html)

### Pros

* Built-in feature.
* Generates a config file.
* Doesn't require copying the Python binary to a project location.

### Cons

* Works only with Python 3.3+

---

## virtualenv

```shell
pip3 install virtualenv

# create environment
virtualenv -p python3 ~/project_dir
# (de)activate environment
cd ~/project_dir
source bin/activate
deactivate
```

### Pros

* Easy to upgrade via `pip`.
* Easily work with multiple versions of Python.
* Supports Python 2.7+

### Cons

* Copies Python binary for any new environment.

---

## pipenv

[Docs](https://pipenv.readthedocs.io/en/latest/)

```shell
brew install pipenv
# create a Pipfile and install a package
cd ~/project_folder
pipenv install requests
# (de)activate environment
pipenv shell
exit
# directly run a command
pipenv run python
pipenv run django-admin startproject project_name
# delete environment
cd ..
pipenv —-rm
```

### Compatibility With Non-pipenv projects

```shell
pip install -r requirements.txt
pipenv lock -r
```

### Pros

* Combines package and environment management into a single tool.
* Supports multiple sub-envs for project environment, e.g. `production` or `test`.
* `Pipfile` includes the list of packages, Python version and other information.

### Cons

* It's slow.
* Spawns a new subshell.
* By default, creates an environemnt in the current user’s home directory.
This can be solved with export `PIPENV_VENV_IN_PROJECT=1`.
* Supports loading `.env` files, but only when running `pipenv` shell and `pipenv run`.
* Does not handle any parts of packaging.
