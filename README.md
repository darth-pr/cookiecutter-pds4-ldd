cookiecutter-pds4-ldd
=====================

A minimal [cookiecutter](https://github.com/audreyr/cookiecutter) template for PDS4 Local Data Dictionary (LDD) development. The resulting repository sets up an project structure and manages an LDD as though it were a python package. 

## Usage

    pip install cookiecutter
    git clone https://github.com/darth-pr/cookiecutter-pds4-ldd.git
    cookiecutter cookiecutter-pds4-ldd/

## Explanation

The decisions `cookiecutter-pds4-ldd` makes should all be explained here.

### README

* **README should use a Markdown (text) format**
  This is the format is compatible with many documentation tools and is a common format used for documentation on GitHub. One can configure [setuptools](https://setuptools.readthedocs.io) to use it, and can be used by [Sphinx](http://sphinx-doc.org/) with a simple conversion.
* **As few README files as possible**
  Additional README files (AUTHORS, CHANGELOG, etc) should be left to the user to create when necessary.

### LICENSE

* **Apache License 2.0**
  This template provides you the [Apache-2.0](https://choosealicense.com/licenses/apache-2.0/) licence.
  If you [choose another license](https://choosealicense.com/), you also need to update the `{{ package_name }}/setup.py` file:
  adjust the `classifiers` and `license` fields accordingly.

### `setup.py`

* **Use setuptools**
  It's the standard packaging library for Python. `distribute` has merged back into `setuptools`, and `distutils` is less capable.
* **setup.py should not import anything from the package**
  When installing from source, the user may not have the packages dependencies installed, and importing the package is likely to raise an `ImportError`.
* **setup.py should be the canonical source of package dependencies**
  There is no reason to duplicate dependency specifiers (i.e. also using a `requirements.txt` file). See the testing section below for testing dependencies.

### Testing

* **Use [Tox](https://tox.readthedocs.io) to manage test environments**
  Tox provides isolation, runs tests across multiple Python versions, and ensures the package can be installed.
* **Uses [pytest](https://docs.pytest.org) as the default test runner**
  This can be changed easily, though pytest is a easier, more powerful test library and runner than the standard library's unittest.
* **Define testing dependencies in `tox.ini`**
  Avoid duplicating dependency definitions, and use `tox.ini` as the canonical description of how the unittests should be run.
* **`tests` directory should not be a package**
  The `tests` directory should not be a Python package unless you want to define some fixtures.
  But the best practices are to use [PyTest fixtures](https://docs.pytest.org/en/latest/fixture.html) which provides a better solution.
  Therefore, the `tests` directory has no `__init__.py` file.
